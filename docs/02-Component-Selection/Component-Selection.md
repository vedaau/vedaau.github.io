---
title: Component Selection
---

## Overview

The following are the components I have selected for my subsystem and the reason as to why I chose them.

**Motor**

| Solution | Pros  | Cons |
| ----- | ----- | ----- |
| **![](image1.png)** Option 1<br> VL53L1X ToF sensor <br> $3.5/each <br> [Link to Product](https://www.futureelectronics.com/p/semiconductors--analog--sensors--time-off-flight-sensors/vl53l1cxv0fy-1-stmicroelectronics-3100441) | High accuracy with distance measurements up to 4 meters.<br> <br> Fast response time.<br> <br>Compact size, making it easy to integrate into various devices.<br> <br>Low power consumption.<br> <br>Inexpensive | Performance can be affected by ambient light conditions.<br> <br>Limited range compared to some other ToF sensors.<br><br> Requires careful calibration for optimal accuracy.<br><br> May struggle with reflective surfaces or dark materials. |
| **![](image2.jpg)** Option 2 <br> OPB732 IR Sensor<br> $4/each<br> [Link to Product](https://www.onlinecomponents.com/en/productdetail/optek-technology-tt-electronics/opb732-51290988.html?msclkid=839b99712d5c180a0780f070a541179a&utm_source=bing&utm_medium=cpc&utm_campaign=Bing%20-%20Pmax%20-%20US%20-%20Low&utm_term=2332201602016770&utm_content=Other&gclid=839b99712d5c180a0780f070a541179a&gclsrc=3p.ds&gad_source=7&gad_campaignid=23052854090) | Known component and setup <br><br> Not too expensive <br><br> Compact <br><br> High availability | Limited range <br><br> No modern features <br><br> Interference sensitivity |
| **![](image3.png)** <br> Option 3 <br> Sharp GP2Y0A21YK0F IR analog distance sensor <br> $7.25/each <br> [Link To Product](https://www.jameco.com/z/GP2Y0A21YK0F-Sharp-Electronic-Components-Sharp-IR-Distance-Sensor-GP2Y0A21YK0F-_2150256.html?CID=digipart) | Easy to interface with microcontrollers.<br><br> Fast update rate for quick detection.<br><br> Compact size <br><br> Decent Range | Anything closer than 10 cm won’t be reliably measured. <br><br> High Power consumption. <br><br> Output signal is noisy and non-linear. <br><br>Lower accuracy at extremes <br><br> sensitivity to reflectance. | 

**Choice:** OPB732 IR Sensor  
**Rationale:** The OPB732 IR sensor is a simple and reliable option that’s easy to set up with the Curiosity Nano board. It doesn’t need extra parts to work and gives consistent distance readings for our project. It’s small, affordable, and well-known, which makes testing and integration quick and straightforward..

**H-Bridge** 

| Solution | Pros | Cons |
| ----- | ----- | ----- |
| **![](16999.jpg)** Option 1 <br> FAN8100N <br> $1.16/each <br> [Link to Product](https://www.digikey.com/en/products/detail/onsemi/FAN8100N/966896?&msclkid=4365b6bb40ef1801d8acdfa0c82914a2&gclid=4365b6bb40ef1801d8acdfa0c82914a2&gclsrc=3p.ds&gad_source=7&gad_campaignid=21987644300) | Simplicity, easy to use <br><br> I already own one <br><br> Cheap | No longer manufactured <br><br> Lacks advanced features  |
| **![](image5.jpg)** Option 2 <br> AMS1117-5.0 <br> $0.5/each <br> [Link to Product](https://www.digikey.com/en/products/detail/evvo/AMS1117-5-0/24370130) | Low Dropout Voltage <br><br> Widely Available <br><br> Compact package <br><br> Built-in Protections | Thermal Issues <br><br> Fixed Output <br> Sensitive to Capacitor Choice |
| **![](image6.jpg)** Option 3 <br> LM2596 <br> $2/each <br> [Link to Product](https://www.ti.com/lit/ds/symlink/lm2596.pdf) | Adjustable Output <br><br> Wide Input Voltage Range.<br><br> Integrated protection features.<br><br> Stable Output | Complex design <br><br> Generates electrical noise<br><br> Larger Circuit Footprint   |

**Choice:** LM7805  
**Rationale:** The LM7805 is an easy-to-use and dependable voltage regulator that works well with the Curiosity Nano board. It gives a stable 5V output and only needs a couple of capacitors to set up. It’s inexpensive, widely available, and provides reliable power for the sensor and other parts of the circuit, making it a practical choice for this project.

