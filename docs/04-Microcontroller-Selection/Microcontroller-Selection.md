---
title: Microcontroller-Selection
tags:
- tag1
- tag2
---

| ESP Info                                      |  Answer                                                                                                      |
| --------------------------------------------- |  --------------------------------------------------------------------------------------------------------- |
| Model                                          | ESP32-S33-WROOM-1-N4         |
| Product Page URL                                    | Found on [Espressif.com](https://www.espressif.com/en/products/socs/esp32-s3)                                                                                    |
| ESP32-S3-WROOM-1-N4 Datasheet URL                   | [ESP32-S3-WROOM-1-N4 Datasheet](https://documentation.espressif.com/esp32-s3-wroom-1_wroom-1u_datasheet_en.pdf)                                              |
| ESP32-S3 Datasheet URL                              | [ESP32-S3 Datasheet](https://documentation.espressif.com/esp32-s3_datasheet_en.pdf)                                                                              |
| ESP32-S3 Technical Reference Manual URL             | [ESP32-S3 Manual](https://documentation.espressif.com/esp32-s3_technical_reference_manual_en.pdf )                                                        |
| Vendor link                                         | [Digikey](https://www.digikey.com/en/products/detail/espressif-systems/ESP32-S3-WROOM-1-N4/16162639)                       |
| Code Examples                                       | [Code for reading audio samples via ESP32 ADC](https://github.com/atomic14/esp32_audio)  |
| External Resources URL(s)                           | [ESP32-S3 ADC documentation](https://docs.espressif.com/projects/esp-idf/en/latest/esp32s3/api-reference/peripherals/adc/index.html), [ESP32 UART programming guide](https://docs.espressif.com/projects/esp-idf/en/v4.3/esp32/api-reference/peripherals/uart.html), [Microphone Component datasheet](https://assets.alliedelec.com/image/upload/v1576062544/Datasheets/4f9566e4b3d0a2191a58ed099a30218b.pdf)  |
| Unit cost                                           | $5.06                                                               |
| Absolute Maximum Current for entire IC              | 500 mA                                                                 |
| Supply Voltage Range                                 | 3V-3.6V                                                |
| Absolute Maximum current <br> (for entire IC)       | 500 mA                                                                                     |
| Maximum GPIO current <br> (per pin)                 | 20 mA                                                                                     |
| Supports External Interrupts?                       | Yes                                                                                     |
| Required Programming Hardware, Cost, URL            | [link](https://docs.espressif.com/projects/esp-idf/en/latest/esp32s3/get-started/index.html)                                                                                  |

| Module         | # Available | Needed | Associated Pins (or * for any) |
| -------------- | ----------- | ------ | ------------------------------ |
| UART           | 3           | 1      |     GPIO 18                         |
| external SPI | 4         | 0      |                -              |
| I2C            | 2           | 0      | -                             |
| GPIO           | 45          | 4      | GPIO 1,2,5,6                              |
| ADC            | 20           | 1     | GPIO 4                              |
| LED PWM        | 8           | 1      | GPIO 12                            |
| USB Programmer | 1           | 1      | GPIO 20                            |




The ESP32 works well for my Microphone Subsystem because it provides sufficient processing capability in a compact design while offering multiple analog and digital I/O options. The RS PRO 7542100 microphone is an analog electret microphone so the ESP32’s built-in ADC will be used to sample the audio signal. The microcontroller processes the captured audio data and transmits it to the main system through UART communication. Additional GPIO and PWM-capable pins can be used to control a debug/status LED for subsystem feedback. Overall, the ESP32 provides the flexibility needed to interface with the analog microphone, process audio signals, and communicate reliably with the rest of the system.
