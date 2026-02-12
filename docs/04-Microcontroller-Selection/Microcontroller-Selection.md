---
title: Microcontroller Selection
tags:
- tag1
- tag2
---

## Overview
The microcontroller was selected based on its ability to handle the communication protocols (I2C, SPI, UART), provide sufficient I/O pins for peripherals, and operate within the 3.3V power budget while meeting all subsystem requirements.

## Microcontroller Comparison

*Table 1: Microcontroller Options*

| **Component** | **Pros** | **Cons** |
| ------------- | -------- | -------- |
| **Option 1**<br>PIC18F27Q10<br>$2.50/each<br>[Link to product](#) | Multiple communication peripherals<br><br>Low power consumption<br><br>Sufficient I/O pins | Limited processing power<br><br>Lower memory capacity |
| **Option 2**<br>ESP32-WROOM-32<br>$4.00/each<br>[Link to product](#) | Built-in Wi-Fi/Bluetooth<br><br>Dual-core processor<br><br>High processing power | Higher power consumption<br><br>More complex programming |
| **Option 3**<br>ATmega328P<br>$1.75/each<br>[Link to product](#) | Well documented<br><br>Easy to program<br><br>Low cost | Limited peripherals<br><br>Lower processing speed |

**Choice:** Option 1: PIC18F27Q10

**Rationale:** The PIC18F27Q10 was selected because it provides all necessary communication peripherals (I2C, SPI, UART) needed for interfacing with the microphone and other subsystem components, operates efficiently at 3.3V with low power consumption, and offers sufficient I/O pins for the subsystem requirements while maintaining compatibility with the overall system architecture.
