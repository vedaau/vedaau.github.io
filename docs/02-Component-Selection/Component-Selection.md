---
title: Component Selection
---

## Overview

The following are the components I have selected for my subsystem and the reason as to why I chose them.

**Motor**

| Solution | Pros  | Cons |
| ----- | ----- | ----- |
| **![](image1.png)** Option 1<br> 33JPF-15380-50 12V Motor <br> $20/each <br> [Link to Product](https://www.futureelectronics.com/p/semiconductors--analog--sensors--time-off-flight-sensors/vl53l1cxv0fy-1-stmicroelectronics-3100441) | High torque for its size. <br> <br> controlled speed output.<br> <br>Simple 2-wire DC operation.<br> <br>I already have this.<br> <br>Metal gearbox. | Noise.<br> <br>Limited lifespan under heavy load.<br><br> low precision.|
| **![](image2.jpg)** Option 2 <br> OPB732 IR Sensor<br> $4/each<br> [Link to Product](https://www.onlinecomponents.com/en/productdetail/optek-technology-tt-electronics/opb732-51290988.html?msclkid=839b99712d5c180a0780f070a541179a&utm_source=bing&utm_medium=cpc&utm_campaign=Bing%20-%20Pmax%20-%20US%20-%20Low&utm_term=2332201602016770&utm_content=Other&gclid=839b99712d5c180a0780f070a541179a&gclsrc=3p.ds&gad_source=7&gad_campaignid=23052854090) | Known component and setup <br><br> Not too expensive <br><br> Compact <br><br> High availability | Limited range <br><br> No modern features <br><br> Interference sensitivity |
| **![](image3.png)** <br> Option 3 <br> Sharp GP2Y0A21YK0F IR analog distance sensor <br> $7.25/each <br> [Link To Product](https://www.jameco.com/z/GP2Y0A21YK0F-Sharp-Electronic-Components-Sharp-IR-Distance-Sensor-GP2Y0A21YK0F-_2150256.html?CID=digipart) | Easy to interface with microcontrollers.<br><br> Fast update rate for quick detection.<br><br> Compact size <br><br> Decent Range | Anything closer than 10 cm won’t be reliably measured. <br><br> High Power consumption. <br><br> Output signal is noisy and non-linear. <br><br>Lower accuracy at extremes <br><br> sensitivity to reflectance. | 

**Choice:** OPB732 IR Sensor  
**Rationale:** The OPB732 IR sensor is a simple and reliable option that’s easy to set up with the Curiosity Nano board. It doesn’t need extra parts to work and gives consistent distance readings for our project. It’s small, affordable, and well-known, which makes testing and integration quick and straightforward..

**H-Bridge** 

| Solution | Pros  | Cons |
| ----- | ----- | ----- |
| **![](16999.jpg)** Option 1 <br> FAN8100N <br> $1.16/each <br> [Link to Product](https://www.digikey.com/en/products/detail/onsemi/FAN8100N/966896?&msclkid=4365b6bb40ef1801d8acdfa0c82914a2&gclid=4365b6bb40ef1801d8acdfa0c82914a2&gclsrc=3p.ds&gad_source=7&gad_campaignid=21987644300) | Simplicity, easy to use <br><br> I already own one <br><br> Cheap | No longer manufactured <br><br> Lacks advanced features  |
| **![](ncv.jpg)** Option 2 <br> NCV7703CD2R2G <br> $2.40/each <br> [Link to Product](https://www.digikey.com/en/products/detail/onsemi/NCV7703CD2R2G/7325621) | Flexible motor/bridge control <br><br> Protection features built-in. <br><br> Cost-effective <br><br> Widely available. | Limited continuous current capability. <br><br> Potential complexity in firmware/hardware integration. |
| **![](image6.jpg)** Option 3 <br> LM2596 <br> $2/each <br> [Link to Product](https://www.ti.com/lit/ds/symlink/lm2596.pdf) | Adjustable Output <br><br> Wide Input Voltage Range.<br><br> Integrated protection features.<br><br> Stable Output | Complex design <br><br> Generates electrical noise<br><br> Larger Circuit Footprint   |

**Choice:** LM7805  
**Rationale:** The LM7805 is an easy-to-use and dependable voltage regulator that works well with the Curiosity Nano board. It gives a stable 5V output and only needs a couple of capacitors to set up. It’s inexpensive, widely available, and provides reliable power for the sensor and other parts of the circuit, making it a practical choice for this project.

