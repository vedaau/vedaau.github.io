---
title: Individal Block Diagram
tags:
- tag1
- tag2
---

## Overview
This subsystem automatically opens and closes the trash-can lid using a DC motor controlled by the PIC18F57Q43 Curiosity Nano. The microcontroller reads signals from the IR sensor through the shared connector, triggering the lid to open when a hand is detected and also reads the test button to ensure the lid can still operate if the sensor fails. It sends PWM control signals to the H-bridge, which drives the 12 V motor to open or close the lid smoothly while supporting safety features like obstruction detection and preventing excessive closing force. The red LED gives simple user feedback. Together, these components meet the key functional requirements: automatic opening, safe closing, pet/child lock behavior through software logic, resistance-based stop, and reliable operation across many cycles.

Power for the subsystem comes from a 9 V supply, while a 5 V regulator provides clean logic voltage to the Curiosity Nano and its I/O. This stable power path ensures durability and protects electronic components. The connector linking the IR sensor and UI lights enables easy assembly and disassembly for cleaning, supports adjustable sensor sensitivity through analog inputs, and keeps the design manufacturable and cost-efficient. Overall, the elements in the block diagram work together to deliver the required automation, safety, user interaction, and reliability while keeping the system simple to maintain and produce.



## Lid Motor Subsystem Block Diagram
Vedaa Ubale's Lid Motor Subsystem 

![Indivial Block diagram](vedaafinalblockdiagrammotorfinal.drawio.png)

## Diagram Link
A direct link to the source file of the block diagram can be found [here](finalbdvedaa.drawio)
