---
title: Module's Selected Major Components
---

## Module's Selected Major Components

The following sections describe the major components used in the Audio(microphone) Subsystem. These include the voltage regulator that provides a stable 3.3 V power supply and the microphone module that captures sound from the environment. Each component was chosen because it works well with the subsystem microcontroller and meets the power and performance needs of the project. Together, these parts allow the subsystem to reliably detect audio signals while keeping the design simple and efficient within the overall system.

### Power Management

**Selected Voltage Switchimg Regulator: TC1264-3.3VAB Regulator**

<img src="https://mm.digikey.com/Volume0/opasdata/d220001/medias/images/6286/150%7EC04-034%7EAB%7E3.jpg?hidebanner=true" 
     width="300" 
     alt="Product Image">


[Link to product](https://www.digikey.com/en/products/detail/microchip-technology/TC1264-3.3VAB/442615?gclsrc=aw.ds&gad_source=1&gad_campaignid=20790518593&gbraid=0AAAAADrbLli0ZT-PF-PBunQ9vVqrEbgw6&gclid=CjwKCAiAqKbMBhBmEiwAZ3UboBYWfaOkWoOk2i8Dx9zRFfUYjNxC4Bj-PdhP4Dzw3kDAWWd71TOCJxoCmtIQAvD_BwE)


### Microphone

**Selected Sensor:  RS PRO 7542100 Microphone**

<img src="https://res.cloudinary.com/rsc/image/upload/b_rgb:FFFFFF,c_pad,dpr_1.0,f_auto,q_auto,w_700/c_pad,w_700/F7542100-01" 
     width="300" 
     alt="Product Image">


 [Link to product](https://us.rs-online.com/product/rs-pro/7542100/71815654/?gclsrc=aw.ds&gad_source=1&gad_campaignid=22593105799&gbraid=0AAAAAD-9z7Fd9Zc_kUm8eCjX4V2buscHA&gclid=EAIaIQobChMIm4HlmtyGkAMVwTlECB1H-ABrEAQYASABEgLx1_D_BwE)  



-----------

*Table 1: Component selection*

**3.3 Volt-switching Regulator**

| **Component**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](https://mm.digikey.com/Volume0/opasdata/d220001/medias/images/6286/150%7EC04-034%7EAB%7E3.jpg?hidebanner=true)<br> TC1264-3.3VAB<br>$1.33/each<br>[link to product](https://www.digikey.com/en/products/detail/microchip-technology/TC1264-3.3VAB/442615?gclsrc=aw.ds&gad_source=1&gad_campaignid=20790518593&gbraid=0AAAAADrbLli0ZT-PF-PBunQ9vVqrEbgw6&gclid=CjwKCAiAqKbMBhBmEiwAZ3UboBYWfaOkWoOk2i8Dx9zRFfUYjNxC4Bj-PdhP4Dzw3kDAWWd71TOCJxoCmtIQAvD_BwE)                 |Broad Operating Temperature<br><br> Broad Operating Range<br><br>Through-Hole Packaging                                               | Inefficient for large voltage drops <br><br> Relatively high dropout voltage<br><br> High geat generation at higher load currents |
| ![](https://mm.digikey.com/Volume0/opasdata/d220001/derivates/1/010/103/MFG_AP6320x_sml.jpg)<br> LD1117-3.3TO-220 3.3V Voltage Regulator <br>$0.77/each<br>[link to product](https://www.digikey.com/en/products/detail/diodes-incorporated/AP63203WU-7/9858430?)                 |Inexpensive<br><br> Compact SMT Package<br><br> Wide Input Voltage Range                                               | Requires external components <br><br>Layout Sensitive<br><br> *Poor heat dissipation at high Vin. |
| ![](https://mm.digikey.com/Volume0/opasdata/d220001/medias/images/6311/846%7EHRP5%7E%7E5.jpg?hidebanner=true)<br> BA33DD0WHFP-TR<br>$2.72/each<br>[link to product](https://www.digikey.com/en/products/detail/rohm-semiconductor/BA33DD0WHFP-TR/3663736)                 | \* High current capability<br>\* Clean output <br>\* Wide Input Voltage Range                                               | \* Lower efficiency <br>\*Poor heat dissipation. |

**Choice:** Option 1: TC1264-3.3VAB regulator

**Rationale:** The TC1264-3.3VAB was chosen because it provides a steady 3.3 V output and can supply enough current for the system. It is simple to use, needs only a few extra components, and includes built-in protection for safety. The TO-220 package also helps with heat dissipation if required.


**Microphone**

| **Component**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](https://res.cloudinary.com/rsc/image/upload/b_rgb:FFFFFF,c_pad,dpr_1.0,f_auto,q_auto,w_700/c_pad,w_700/F7542100-01)<br>Option 1.<br> RS PRO 7542100 Microphone <br>$0.61/each<br>[link to product](https://us.rs-online.com/product/rs-pro/7542100/71815654/?gclsrc=aw.ds&gad_source=1&gad_campaignid=22593105799&gbraid=0AAAAAD-9z7Fd9Zc_kUm8eCjX4V2buscHA&gclid=EAIaIQobChMIm4HlmtyGkAMVwTlECB1H-ABrEAQYASABEgLx1_D_BwE)                 | Low cost & compact <br><br> Omnidirectional sound pickup <br><br> Low power requirement <br><br> Easy to integrate   | Not ideal for high-quality recordings <br><br> Noise limitations |        
| ![](https://mm.digikey.com/Volume0/opasdata/d220001/derivates/2/001/212/MFG_MFG_CMA-4544PF-W%28640x640%29.jpg?hidebanner=true)<br> Option 3. <br> CMA-4544PF-W Microphone <br> $0.76/each <br> [Link to product](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices-/CMA-4544PF-W/1869981?gclsrc=aw.ds&gad_source=1&gad_campaignid=20243136172&gbraid=0AAAAADrbLlj1J1-wrnvGXGv0h4K-eIZg2&gclid=Cj0KCQjwjL3HBhCgARIsAPUg7a68c1BZp6LEFrLCHPUIop5vsIPro80buftPfndr3yCjhH8FneqTxqMaAmJ3EALw_wcB) |  Good sound range <br><br> Low power use <br><br> Omnidirectional | Sensitive to Noise <br><br> Basic audio quality <br><br> Limited temperature range|
| ![](https://www.sparkfun.com/media/catalog/product/cache/a793f13fd3d678cea13d28206895ba0c/1/2/12758-02.jpg)<br> Option 2. <br> SparkFun Electret Microphone Breakout <br> $8.50/each <br> [Link to product](https://www.sparkfun.com/sparkfun-electret-microphone-breakout.html) |  Built-in amplifier <br> Ready to use <br> Wide operating voltage <br><br> Good for general sound |  Limited frequency range <br><br> Expensive <br> Analog output only |   

**Choice:** Option 3: RS PRO 7542100 Microphone 

**Rationale:** The RS Pro 7542100 Electret Microphone was chosen because it provides a simple and reliable omnidirectional audio capture solution with a standard 2V operating voltage and moderate sensitivity suitable for general sound input. This microphone has a broad frequency range for capturing speech and audio and is easy to integrate with minimal external circuitry. Its compact size and low supply current make it appropriate for space-constrained designs where basic sound detection or voice pickup is required.
