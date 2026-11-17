# 74HC595 Module

An 8-bit SIPO (serial-in, parallel-out) shift register board for learning how the 74HC595 works.
Data, clock, latch and clear are entered by hand with push buttons, and the eight outputs are shown on LEDs.
Boards can be chained through JST-XH connectors.

![3D render](documentation/3D-view/render-iso.png)

## Features
- 74HC595 in a DIP-16 socket
- 4 push buttons: **DATA IN**, **CLOCK**, **LATCH**, **CLEAR**, each with an indicator LED
- 8 output LEDs (O1–O8) plus a 1×8 header for the outputs
- USB-C 5 V input (power only) with a 0.5 A resettable PTC fuse and reverse-polarity clamp
- Chain IN / OUT on 6-pin JST-XH: +5V, SRCLK, RCLK, SRCLR, SER, GND

## Specifications
| | |
|---|---|
| Board size | 100 × 62 mm, 4 × M3 mounting holes |
| Layers | 2, GND pour on both sides |
| Supply | 5 V via USB-C, about 90 mA max per board |
| Min track / clearance | 0.2 mm / 0.2 mm |

## Repository contents
| Folder / file | What it is |
|---|---|
| `74HC595-module.kicad_pro` | KiCad 10 project (open this) |
| `gerber/` | Gerber and drill files for manufacturing |
| `documentation/` | Schematic PDF, board layout PDF, BOM, 3D renders and GLB model |
| `3dmodels/` | 3D models used by the board (banded resistors, USB-C, PTC fuse) |

## Ordering the PCB
1. Zip the contents of `gerber/`.
2. Upload it to a PCB fab (e.g. JLCPCB or PCBWay).
3. Options: 2 layers, 1.6 mm FR-4, **HASL lead-free** finish, any solder mask colour.

## Assembly
- Parts list: [`documentation/74HC595-module-BOM.csv`](documentation/74HC595-module-BOM.csv)
- Also buy a **DIP-16 IC socket**, which isn't listed in the BOM.
- Solder the SMD parts first (J1 USB-C, F1, D1, D2, R1–R3, C1), then the through-hole parts from lowest to tallest.
- Check polarity on the diodes, LEDs and C2.

## Usage
1. Plug in USB-C. The green power LED (D2) lights.
2. Set **DATA IN**, then press **CLOCK** to shift the bit in. Repeat for up to 8 bits.
3. Press **LATCH** to show the shifted bits on O1–O8.
4. Press **CLEAR** to reset the shift register.

## Built with
KiCad 10.0

## License
<!-- e.g. CERN-OHL-S-2.0, CC-BY-SA-4.0, or "All rights reserved" -->

## Author
<!-- your name / institution, as you want it shown publicly -->