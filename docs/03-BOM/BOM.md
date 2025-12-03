---
title: Bill of Materials
tags:
- tag1
- tag2
---

## Overview
This Bill of Materials (BOM) lists all the parts needed for the trash-lid motor subsystem. This subsystem takes a signal from the external IR sensor system and uses an H-bridge to control a DC motor that opens and closes the trash lid. The BOM includes basic parts like resistors and capacitors, the H-bridge motor driver, the DC motor, connectors, and any power parts needed. Each item includes the quantity, cost, part number, and links for ordering or datasheets. This BOM makes it easy to buy the parts and put the system together for the EGR 304 project.

## Bill of Materials

*Table ##: BOM table

| **Part Name/Description** | **Qty** | **Unit Cost** | **Total Cost** | **Manufacture** | **Manufacturer #** | **Vendor Link** |**Datasheet Link** | **Schematic Reference Designators** |
|:--------------------|:----|:---------------|:-----|:--------|:-----|:-----|:----|:-----|
0.33uF capacitor | 1 | $0.42 | $0.42 | KEMET | C322C334Z5U5TA | [DigiKey](https://www.digikey.com/en/products/detail/kemet/C322C334Z5U5TA/3726088?gclsrc=aw.ds&gad_source=1&gad_campaignid=20228387720&gclid=Cj0KCQjwmYzIBhC6ARIsAHA3IkTUvAUXjaSi9dtqd5UQ1oWlLs1yzOiD5bXtdA-xDQW9BfX5BuDegBMaAuZIEALw_wcB) | [datasheet link](https://www.yageogroup.com/content/datasheet/asset/file/KEM_C1051_GOLDMAX_Z5U) | C1 |
0.1uF capacitor | 2 | $0.39 | $0.78 | KEMET | C322C104M5U5TA | [DigiKey](&gclid=Cj0KCQjwmYzIBhC6ARIsAHA3IkQtVsDJy4La9kynxretCKE3b74tBP1tosbPa4mKWG84mkcgQY-QJS8aAqSAEALw_wcB) | [datasheet link](https://www.yageogroup.com/content/datasheet/asset/file/KEM_C1051_GOLDMAX_Z5U) | C2,C3 |
12V DC Motor |	1	| $13.50 | $13.50	| Advanced Electronics |	33JPF-15380-50	| [Amazon](https://www.amazon.com/Gear-Motor-85RPM-12Vdc-Shaft/dp/B07G68215Y) | [datasheet link](https://web.archive.org/web/20230923052123/https://www.allelectronics.com/mas_assets/media/allelectronics2018/spec/DCM-416.pdf) |	D2 |
Light emitting diode	| 1	| $0.15 |	$0.15	| Würth Elektronik | 151051RS11000	| [DigiKey](https://www.digikey.com/en/products/detail/w-rth-elektronik/151051RS11000/4490012) | [datasheet link](https://www.we-online.com/components/products/datasheet/151051RS11000.pdf) |	D5 |
2A Fuse 5x20	|	1	|	$23.18 |	$23.18	|	OptiFuse|	FPK-2A	|	[DigiKey](https://www.digikey.com/en/products/detail/optifuse/FPK-2A/15791648?msclkid=c9695dff46011b736e0b34cfd9dd8a62&gclid=c9695dff46011b736e0b34cfd9dd8a62&gclsrc=3p.ds&gad_source=7&gad_campaignid=23118878093)|	[datasheet link](https://www.optifuse.com/optifuse_ecommerce_tools/datasheets/FPK.pdf)	|	F1	|
DC Barrel Jack Switch	|	1	|	$0.76 	|	$0.76	|	Same Sky 	|	PJ-102AH	|	[DigiKey](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices-/PJ-102AH/408448?gclsrc=aw.ds&gad_source=1&gad_campaignid=20470400566&gclid=Cj0KCQjwmYzIBhC6ARIsAHA3IkQ00erxY84KaNb76f-GhoW7_KGTMajcxsxgxcxuDGf4zAuZBoELFjgaAgW8EALw_wcB)	|	[datasheet link](https://www.sameskydevices.com/product/resource/pj-102ah.pdf)	|	J1	|
1x40 Male Pin Header 	|	1	|	$1.38 	|	$1.38	|	Würth Elektronik	|	61304011121	|	[DigiKey](https://www.digikey.com/en/products/detail/w-rth-elektronik/61304011121/4846884?gclsrc=aw.ds&gad_source=1&gad_campaignid=20234014242&gclid=Cj0KCQjwmYzIBhC6ARIsAHA3IkQj74aD2qkyl9gXP1vvacIFSDxMCCTU2mZye2Md541CcTs5KLA_BYEaAigvEALw_wcB)	|	[datasheet link](https://www.we-online.com/components/products/datasheet/61304011121.pdf)	|	J2	|
1x40 Female Pin Header	|	1	|	$2.62 	|	$2.62	|	Würth Elektronik	|	61304011821	|	[DigiKey](https://www.digikey.com/en/products/detail/w-rth-elektronik/61304011821/17737790?gclsrc=aw.ds&gad_source=1&gad_campaignid=20234014242&gclid=Cj0KCQjwmYzIBhC6ARIsAHA3IkSrBbHIttfTkBAGKjd84wbJuTr9hJ_bDcTv-T7naRNIRnS72dbaa84aAneZEALw_wcB)	|	[datasheet link](https://www.we-online.com/components/products/datasheet/61304011821.pdf)	|	J3	|
Various Value Resistors 1/4W	|	1	|	$10.54 	|	$10.54	|	SparkFun Electronics	|	10969	|	[DigiKey](https://www.digikey.com/en/products/detail/sparkfun-electronics/10969/14671649?gclsrc=aw.ds&gad_source=1&gad_campaignid=20243136172&gclid=Cj0KCQjwmYzIBhC6ARIsAHA3IkRiqGplW81Ppf_4C1B_BSMUlbRJ_S3UcfGGw_oBA3Vsh1-jwst-gp0aAou3EALw_wcB)	|	n/a	|	R1-R10	|
Push Buttons	|	1	|	$0.10 	|	$0.1	|	Same Sky 	|	TS02-66-55-BK-100-LCR-D	|	[DigiKey](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices-/TS02-66-55-BK-100-LCR-D/15634297?gclsrc=aw.ds&gad_source=1&gad_campaignid=20243136172&gclid=Cj0KCQjwmYzIBhC6ARIsAHA3IkShnAVMbs1ppFFGpDy-OZeny5IyB8qEd0es-Ol-RUmWaSK4jIJGIKcaAjNIEALw_wcB)	|	[datasheet link](https://www.sameskydevices.com/product/resource/ts02.pdf)	|	SW1	|
Test Point	|	5	|	$0.39 	|	$1.95	|	Keystone Electronics	|	5000	|	[DigiKey](https://www.digikey.com/en/products/detail/keystone-electronics/5000/255326?gclsrc=aw.ds&gad_source=1&gad_campaignid=20228387720&gclid=Cj0KCQjwmYzIBhC6ARIsAHA3IkTpAks25bo8SQJEHmZHCBSWT_xgnynZ6hOmM03b7lduz7YzHTczqk4aAtdXEALw_wcB)	|	[datasheet link](https://www.keyelco.com/userAssets/file/M65p56.pdf)	|	TP1	|
PIC18F57Q43 Curiosity Nano	|	1	|	$9.99 	|	$9.99	|	Microchip	|	DM164150	|	[Microchip](https://www.microchip.com/en-us/development-tool/dm164150)	|	[datasheet link](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ProductDocuments/UserGuides/PIC18F57Q43-Curiosity-Nano-HW-UserGuide-DS40002186B.pdf)	|	U1	|
H-Bridge 	|	1	|	$0.80 	|	$0.80	|	onsemi 	|	FAN8100N	|	[DigiKey](https://www.digikey.com/en/products/detail/onsemi/FAN8100N/966896)	|	[datasheet link](https://mm.digikey.com/Volume0/opasdata/d220001/medias/docus/1021/FAN8100N%2CMTC.pdf)	|	U2	|
LM7805 Voltage Regulator 	|	1	|	$0.50 	|	$0.5	|	STMicroelectronics	|	L7805CV	|	[DigiKey](https://www.digikey.com/en/products/detail/stmicroelectronics/L7805CV/585964?gclsrc=aw.ds&gad_source=1&gad_campaignid=20228387720&gclid=Cj0KCQjwmYzIBhC6ARIsAHA3IkT7l51KsMQlvT5aFTGSM2XdK1rWcEssLr9AxKhiESSAD9dUmHo0sXwaAvwdEALw_wcB)	|	[datasheet link](https://www.st.com/content/ccc/resource/technical/document/datasheet/41/4f/b3/b0/12/d4/47/88/CD00000444.pdf/files/CD00000444.pdf/jcr:content/translations/en.CD00000444.pdf)	|	U3	|
2x4 IDC Connector with 8-wire ribbon cable	|	1	|	$5.27 	|	$5.27	|	Samtec Inc.	|	IDSS-08-D-06.00-RW	|	[DigiKey](https://www.digikey.com/en/products/detail/samtec-inc/IDSS-08-D-06-00-RW/9733997)	|	[datasheet link](https://www.digikey.com/en/products/detail/samtec-inc/IDSS-08-D-06-00-RW/9733997)	|	U6	|
Jumpers	|	10	|	$0.28 	|	$2.8	|	Würth Elektronik	|	60900213421	|	[DigiKey](https://www.digikey.com/en/products/detail/w-rth-elektronik/60900213421/2508447?gclsrc=aw.ds&gad_source=1&gad_campaignid=20234014242&gclid=Cj0KCQjwmYzIBhC6ARIsAHA3IkQMud7idbNs65WLQuZnHl9jCsljuTxIC1ijsRRhDfBb-vuXHQKzqbsaAhOfEALw_wcB)	|	[datasheet link](https://www.we-online.com/components/products/datasheet/60900213421.pdf) |	n/a	|
IC Sockets 8-Pin	|	10	|	$0.21 	|	$2.1	|	TE Connectivity AMP Connectors	|	1-2199298-2	|	[DigiKey](https://www.digikey.com/en/products/detail/te-connectivity-amp-connectors/1-2199298-2/5022039?gclsrc=aw.ds&gad_source=1&gad_campaignid=20234014242&gclid=Cj0KCQjwmYzIBhC6ARIsAHA3IkQiOlzCmqA2vXbJeWMKFgAs_-2NHBWdR99ihq-Z9xXHAzUo6FPEXeEaAv_kEALw_wcB)|	[datasheet link](https://www.te.com/usa-en/product-1-2199298-2.datasheet.pdf)	|	n/a	|






