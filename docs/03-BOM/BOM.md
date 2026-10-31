---
title: Bill of Materials
tags:
- tag1
- tag2
---

## Overview
My BOM includes all the main components needed for my heart rate monitor PCB, including the 9V power supply, barrel jack, fuse, and L7805 voltage regulator to provide a stable 5V output. It also includes the PIC18F57Q43 Curiosity Nano board, an MCP6004 op-amp, a thermistor, resistors, capacitors, LEDs, and a pushbutton for the sensing and indicator circuits. Overall, these components provide the power, signal processing, and temperature indication needed for my design.

## Bill of Materials Table

*Table #1*

| **Part Name/Description** | **Qty** | **Unit Cost** | **Total Cost** | **Manufacture** | **Manufacturer #** | **Vendor Link** |**Datasheet Link** | **Schematic Reference Designators** |
|:--------------------|:----|:---------------|:-----|:--------|:-----|:-----|:----|:-----|
DC Barrel Jack, 5.5 × 2.1 mm, through-hole | 1 | $0.81 | $ 0.81 | Same Sky | PJ-002AH / CP-002AH-ND | [DigiKey](https://sc-b.digikeyassets.com/en/products/detail/same-sky-formerly-cui-devices/PJ-002AH/408446?utm_source) | [datasheet link](https://www.sameskydevices.com/product/resource/pj-002ah.pdf) | Tbd if needed |
DC Barrel Jack, 5.5 × 2.0 mm, through-hole | 1 | $0.83 | $0.83 | Same Sky | PJ-102AH / CP-102AH-ND | [DigiKey](https://www.digikey.com/en/products/detail/cui-devices/PJ-102AH/408448)  | [datasheet link](https://www.sameskydevices.com/product/resource/pj-102ah.pdf) | J1 Barrel_Jack_Switch
Quad Operational Amplifier, DIP-14 | 1 | $0.60 | $0.60 | Microchip Technology | MCP6004 | [DigiKey](https://www.digikey.com/en/products/detail/microchip-technology/MCP6004-I-P/523060?gclsrc=aw.ds&gad_source=1&gad_campaignid=20790518593&gbraid=0AAAAADrbLliJItBqguLw7XKry3y1w794w&gclid=CjwKCAjwl4HXBhAjEiwAHlpWhFUJ2dQqAaFPD_3AsAtwFl_I4R_VA-0ROPuMHdSRvImSbvAWkVXC_hoCsxIQAvD_BwE) | [datasheet link](https://ww1.microchip.com/downloads/en/DeviceDoc/MCP6001-1R-1U-2-4-1-MHz-Low-Power-Op-Amp-DS20001733L.pdf) | MCP6004-CM1-A, MCP6004-CM1-E
Quad Operational Amplifier, SOIC-14 | 1 | $0.58 | $0.58 | Texas Instruments | LM324W | [DigiKey](https://www.digikey.com/en/products/detail/texas-instruments/LM324N/277627) | [datasheet link](https://www.ti.com/lit/ds/symlink/lm224.pdf?HQS=dis-dk-null-digikeymode-dsf-pf-null-wwe&ts=1793124509824)  | Tbd if needed
Blue LED from SMRAZA kit | 1 | Included in kit | Included in kit | SMRAZA kit | Not Specified | PRLTA 109 | N/a | D1
Red LED from SMRAZA kit | 1 | Included in kit | Included in kit | SMRAZA kit | Not Specified | PRLTA 109 | N/a | D2
Ceramic Capacitor, 0.33 µF, 0.33 µF ±10% 100V Ceramic Capacitor X7R Radial | 1 | $0.88 | $0.88 | KEMET | C0805F104K5RACTU | [DigiKey](https://www.digikey.com/en/products/detail/kemet/C320C334K1R5TA/12701336) | [datasheet link](https://yageogroup.com/content/datasheet/asset/file/KEM_C1050_GOLDMAX_X7R)  | C1
0.1 µF Ceramic Capacitor, +/-10%, X7R, 50V, 0805 package |10 | 0.2750 | $2.75 | KEMET | C0805F104K5RACTU | [DigiKey](https://www.digikey.com/en/products/detail/kemet/C320C104K5R5TA/818040) |  [datasheet link](https://yageogroup.com/content/datasheet/asset/file/KEM_C1050_GOLDMAX_X7R) | C2, C3
Momentary Pushbutton from SMRAZA kit | 1 | Included in kit | Included in kit | SMRAZA kit | Not Specified | PRLTA 109 | N/a | SW1
5 V Linear Voltage Regulator, TO-220 | 1 | $1.53 | $1.53 | STMicroelectronics | L7805BV | [DigiKey](https://www.digikey.com/en/products/detail/stmicroelectronics/L7805ABV-DG/3945936) |  [datasheet link](https://www.st.com/content/ccc/resource/technical/document/datasheet/41/4f/b3/b0/12/d4/47/88/CD00000444.pdf/files/CD00000444.pdf/jcr:content/translations/en.CD00000444.pdf) | LM7805_CM
THERMISTOR NTC 10KOHM 3470K BEAD | 1 | $0.33 | $0.33 | Cantherm | MF52A2103J3470 | [DigiKey](https://www.digikey.com/en/products/detail/cantherm/MF52A2103J3470/1191033) |  [datasheet link](https://www.cantherm.com/wp-content/uploads/2017/05/cantherm_mf52_1.pdf) | TH1
Rotary Potentiometer, 10 kΩ, linear taper (10KB) | 1 | Included in kit | Included in kit | SMRAZA kit | Not Specified | PRLTA 109 | N/a | Potentiometer-CM1
Resistor, 10 kΩ, ±5%, ¼ W, carbon film, axial through-hole | 1 | Included in kit | Included in kit | SMRAZA kit | Not Specified | PRLTA 109 | N/a | R1
Resistor, 1 kΩ, ±5%, ¼ W, carbon film, axial through-hole | 1 | Included in kit | Included in kit | SMRAZA kit | Not Specified | PRLTA 109 | N/a | R3
9V 9 W AC/DC External Wall Mount (Class II) Adapter Fixed Blade Input | 1 | $11.41 | $11.41 | Pololu | 1470 | [DigiKey](https://www.digikey.com/en/products/detail/pololu/1470/19200211) |  [datasheet link](https://www.pololu.com/product-info-merged/1470) | N/a
FUSE GLASS 500MA 250VAC 5X20MM | 1 | $2.57 | $2.57 | Eaton - Electronics Division | BK/GDC-500MA | [DigiKey](https://www.digikey.com/en/products/detail/eaton-electronics-division/BK-GDC-500MA/264793?utm_source) |  [datasheet link](https://www.eaton.com/content/dam/eaton/products/electronic-components/resources/data-sheet/eaton-gdc-time-delay-glass-tube-fuses-data-sheet.pdf) | F1

## Bill of Materials Excel Image
![](ExcelBOM.png)
**Figure 2:** Excel Image


