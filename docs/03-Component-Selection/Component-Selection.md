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


[Link to product](https://www.digikey.com/en/products/detail/rohm-semiconductor/BA33DD0WHFP-TR/3663736)


### Microphone

**Selected Sensor:  RS PRO 7542100 Microphone**

<img src="https://res.cloudinary.com/rsc/image/upload/b_rgb:FFFFFF,c_pad,dpr_1.0,f_auto,q_auto,w_700/c_pad,w_700/F7542100-01" 
     width="300" 
     alt="Product Image">


 [Link to product](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices-/CMA-4544PF-W/1869981?gclsrc=aw.ds&gad_source=1&gad_campaignid=20243136172&gbraid=0AAAAADrbLlj1J1-wrnvGXGv0h4K-eIZg2&gclid=Cj0KCQjwjL3HBhCgARIsAPUg7a68c1BZp6LEFrLCHPUIop5vsIPro80buftPfndr3yCjhH8FneqTxqMaAmJ3EALw_wcB)  



-----------

*Table 1: Component selection*

**3.3 Volt-switching Regulator**

| **Component**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](https://mm.digikey.com/Volume0/opasdata/d220001/medias/images/6286/150%7EC04-034%7EAB%7E3.jpg?hidebanner=true)<br> TC1264-3.3VAB<br>$1.33/each<br>[link to product](https://www.digikey.com/en/products/detail/microchip-technology/TC1264-3.3VAB/442615?gclsrc=aw.ds&gad_source=1&gad_campaignid=20790518593&gbraid=0AAAAADrbLli0ZT-PF-PBunQ9vVqrEbgw6&gclid=CjwKCAiAqKbMBhBmEiwAZ3UboBYWfaOkWoOk2i8Dx9zRFfUYjNxC4Bj-PdhP4Dzw3kDAWWd71TOCJxoCmtIQAvD_BwE)                 | \* High output capacity<br>\* Built in protection for over-current and temperature<br>\* Wide Operating Range                                               | \* High Dropout Voltage<br>\* Inefficient for power sensitive designs<br>\* Difficult with non-through hole designs |
| ![](https://mm.digikey.com/Volume0/opasdata/d220001/derivates/1/010/103/MFG_AP6320x_sml.jpg)<br> AP63203WU-7 IC 3.3V 2A TSOT23-6<br>$0.77/each<br>[link to product](https://www.digikey.com/en/products/detail/diodes-incorporated/AP63203WU-7/9858430?)                 | \* Inexpensive<br>\* Compact SMT Package<br>\* Wide Input Voltage Range                                               | \* Requires external components <br>\* Layout Sensitive<br>\*Poor heat dissipation at high Vin. |
| ![](https://mm.digikey.com/Volume0/opasdata/d220001/medias/images/6311/846%7EHRP5%7E%7E5.jpg?hidebanner=true)<br> BA33DD0WHFP-TR<br>$2.72/each<br>[link to product](https://www.digikey.com/en/products/detail/rohm-semiconductor/BA33DD0WHFP-TR/3663736)                 | \* High current capability<br>\* Clean output <br>\* Wide Input Voltage Range                                               | \* Lower efficiency <br>\*Poor heat dissipation. |

**Choice:** Option 3: BA33DD0WHFP-TR 3.3V 2A regulator

**Rationale:** The BA33DD0WHFP-TR is a 3.3 V regulator capable of handling up to 2 A and works over a wide input voltage range, while providing clean, low-noise output.  It requires only small ceramic capacitors and includes built-in protection features, which helps keep the PCB simple, compact, and reliable.

**Microphone**

| **Component**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](https://res.cloudinary.com/rsc/image/upload/b_rgb:FFFFFF,c_pad,dpr_1.0,f_auto,q_auto,w_700/c_pad,w_700/F7542100-01)<br>Option 1.<br> RS PRO 7542100 Microphone <br>$0.61/each<br>[link to product](https://us.rs-online.com/product/rs-pro/7542100/71815654/?gclsrc=aw.ds&gad_source=1&gad_campaignid=22593105799&gbraid=0AAAAAD-9z7Fd9Zc_kUm8eCjX4V2buscHA&gclid=EAIaIQobChMIm4HlmtyGkAMVwTlECB1H-ABrEAQYASABEgLx1_D_BwE)                 | \* Wide frequency response<br>\* High signal to noise ratio <br>\* Omni directoinal sound detection                                             | \* Limited output constraints<br>\* Can't handle extreme temps. |
| ![](https://www.sparkfun.com/media/catalog/product/cache/a793f13fd3d678cea13d28206895ba0c/1/2/12758-02.jpg)<br>\* Option 2. <br>\* Sparkfun microphone breakout <br>\* $8.50/each <br>\* [Link to product](https://www.sparkfun.com/sparkfun-electret-microphone-breakout.html) | \* Integrated amplifier <br>\* More compact <br> \* Wide operating voltage | * More expensive <br>\* Limited frequency range <br>\* Potential power noise                                                       |           
| ![](https://mm.digikey.com/Volume0/opasdata/d220001/derivates/2/001/212/MFG_MFG_CMA-4544PF-W%28640x640%29.jpg?hidebanner=true)<br>\* Option 3. <br>\* CMA-4544PF-W Microphone <br>\* $0.76/each <br>\* [Link to product](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices-/CMA-4544PF-W/1869981?gclsrc=aw.ds&gad_source=1&gad_campaignid=20243136172&gbraid=0AAAAADrbLlj1J1-wrnvGXGv0h4K-eIZg2&gclid=Cj0KCQjwjL3HBhCgARIsAPUg7a68c1BZp6LEFrLCHPUIop5vsIPro80buftPfndr3yCjhH8FneqTxqMaAmJ3EALw_wcB) | \* Minimizes background noise <br>\* Wide frequency range t <br> \* Uniform sensitivity in all directions | * Weaker sensitivity at lower voltages <br>\* requires external tuning <br>\* Lower sensitivity                                                      |

**Choice:** Option 3: CMA-4544PF-W Microphone 

**Rationale:** The compact size of this microphone will allow it to easily fit within the device. It's wide frequency range, omni-directional noise detection, and high signal-to-noise ratio lets it precisely read sound levels while minimizing background noise. 
