---
title: Module's Selected Major Components
---

## Module's Selected Major Components

The following sections describe the major components used in the Audio(microphone) Subsystem. These include the voltage regulator that provides a stable 3.3 V power supply and the microphone module that captures sound from the environment. Each component was chosen because it works well with the subsystem microcontroller and meets the power and performance needs of the project. Together, these parts allow the subsystem to reliably detect audio signals while keeping the design simple and efficient within the overall system.

### Power Management

**Selected Voltage Switchimg Regulator: LM2575GR-3.3V Regulator**

<img src="https://mm.digikey.com/Volume0/opasdata/d220001/derivates/1/001/176/122/MFG_TO-263-5L_sml%28200x200%29.jpg" 
     width="300" 
     alt="Product Image">


[Link to product](https://www.digikey.com/en/products/detail/taejin/LM2575GR-3-3/22237505)


### Microphone

**Selected Sensor:  CMEJ-0413-42-SMT-TR Microphone**

<img src="https://mm.digikey.com/Volume0/opasdata/d220001/derivates/1/010/508/MFG_CMEJ-0413-42-SMT-TR_sml.jpg" 
     width="300" 
     alt="Product Image">


 [Link to product](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices-/CMEJ-0413-42-SMT-TR/10253448)  



-----------

*Table 1: Component selection*

**3.3 Volt-switching Regulator**

| **Component**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](https://mm.digikey.com/Volume0/opasdata/d220001/derivates/1/001/176/122/MFG_TO-263-5L_sml%28200x200%29.jpg)<br> LM2575GR-3.3V Regulator <br>$0.60/each<br>[link to product](https://www.digikey.com/en/products/detail/taejin/LM2575GR-3-3/22237505)                 |Wide Input Voltage Range<br><br> Built-in Protection<br><br>Efficient Power Conversion                                               | Larger and Older Design <br><br> Noise |
| ![](https://cdn-shop.adafruit.com/970x728/2165-00.jpg)<br> LD1117-3.3TO-220 3.3V Voltage Regulator <br>$1.25/each<br>[link to product](https://www.adafruit.com/product/2165)                 |Inexpensive<br><br> Built-in protection<br><br> Widely available <br><br>Easy to use                                               | Inefficient for large voltage drops <br><br>Gets hot at higher current<br><br> Not suitable for battery efficiency|
| ![](https://mm.digikey.com/Volume0/opasdata/d220001/derivates/1/001/202/815/296%7E4202561%7EDDA%7E8_sml%28200x200%29.jpg)<br> Texas Instruments TPS7B8633DQDDARQ1 3.3V LDO <br>$2.30/each<br>[link to product](https://www.digikey.com/en/products/detail/texas-instruments/TPS7B8633DQDDARQ1/16627798)                 | Low idle current <br><br> Easy Integration <br><br> Wide Input Voltage Range                                               | Lower efficiency <br><br>Wastes power as heat <br><br> Requires external capacitors |

**Choice:** Option 1: LM2575GR-3.3V Regulator

**Rationale:** The LM2575GR-3.3V Regulator was chosen because it efficiently converts higher voltages to 3.3 V with low heat loss, and it can supply up to about 1 amp for microcontrollers and other circuits. It works from a wide range of input voltages and only needs a few extra parts, which is useful for most power supply designs. While not the smallest or newest part, it’s simple and reliable for stepping down to 3.3 V in many embedded projects.


**Microphone**

| **Component**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](https://res.cloudinary.com/rsc/image/upload/b_rgb:FFFFFF,c_pad,dpr_1.0,f_auto,q_auto,w_700/c_pad,w_700/F7542100-01)<br>Option 1.<br> RS PRO 7542100 Microphone <br>$0.61/each<br>[link to product](https://us.rs-online.com/product/rs-pro/7542100/71815654/?gclsrc=aw.ds&gad_source=1&gad_campaignid=22593105799&gbraid=0AAAAAD-9z7Fd9Zc_kUm8eCjX4V2buscHA&gclid=EAIaIQobChMIm4HlmtyGkAMVwTlECB1H-ABrEAQYASABEgLx1_D_BwE)                 | Low cost & compact <br><br> Omnidirectional sound pickup <br><br> Low power requirement <br><br> Easy to integrate   | Not ideal for high-quality recordings <br><br> Noise limitations |        
| ![](https://mm.digikey.com/Volume0/opasdata/d220001/derivates/2/001/212/MFG_MFG_CMA-4544PF-W%28640x640%29.jpg?hidebanner=true)<br> Option 2. <br> CMA-4544PF-W Microphone <br> $0.76/each <br> [Link to product](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices-/CMA-4544PF-W/1869981?gclsrc=aw.ds&gad_source=1&gad_campaignid=20243136172&gbraid=0AAAAADrbLlj1J1-wrnvGXGv0h4K-eIZg2&gclid=Cj0KCQjwjL3HBhCgARIsAPUg7a68c1BZp6LEFrLCHPUIop5vsIPro80buftPfndr3yCjhH8FneqTxqMaAmJ3EALw_wcB) |  Good sound range <br><br> Low power use <br><br> Omnidirectional | Sensitive to Noise <br><br> Basic audio quality <br><br> Limited temperature range|
| ![](https://mm.digikey.com/Volume0/opasdata/d220001/derivates/1/010/508/MFG_CMEJ-0413-42-SMT-TR_sml.jpg)<br> Option 3. <br> CMEJ-0413-42-SMT-TR Microphone <br> $0.59/each <br> [Link to product](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices-/CMEJ-0413-42-SMT-TR/10253448) |  Low Cost <br><br> Omnidirectional Pickup <br><br> Very Compact & Easy to Integrate <br><br> Good for general sound |  Limited frequency range <br><br> not suitable for professional audio <br><br> more noise and lower dynamic range |   

**Choice:** Option 3: CMEJ-0413-42-SMT-TR Microphone

**Rationale:** The CMEJ-0413-42-SMT-TR microphone was chosen because it is small, cheap, and easy to use. It picks up sound from all directions and works well for basic voice or environmental sound. Its low power needs and small size make it good for compact devices. While it is not high-quality audio and has a limited frequency range, it is reliable for simple sound detection.
