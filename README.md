# LAMPED - A SIMPLE LIGHT CONTROL MECHANISM
<br>  

<img width=100% alt="image" src="https://github.com/user-attachments/assets/79f0fd06-d780-490f-a6a7-fe14eaa620d1" />
<br>
<br>

A simple, desk-friendly LED “lamp” built around the **LM3914** LED driver: a **10‑LED circular array** that lights up progressively based on a **potentiometer** input. Powered from **5V USB**, designed in **KiCad**, and ready for fabrication (Gerbers + BOM + pick&place included).
<br>  
<br>


## Table of Contents
- [Overview](#overview)
- [How it works](#how-it-works)
- [Repository structure](#repository-structure)
- [Hardware (schematic & PCB)](#hardware-schematic--pcb)
- [Manufacturing files](#manufacturing-files)
- [Bill of Materials](#bom)
- [Assembly notes](#assembly-notes)
- [Usage](#usage)
- [Project journal](#project-journal)
- [License](#license)

---

## Overview
**LAMPED** is a small hardware project: turning a potentiometer makes LEDs light up sequentially (like a “level meter”), creating a lamp-like visual effect. The LEDs are arranged in a circle to mimic a bulb aesthetic.

Key points:
- **10 LEDs** in a circular pattern
- **LM3914** handles the LED level display logic
- **USB 5V power** (USB-A connector footprint on the board)
- Designed in **KiCad**
- Includes production outputs for fabrication & assembly

---

## How it works
The **LM3914** is a dot/bar display driver. In this design it’s used as a **10-step indicator**: as the potentiometer changes the input level, the IC activates LED outputs sequentially, producing a smooth “brighter/dimmer” visual progression.

---

## Repository structure
- `README.md` — project documentation (you are here)
- `JOURNAL.md` — build log / progress notes
- `src/` — KiCad source files (schematic, PCB, 3D model export)
  - `LAMPED.kicad_sch`
  - `LAMPED.kicad_pcb`
  - `LAMPED.kicad_pro`
  - `LAMPED.step`
- `production/` — manufacturing / assembly outputs
  - `gerbers.zip` — fabrication package
  - `LAMPED_bom.csv` — bill of materials export
  - `LAMPED_positions.csv` — pick & place / component positions
  - `LAMPED_designators.csv` — designators mapping
  - `netlist.ipc` — IPC netlist export
- `images/` — renders/photos here

---

## Hardware (schematic & PCB)
This project was inspired by an existing LM3914 LED lamp idea and then reworked into a custom KiCad design:
- Custom schematic in KiCad
- Bulb-shaped PCB outline
- Routing intentionally keeps the center area clear to preserve the visual design
<br>

### SCHEMATIC
 
<img width=100% alt="image" src="https://github.com/user-attachments/assets/50ad7688-248e-4473-be07-e0f020c6c042" />
<br>

### PCB
<div align="center">
  <table>
    <tr>
      <td valign="bottom"><img width="330" height="420" alt="image" src="https://github.com/user-attachments/assets/89e7096e-645f-4b43-b2e2-fd16c4cf1e40" /></td>
<td valign="bottom"><img width="370" height="420" alt="Capture d&#39;écran 2026-04-17 191458" src="https://github.com/user-attachments/assets/92893ec3-58d0-4f10-ac41-464cc5cfe0e1" /></td>
  </table>
</div>

---

## Manufacturing files
Ready-to-use outputs are included in `production/`:

- **Gerbers**: `production/gerbers.zip`
- **BOM**: `production/LAMPED_bom.csv`
- **Pick & place**: `production/LAMPED_positions.csv`
- **Designators**: `production/LAMPED_designators.csv`
- **Netlist**: `production/netlist.ipc`

Typical flow:
1. Upload `gerbers.zip` to your PCB manufacturer.
2. Use the BOM + positions file for assembly (if your manufacturer supports it).
3. Otherwise hand-solder using the BOM as reference.

---

## BOM

|Designator                             |Footprint                                       |Quantity|Value  |
|---------------------------------------|------------------------------------------------|--------|-------|
|D1, D10, D2, D3, D4, D5, D6, D7, D8, D9|LED_D5.0mm                                      |10      |LED    |
|J1                                     |USB_A_Molex_67643_Horizontal                    |1       |USB_A  |
|LM3914                                 |DIP-18_W7.62mm                                  |1       |LM3914N|
|POT1                                   |Potentiometer_Bourns_3386P_Vertical             |1       |10k    |
|R1                                     |R_Axial_DIN0204_L3.6mm_D1.6mm_P7.62mm_Horizontal|1       |100    |
|R2                                     |R_Axial_DIN0204_L3.6mm_D1.6mm_P7.62mm_Horizontal|1       |2.5k   |
|R3                                     |R_Axial_DIN0204_L3.6mm_D1.6mm_P7.62mm_Horizontal|1       |15k    |


## Assembly notes
General recommendations:
- **LED polarity**: ensure all LEDs are oriented correctly before soldering.
- **Solder order**: start with low-profile parts (resistors, IC socket if any), then LEDs, potentiometer, USB connector.
- **USB connector**: ensure mechanical alignment so it plugs in cleanly.

---

## Usage
1. Plug the board into a **5V USB** power source (computer USB port or USB power adapter).
2. Turn the **potentiometer** to see LEDs light up sequentially.

---

## Project journal
Progress notes and timelapses are in:
- `JOURNAL.md`

---

## License

This project is licensed under the [MIT License](./LICENSE).

---
