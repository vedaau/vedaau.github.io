---
title: Component Selection
---

## Overview

The following are the components I have selected for my subsystem and the reason as to why I chose them.

**Motor**

| Solution | Pros  | Cons |
| ----- | ----- | ----- |
| **![](nfp.jpg)** Option 1<br> 33JPF-15380-50 12V DC Motor <br> $20/each <br> [Link to Product](https://www.ebay.com/itm/355883040232) | High torque for its size. <br> <br> controlled speed output.<br> <br>Simple 2-wire DC operation.<br> <br>I already have this.<br> <br>Metal gearbox. | Noise.<br> <br>Limited lifespan under heavy load.<br><br> low precision.|
| **![](rob.jpg)** Option 2 <br> ROB-11696 STANDARD MOTOR 12V <br> $2.75/each<br> [Link to Product](https://www.digikey.com/en/products/detail/sparkfun-electronics/11696/6163657) | Very low cost <br><br> Good no-load speed <br><br> Compact <br><br> High availability | Limited torque/power <br><br> No speed control <br><br> Noise, brush wear, and maintenance. |
| **![](fit.jpg)** <br> Option 3 <br> FIT0495-A 6V DC Motor <br> $10/each <br> [Link To Product](https://www.digikey.com/en/products/detail/dfrobot/FIT0495-A/7087178) | Simple and straightforward to use.<br><br> High torque. <br><br> Compact size <br><br> Decent Voltage Range | Very slow output speed <br><br> Limited to low-to-moderate workloads. <br><br> Low operating voltage. | 

**Choice:** 33JPF-15380-50 12V DC Motor 

**Rationale:** This motor was chosen because it provides good torque for its size, lets us control the speed easily, and only needs a simple 2-wire connection. It also works well with the mechanical load of my design. Since I already own this motor, we avoid extra cost and shipping delays.
The downsides such as some gearbox noise, lower precision, and shorter life under heavy use are acceptable because our project does not need high accuracy or long-term continuous operation.

**H-Bridge** 

| Solution | Pros  | Cons |
| ----- | ----- | ----- |
| **![](16999.jpg)** Option 1 <br> FAN8100N <br> $1.16/each <br> [Link to Product](https://www.digikey.com/en/products/detail/onsemi/FAN8100N/966896?&msclkid=4365b6bb40ef1801d8acdfa0c82914a2&gclid=4365b6bb40ef1801d8acdfa0c82914a2&gclsrc=3p.ds&gad_source=7&gad_campaignid=21987644300) | Simplicity, easy to use <br><br> I already own one <br><br> Cheap | No longer manufactured <br><br> Lacks advanced features  |
| **![](ncv.jpg)** Option 2 <br> NCV7703CD2R2G <br> $2.40/each <br> [Link to Product](https://www.digikey.com/en/products/detail/onsemi/NCV7703CD2R2G/7325621) | Flexible motor/bridge control <br><br> Protection features built-in. <br><br> Cost-effective <br><br> Widely available. | Limited continuous current capability. <br><br> Potential complexity in firmware/hardware integration. |
| **![](drv.jpg)** Option 3 <br> DRV8220DSGR <br> $0.88/each <br> [Link to Product](https://www.digikey.com/en/products/detail/texas-instruments/DRV8220DSGR/15295769) | Good output current for small / medium motors. <br><br> Low-power sleep mode.<br><br> Compact.<br><br> Wide voltage range. | Not for heavy-duty <br><br> Incompatible with PCB <br><br> Thermal / power dissipation constraints.  |

**Choice:** FAN8100N  
**Rationale:** I chose the FAN8100N driver because it is simple to use, fits easily into my circuit, and I already have it available. This saves time and avoids buying new parts. Although it lacks advanced features and may be older hardware, it is still suitable because the motor only needs basic control (on/off and forward/reverse). Long-term durability or advanced functions are not important for this project.

**Voltage Regulator** 

| Solution | Pros  | Cons |
| ----- | ----- | ----- |
| **![](lm78.PNG)** Option 1 <br> LM7805 <br> $0.55/each <br> [Link to Product](https://www.digikey.com/en/products/detail/texas-instruments/LM7805CT-NOPB/3901929) | Simplicity, easy to use <br><br> I already own one <br><br> Reliable | High dropout voltage <br><br> Gets hot  |
| **![](ua7.PNG)** Option 2 <br> UA7805CKCS <br> $1.34/each <br> [Link to Product](https://www.digikey.com/en/products/detail/texas-instruments/UA7805CKCSE3/1494012) | Can handle higher current <br><br> Very reliable design <br><br> Good performance under heavy loads | Also has a high dropout <br><br> Can create heat if input voltage is much higher than 5V. |
| **![](ams11.PNG)** Option 3 <br> AMS1117-5.0 <br> $0.12/each <br> [Link to Product](https://www.digikey.com/en/products/detail/evvo/AMS1117-5-0/24370130) | Lower dropout (about 1.1V) <br><br> Very cheap <br><br> Compact | Can only handle about 1A of current <br><br> Runs hot at high load <br><br> TNot as robust as the 7805  |

**Choice:** LM7805

**Rationale:** I chose the LM7805 because it is easy to use, reliable, and I already have one available. It provides a steady 5V output and works well for simple circuits like this project. Even though it has a higher dropout voltage and can get warm, the current needs of this project are so that it will still work fine.


**External Power Supply** 

| Solution | Pros  | Cons |
| ----- | ----- | ----- |
| **![](16999.jpg)** Option 1 <br> BestCH 9V 3.0A AC Adapter <br> $4.52/each <br> [Link to Product](https://www.digikey.com/en/products/detail/onsemi/FAN8100N/966896?&msclkid=4365b6bb40ef1801d8acdfa0c82914a2&gclid=4365b6bb40ef1801d8acdfa0c82914a2&gclsrc=3p.ds&gad_source=7&gad_campaignid=21987644300) | Reliable <br><br> Automatic overload cut off <br><br> No voltage fluctuations |  Higher heat output <br><br> Cannot handle high voltage  |
| **![](ncv.jpg)** Option 2 <br> DCU120050D4740 12V power supply <br> $7.65/each <br> [Link to Product](https://www.digikey.com/en/products/detail/onsemi/NCV7703CD2R2G/7325621) | Compact <br><br> Consistent voltage supply <br><br> Cost-effective <br><br> Widely available. | Unregulated current output <br><br> Low output current |
| **![](drv.jpg)** Option 3 <br> WR9HD1333CCP-F(R6B) 9V Power Supply <br> $6.23/each <br> [Link to Product](https://www.digikey.com/en/products/detail/texas-instruments/DRV8220DSGR/15295769) | Wide input voltage range <br><br> Sufficient voltage for small circuits <br><br> Efficient | Polarity & Connector Compatibility <br><br> Voltage Stability / Headroom Limitations  |

**Choice:** BestCH 9V 3.0A AC Adapter  
**Rationale:** This power supply gives a steady, reliable output and includes overload protection to keep your electronics safe. It powers on smoothly, helping avoid sudden voltage spikes that could harm your circuits or cause weird startup problems. Overall, it’s a dependable and easy-to-use option with helpful safety features.
