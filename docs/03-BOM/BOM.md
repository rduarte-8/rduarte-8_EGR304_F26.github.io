---
title: Bill of Materials
tags:
- BOM
- EGR304
---

## Overview

The following Bill of Materials contains the components required for the pressure-pad subsystem. The subsystem includes the pressure sensor and signal-conditioning circuitry, PIC18F57Q43 Curiosity Nano, debug components, 5 V regulation, DC motor, H-bridge motor driver, and external 9 V power supply. Common resistors, capacitors, the LED, and pushbutton are sourced from the Smraza electronics component kit when available.

## Bill of Materials

*Table 1: Pressure Pad Subsystem Bill of Materials*

| **Part Name/Description** | **Qty** | **Unit Cost** | **Total Cost** | **Manufacturer** | **Manufacturer #** | **Vendor Link** | **Datasheet Link** | **Schematic Reference Designators** |
|:--------------------------|:-------:|:-------------:|:--------------:|:-----------------|:-------------------|:----------------|:-------------------|:------------------------------------|
| PIC18F57Q43 Curiosity Nano Evaluation Kit | 1 | $10.61 | $10.61 | Microchip Technology | DM164150 | [DigiKey](https://www.digikey.com/en/products/detail/microchip-technology/DM164150/11586705) | [Datasheet](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ProductDocuments/DataSheets/PIC18F27-47-57Q43-Data-Sheet-40002147.pdf) | PIC18F57Q43 Curiosity Nano |
| Force Sensing Resistor | 1 | $9.60 | $9.60 | Ohmite | FSR01CE | [DigiKey](https://www.digikey.com/en/products/detail/ohmite/FSR01CE/9178296) | [Datasheet](https://www.ohmite.com/assets/docs/res_fsr.pdf) | R1 |
| Quad Rail-to-Rail Operational Amplifier, 14-PDIP | 1 | $0.60 | $0.60 | Microchip Technology | MCP6004-I/P | [DigiKey](https://www.digikey.com/en/products/detail/microchip-technology/MCP6004-I-P/523060) | [Datasheet](https://ww1.microchip.com/downloads/en/DeviceDoc/21733j.pdf) | U3 |
| 5 V Linear Voltage Regulator, TO-220 | 1 | $1.01 | $1.01 | onsemi | MC7805CTG | [DigiKey](https://www.digikey.com/en/products/detail/onsemi/MC7805CTG/919333) | [Datasheet](https://www.onsemi.com/pdf/datasheet/mc7800-d.pdf) | U1 |
| Quad Half-H Motor Driver, 16-PDIP | 1 | $4.39 | $4.39 | Texas Instruments | SN754410NE | [DigiKey](https://www.digikey.com/en/products/detail/texas-instruments/SN754410NE/380180) | [Datasheet](https://www.ti.com/lit/ds/symlink/sn754410.pdf) | U4 |
| Brushed DC Motor, 3 V–12 V Operating Range | 1 | $11.50 | $11.50 | Mabuchi Motor | RF370CA-15370 | [DigiKey](https://www.digikey.com/en/products/detail/mabuchi-motor/RF370CA-15370/29784566) | [Product Information](https://product.mabuchi-motor.com/detail.html?id=78) | J5 / Motor |
| 9 V / 2 A, 18 W AC/DC Wall Adapter | 1 | $10.53 | $10.53 | Tensility | 16-00134 | [DigiKey](https://www.digikey.com/en/products/detail/tensility/16-00134/10324425) | [DigiKey Specifications](https://www.digikey.com/en/products/detail/tensility/16-00134/10324425) | External Power Supply |
| 5.5 mm OD / 2.1 mm ID Through-Hole DC Barrel Jack | 1 | $0.75 | $0.75 | Same Sky | PJ-202A | [DigiKey](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices/PJ-202A/252007) | [Datasheet](https://www.sameskydevices.com/product/resource/pj-202a.pdf) | J1 |
| 8-Position, 2×4, 2.54 mm Through-Hole Header | 1 | $1.86 | $1.86 | Molex | 0702460801 | [DigiKey](https://www.digikey.com/en/products/detail/molex/0702460801/760165) | [DigiKey Specifications](https://www.digikey.com/en/products/detail/molex/0702460801/760165) | J2 |
| 1.5 A Time-Delay Through-Hole Fuse | 1 | $1.78 | $1.78 | Littelfuse | 087501.5MXEP | [DigiKey](https://www.digikey.com/en/products/detail/littelfuse-inc/087501-5MXEP/2059458) | [DigiKey Specifications](https://www.digikey.com/en/products/detail/littelfuse-inc/087501-5MXEP/2059458) | F1 |
| 0.33 µF, 25 V Ceramic Capacitor | 1 | $0.45 | $0.45 | TDK | FA24X8R1E334KNU06 | [DigiKey](https://www.digikey.com/en/products/detail/tdk/FA24X8R1E334KNU06/24632530) | [DigiKey Specifications](https://www.digikey.com/en/products/detail/tdk/FA24X8R1E334KNU06/24632530) | C1 |
| 1×6, 2.54 mm Through-Hole Female Header | 1 | $0.79 | $0.79 | Harwin | D01-9970642 | [DigiKey](https://www.digikey.com/en/products/detail/harwin-inc/D01-9970642/3727951) | [DigiKey Specifications](https://www.digikey.com/en/products/detail/harwin-inc/D01-9970642/3727951) | J4 |
| 10 kΩ, 1/4 W Resistor | 3 | $0.05 | $0.15 | Smraza Kit / Generic | 10 kΩ | N/A - On Hand | N/A | R2, R3, R5 |
| 330 Ω, 1/4 W Resistor | 1 | $0.05 | $0.05 | Smraza Kit / Generic | 330 Ω | N/A - On Hand | N/A | R4 |
| 0.1 µF Ceramic Capacitor | 6 | $0.05 | $0.30 | Smraza Kit / Generic | 0.1 µF | N/A - On Hand | N/A | C2, C3, C4, C5, C6, C7 |
| 100 µF, 25 V Polarized Electrolytic Capacitor | 1 | $0.10 | $0.10 | Smraza Kit / Generic | 100 µF / 25 V | N/A - On Hand | N/A | C8/C9 |
| Standard LED | 1 | $0.05 | $0.05 | Smraza Kit / Generic | LED | N/A - On Hand | N/A | D1 |
| Momentary Tactile Pushbutton | 1 | $0.10 | $0.10 | Smraza Kit / Generic | Pushbutton | N/A - On Hand | N/A | SW1 |

**Estimated Total Cost: $54.62**

