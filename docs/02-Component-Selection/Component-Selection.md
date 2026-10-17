---
title: Component Selection
---

# Major Component Selection

## Pressure Sensor

*Table 1: Pressure Sensor Selection*

| **Solution** | **Pros** | **Cons** |
| --- | --- | --- |
| ![](FSR01CE.png)<br>**Option 1**<br>FSR01CE<br>Ohmite Force Sensing Resistor<br>[DigiKey Product Page](https://www.digikey.com/en/products/detail/ohmite/FSR01CE/9178296) | * Large sensing area is well suited for the pressure pad.<br>* Thin construction makes it easy to install under the pressure surface.<br>* Resistance output can be converted to voltage using a simple voltage divider.<br>* Requires relatively little supporting circuitry.<br>* Simple analog output is easy to interface with the signal-conditioning circuit. | * Resistance-to-force relationship is nonlinear.<br>* Less accurate than precision force sensors such as load cells.<br>* Output can vary depending on how force is distributed across the sensing area.<br>* Calibration is required for accurate force measurements. |
| ![](FSR02CE.png)<br>**Option 2**<br>FSR02CE<br>Ohmite Force Sensing Resistor<br>[DigiKey Product Page](https://www.digikey.com/en/products/detail/ohmite/FSR02CE/9178297) | * Compact size requires little installation space.<br>* Thin construction simplifies mechanical integration.<br>* Resistance output allows simple analog signal conditioning.<br>* Requires few supporting electrical components. | * Smaller sensing area is less suitable for the pressure pad.<br>* Force must be concentrated over a smaller area.<br>* Resistance-to-force relationship is nonlinear.<br>* Requires calibration for accurate force measurements. |
| ![](FSR03CE.png)<br>**Option 3**<br>FSR03CE<br>Ohmite Force Sensing Resistor<br>[DigiKey Product Page](https://www.digikey.com/en/products/detail/ohmite/FSR03CE/9178298) | * Larger sensing area than the FSR02CE.<br>* Thin construction allows installation underneath the pressure surface.<br>* Resistance output is easy to interface with analog circuitry.<br>* Requires relatively few supporting components. | * Sensing area is smaller than the FSR01CE.<br>* Nonlinear response makes precise force measurements difficult.<br>* Requires calibration for quantitative measurements.<br>* Output can vary with force distribution. |

**Choice:** Option 1: FSR01CE

**Rationale:** The FSR01CE was selected because its larger sensing area is better suited for the pressure-pad subsystem. Its resistance-based output can be converted into a voltage using a simple voltage divider and conditioned before being measured by the microcontroller. The subsystem primarily needs to detect changes in applied pressure rather than make precision force measurements, making the FSR01CE a suitable combination of sensing area, simple interfacing, and mechanical integration.

---

## Operational Amplifier

*Table 2: Operational Amplifier Selection*

| **Solution** | **Pros** | **Cons** |
| --- | --- | --- |
| ![](MCP6004-I/P.png)<br>**Option 1**<br>MCP6004-I/P<br>Microchip Technology<br>Quad Operational Amplifier<br>14-PDIP Through-Hole<br>[DigiKey Product Page](https://www.digikey.com/en/products/detail/microchip-technology/MCP6004-I-P/523060) | * Operates from 1.8 V to 6 V and is compatible with the 5 V rail.<br>* Rail-to-rail output provides a large usable output-voltage range.<br>* Four operational amplifiers are included in one IC.<br>* Low supply current reduces system power consumption.<br>* Through-hole PDIP package is easy to solder.<br>* Extra amplifier channels allow future expansion. | * 1 MHz gain-bandwidth product is lower than higher-performance alternatives.<br>* Four amplifier channels may be more than currently required.<br>* 14-pin package occupies more PCB space than an 8-pin dual amplifier.<br>* Cannot operate directly from supply voltages greater than 6 V. |
| ![](MCP6002-I/P.png)<br>**Option 2**<br>MCP6002-I/P<br>Microchip Technology<br>Dual Operational Amplifier<br>8-PDIP Through-Hole<br>[DigiKey Product Page](https://www.digikey.com/en/products/detail/microchip-technology/MCP6002-I-P/500875) | * Operates from 1.8 V to 6 V and is compatible with the 5 V rail.<br>* Rail-to-rail output is suitable for interfacing with the microcontroller ADC.<br>* Smaller 8-pin package requires less PCB space.<br>* Low supply current reduces system power consumption.<br>* Through-hole package simplifies soldering and assembly. | * Contains only two amplifier channels compared with four in the MCP6004.<br>* Future expansion could require an additional IC.<br>* 1 MHz bandwidth is lower than higher-performance alternatives.<br>* Provides fewer amplifier channels while offering similar electrical performance to the MCP6004. |
| ![](TLV2464IN.png)<br>**Option 3**<br>TLV2464IN<br>Texas Instruments<br>Quad Operational Amplifier<br>14-PDIP Through-Hole<br>[DigiKey Product Page](https://www.digikey.com/en/products/detail/texas-instruments/TLV2464IN/374297) | * Contains four operational amplifiers in one package.<br>* Compatible with the 5 V power rail.<br>* Rail-to-rail output provides a large usable output range.<br>* 6.4 MHz bandwidth provides greater performance than the MCP6004.<br>* Through-hole package simplifies manual PCB assembly. | * More expensive than the MCP6004 and MCP6002.<br>* Higher supply current increases system power consumption.<br>* Additional bandwidth is unnecessary for the slowly changing pressure-pad signal.<br>* 14-pin package provides no PCB-space advantage over the MCP6004. |

**Choice:** Option 1: MCP6004-I/P

**Rationale:** The MCP6004-I/P was selected because it provides four operational amplifiers, rail-to-rail output, low power consumption, and direct compatibility with the 5 V power rail. The MCP6002-I/P requires less PCB space but only provides two amplifier channels. The TLV2464IN provides greater bandwidth, but this additional performance is unnecessary for the relatively slow pressure-pad signal. The MCP6004-I/P therefore provides the required performance while also providing additional amplifier channels for future signal-conditioning requirements.

---

## 5 V Voltage Regulator

*Table 3: Voltage Regulator Selection*

| **Solution** | **Pros** | **Cons** |
| --- | --- | --- |
| ![](MC7805CTG.png)<br>**Option 1**<br>MC7805CTG<br>onsemi<br>5 V Linear Voltage Regulator<br>TO-220 Through-Hole<br>[DigiKey Product Page](https://www.digikey.com/en/products/detail/onsemi/MC7805CTG/919333) | * Provides the regulated 5 V output required by the subsystem.<br>* Through-hole TO-220 package simplifies manual soldering.<br>* High output-current capability provides substantial current margin.<br>* Common regulator architecture simplifies circuit implementation.<br>* Internal protection features improve reliability. | * Excess input voltage is dissipated as heat.<br>* Requires an input voltage sufficiently above 5 V to maintain regulation.<br>* Efficiency decreases as the difference between input and output voltage increases.<br>* Thermal management may be required at high load currents. |
| ![](UA7805CKCS.png)<br>**Option 2**<br>UA7805CKCS<br>Texas Instruments<br>5 V Linear Voltage Regulator<br>TO-220 Through-Hole<br>[DigiKey Product Page](https://www.digikey.com/en/products/detail/texas-instruments/UA7805CKCS/521612) | * Fixed 5 V output directly matches the required power rail.<br>* High output-current capability provides significant design margin.<br>* Internal thermal protection improves reliability.<br>* Internal current limiting provides protection during fault conditions.<br>* Through-hole TO-220 package simplifies assembly. | * Linear regulation dissipates excess input voltage as heat.<br>* Input voltage must remain sufficiently above 5 V.<br>* Current capability is much greater than required by this subsystem.<br>* Less efficient than a switching regulator when operating from a higher input voltage. |
| ![](LM2931T-5.0/PNOPB.png)<br>**Option 3**<br>LM2931T-5.0/NOPB<br>Texas Instruments<br>5 V Low-Dropout Linear Regulator<br>TO-220 Through-Hole<br>[DigiKey Product Page](https://www.digikey.com/en/products/detail/texas-instruments/LM2931T-5-0-NOPB/28104) | * Fixed 5 V output matches the required system voltage.<br>* Low-dropout design can operate with a lower input voltage than conventional 7805 regulators.<br>* Through-hole TO-220 package simplifies manual soldering.<br>* Lower dropout can reduce wasted voltage when the input supply is close to 5 V. | * Lower maximum output current than the 7805 alternatives.<br>* Provides less current margin for future expansion.<br>* Still dissipates excess input voltage as heat.<br>* Output-current capability must be verified using the final power budget. |

**Choice:** Option 1: MC7805CTG

**Rationale:** The MC7805CTG was selected because it provides the required regulated 5 V output and sufficient current capacity for the pressure-pad subsystem while maintaining additional current margin. Its through-hole TO-220 package is appropriate for manual PCB assembly. The LM2931 provides lower dropout but has less output-current capability, while the UA7805CKCS provides more current capability than the subsystem requires. The MC7805CTG therefore provides a simple and robust solution when paired with an appropriate external DC supply.

---

## DC Barrel Jack

*Table 4: DC Barrel Jack Selection*

| **Solution** | **Pros** | **Cons** |
| --- | --- | --- |
| ![](PJ-202A.png)<br>**Option 1**<br>PJ-202A<br>Same Sky<br>5.5 mm OD / 2.1 mm ID<br>Through-Hole DC Barrel Jack<br>[DigiKey Product Page](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices/PJ-202A/252007) | * Through-hole mounting provides a strong mechanical PCB connection.<br>* 5.5 mm by 2.1 mm size is suitable for commonly available DC adapters.<br>* Right-angle orientation allows convenient access from the PCB edge.<br>* Electrical ratings provide substantial margin for the subsystem.<br>* Integrated switching contact provides additional power-routing flexibility. | * Occupies more PCB area than smaller power connectors.<br>* Connecting and disconnecting the adapter applies mechanical force to the PCB.<br>* External supply must use a compatible 5.5 mm by 2.1 mm plug.<br>* Does not inherently protect against incorrect supply voltage or polarity. |
| ![](PJ-102A.png)<br>**Option 2**<br>PJ-102A<br>Same Sky<br>5.5 mm OD / 2.0 mm ID<br>Through-Hole DC Barrel Jack<br>[DigiKey Product Page](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices/PJ-102A/275425) | * Through-hole mounting provides good mechanical strength.<br>* Right-angle orientation is convenient for PCB-edge mounting.<br>* Electrical ratings exceed the expected subsystem requirements.<br>* Integrated switching contact provides additional power-routing options. | * 2.0 mm center pin is less compatible with common 2.1 mm plugs.<br>* Requires a specifically matched external power adapter.<br>* Occupies valuable PCB-edge space.<br>* Does not protect the circuit from an incorrect supply voltage or polarity. |
| ![](PJ-002A.png)<br>**Option 3**<br>PJ-002A<br>Same Sky<br>5.5 mm OD / 2.0 mm ID<br>Through-Hole DC Barrel Jack<br>[DigiKey Product Page](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices/PJ-002A/96962) | * Through-hole construction provides good mechanical strength.<br>* Electrical ratings provide substantial margin over the expected subsystem load.<br>* Right-angle configuration allows convenient PCB-edge access.<br>* Simple construction makes schematic integration straightforward. | * 2.0 mm center pin requires a matching external plug.<br>* Less compatible with common 2.1 mm adapters than the PJ-202A.<br>* Physical connector occupies significant PCB-edge space.<br>* Does not provide protection against incorrect external supply voltage or polarity. |

**Choice:** Option 1: PJ-202A

**Rationale:** The PJ-202A was selected because its through-hole construction provides a strong mechanical connection to the PCB and its right-angle orientation allows convenient access from the edge of the board. Its 5.5 mm outer diameter and 2.1 mm center-pin configuration provides a practical connection for an external DC power adapter. Its electrical ratings also provide substantial margin over the requirements of the pressure-pad subsystem. Compared with the other two options, the PJ-202A provides the preferred 2.1 mm center-pin connection for the planned external power supply.