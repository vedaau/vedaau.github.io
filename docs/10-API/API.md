# API

## Overview

This page documents the message API for the **Sable Audio Subsystem** (Microphone).  
My subsystem reads audio data from an ICS43434 I2S digital microphone and broadcasts
audio samples to the team over the daisy-chain UART network.

### Packet Structure (Class Protocol)

All messages follow the class-wide protocol:

| Byte | Value | Description |
|------|-------|-------------|
| 0 | `0x41` | Prefix byte 1 |
| 1 | `0x5A` | Prefix byte 2 |
| 2 | Source ID | Sender's node address |
| 3 | Dest ID | Receiver's node address (0xFF = broadcast) |
| 4–61 | Message Data | Up to 58 bytes of message content |
| 62 | `0x59` | Suffix byte 1 |
| 63 | `0x42` | Suffix byte 2 |

> My subsystem's **Source ID is 0x06** (Microphone/Audio node).  
> Messages I send are **broadcast** (Dest ID = 0xFF).

---

## Messages I Send

### Message Type 6 — Microphone Audio Stream

This message is broadcast to all nodes whenever a new audio sample is captured
from the ICS43434 I2S microphone.

|  | Byte 1 | Byte 2 | Bytes 3–4 |
|--|--------|--------|-----------|
| **Variable Name** | `message_type` | `reserved` | `audio` |
| **Variable Type** | `uint8_t` | `uint8_t` | `uint16_t` |
| **# of Bytes** | 1 | 1 | 2 |
| **Min Value** | 6 | 0 | 0 |
| **Max Value** | 6 | 0 | 65535 |
| **Example** | 6 | 0 | 32768 |

**Field descriptions:**
- `message_type`: Always `6` for this message type
- `reserved`: Unused byte, always `0`
- `audio`: 16-bit unsigned audio sample captured from ICS43434 microphone (0 = silence, 65535 = max amplitude)

---

## Messages I Receive

My subsystem does not have any message types specifically addressed to it.  
However, the receiver must handle **all messages** on the daisy chain according to the protocol:

- **Pass on** messages intended for someone else
- **Discard** messages that originated from me (source ID = 0x06 looping back)
- **Ignore** malformed messages (wrong prefix/suffix, oversized, or out-of-frame bytes)

For awareness, the other message types on the network are:

| Message Type | Description |
|---|---|
| 1 | Arm XYZ position → Armando |
| 2 | Arm XYZ position (Armando → HMI/Webuser) |
| 3 | Speed and movement type → Khalid |
| 4 | Speed and movement type (Khalid → HMI/Webuser) |
| 5 | Video feed stream information |
| **6** | **Microphone audio stream (MY MESSAGE)** |
| 7 | Speaker audio # (Stretch Goal) |

---

## Handling Code

### Message Receiver

The receiver handles all incoming UART daisy-chain messages:

```c
// Pseudocode for message receiver
#define MY_NODE_ID    0x06   // Microphone subsystem node ID

void process_received_message(uint8_t* buf, uint8_t len) {
    // Ignore messages larger than buffer
    if (len > 64) return;

    // Validate prefix and suffix
    if (buf[0] != 0x41 || buf[1] != 0x5A) return;
    if (buf[62] != 0x59 || buf[63] != 0x42) return;

    uint8_t source_id = buf[2];
    uint8_t dest_id   = buf[3];
    uint8_t msg_type  = buf[4];

    // Discard messages that originated from me (looped back)
    if (source_id == MY_NODE_ID) return;

    // Pass on messages not intended for me
    if (dest_id != MY_NODE_ID && dest_id != 0xFF) {
        uart_send(buf, len);
        return;
    }

    // Process messages intended for me (broadcast or direct)
    // (No specific message types addressed to my node currently)
    // Acknowledge receipt for debugging
    acknowledge_message(msg_type, source_id);
}
```

### Message Sender

The sender broadcasts audio samples at a rate controlled by a timer interrupt:

```c
#define MY_NODE_ID     0x06  // Microphone subsystem node ID
#define BROADCAST_ID   0xFF
#define MSG_TYPE_AUDIO 6
#define SEND_INTERVAL_MS 50  // Max send rate: 20 Hz

void send_audio_message(uint16_t audio_sample) {
    uint8_t packet[64] = {0};

    // Prefix
    packet[0] = 0x41;
    packet[1] = 0x5A;

    // Addressing
    packet[2] = MY_NODE_ID;   // Source: me (0x06)
    packet[3] = BROADCAST_ID; // Dest: everyone (0xFF)

    // Message data
    packet[4] = MSG_TYPE_AUDIO;   // message_type
    packet[5] = 0x00;             // reserved
    packet[6] = (audio_sample >> 8) & 0xFF;  // audio high byte
    packet[7] = audio_sample & 0xFF;          // audio low byte

    // Suffix
    packet[62] = 0x59;
    packet[63] = 0x42;

    uart_send(packet, 64);
}

// Timer interrupt — called every SEND_INTERVAL_MS
void __interrupt() timer_isr(void) {
    if (TMR0IF) {
        TMR0IF = 0;
        uint16_t sample = read_i2s_microphone();
        send_audio_message(sample);
        reload_timer();
    }
}
```

---

## Software Download

*(Link to zipped MPLabX project will go here)*

---

## Resources

- [Team Website](https://egr314-s-2026-303.github.io/)
- [Protocol Specification](https://embedded-systems-design.bitbucket.io)

