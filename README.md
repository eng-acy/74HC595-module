<h1 align="center">74HC595 Module</h1>

An 8-bit SIPO (Serial-In, Parallel-Out) shift register board for learning how the 74HC595 works.
**DATA IN**, **CLOCK**, **LATCH** and **CLEAR** are entered by hand with push buttons, and the eight outputs are shown on LEDs.
Boards can be chained through 6-Pin JST-XH connectors.

## Features
- 74HC595 (optional DIP-16 socket)
- 4 push buttons: **DATA IN**, **CLOCK**, **LATCH**, **CLEAR**, each with an indicator LED
- 8 output LEDs (O1–O8) plus a 01×08 header for the outputs
- USB-C 5V input (Power only) with a 0.5 A resettable PTC fuse and reverse-polarity clamp
- Chain IN / OUT on 6-Pin JST-XH: **+5V**, **RCLK**, **SRCLK**, **SRCLR**, **SER_IN/O8'**, **GND**

## Specifications
| Specification | Description |
|---|---|
| Board size | 100×62 mm, 04×M3 mounting holes |
| Layers | 2, GND pour on both sides |
| Power | 5V via USB-C, about 90 mA max per board |

## 3D View

![Isometric view](documentation/3D-renders/render-iso.png)

![Top view](documentation/3D-renders/render-top.png)

![Bottom view](documentation/3D-renders/render-bottom.png)

## Repository contents
| Files / Folders | Description |
|---|---|
| [`74HC595-module.kicad_pro`](74HC595-module.kicad_pro) | KiCad 10 project (open this to open the entire project) |
| [`74HC595-module.kicad_sch`](74HC595-module.kicad_sch) | KiCad 10 schematic (open this to view only the schematic) |
| [`74HC595-module.kicad_pcb`](74HC595-module.kicad_pcb) | KiCad 10 pcb (open this to view only the pcb) |
| [`gerbers/`](gerbers/) | Gerber and drill files for manufacturing |
| [`documentation/`](documentation/) | Schematic PDF, Board Layout PDF, BOM, 3D Renders and GLB Model |
| [`3dmodels/`](3dmodels/) | Custom 3D models used by the board (Banded resistors, USB-C, Resettable PTC fuse) |

## Ordering the PCB
1. Zip the contents of [`gerbers/`](gerbers/) or download the Gerber zip from the [latest release](https://github.com/engadrianchristian-ctrl/74HC595-module/releases/latest).
2. Upload it to a PCB fab (e.g. JLCPCB or PCBWay).
3. Options: 2 layers, 1.6 mm FR-4, HASL lead-free finish, any solder mask colour.

## Assembly
- Parts list: [`documentation/74HC595-module-BOM.csv`](documentation/74HC595-module-BOM.csv)
- The IC can be soldered directly to the board or you can also buy a **DIP-16 IC socket**, which isn't listed in the BOM.
- Solder the SMD parts first (J1 USB-C, F1, D1, D2, R1–R3, C1), then the through-hole parts from lowest to tallest.
- Check polarity on the diodes, LEDs and C2.

## How to use
1. Plug in USB-C. The green power LED (D1) should light up.
2. While holding **DATA IN** (1) or leaving it released (0), press **CLOCK** to shift the bit to the shift register. Repeat shifting bits as desired.
3. Press **LATCH** to store the shifted bits to the output register (O1–O8).
4. Press **CLEAR** to reset the shift register, then press **LATCH** to clear the output register.

## Built with
KiCad 10.0

## License
This work, including the KiCad design files, Gerber and drill files, documentation, renders and 3D models in this repository, is licensed under the
[Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).

**You are free to:**
- **Share** – Copy and redistribute the material in any medium or format.
- **Adapt** – Remix, transform, and build upon the material for any purpose, even commercially.

**Under the following terms:**
- **Attribution** – You must give appropriate credit, provide a link to the license, and indicate if changes were made.
- **ShareAlike** – If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

You may share and adapt the design, including commercially, as long as you give credit and release your changes under the same license.

The full legal code is available at: [creativecommons.org/licenses/by-sa/4.0/legalcode](https://creativecommons.org/licenses/by-sa/4.0/legalcode)

See [`LICENSE`](LICENSE) for details.

## Author
<p align="left">
  <b>Adrian Christian Yap:</b>&emsp;
  <a href="https://www.linkedin.com/in/adrian-christian-yap-955712136/"><img align="absmiddle" height="28" alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZmZmZiIgZD0iTTIwLjQ1IDIwLjQ1aC0zLjU2di01LjU3YzAtMS4zMy0uMDItMy4wNC0xLjg1LTMuMDQtMS44NSAwLTIuMTQgMS40NS0yLjE0IDIuOTR2NS42N0g5LjM0VjloMy40MXYxLjU2aC4wNWMuNDgtLjkgMS42NC0xLjg1IDMuMzctMS44NSAzLjYgMCA0LjI3IDIuMzcgNC4yNyA1LjQ2djYuMjh6TTUuMzQgNy40M2EyLjA2IDIuMDYgMCAxIDEgMC00LjEzIDIuMDYgMi4wNiAwIDAgMSAwIDQuMTN6TTcuMTIgMjAuNDVIMy41NlY5aDMuNTZ2MTEuNDV6Ii8%2BPC9zdmc%2B&logoColor=white"></a>
</p>
<p align="left">
  <b>MFI Polytechnic Institute:</b>&emsp;
  <a href="https://www.mfi.edu.ph/"><img align="absmiddle" height="28" alt="MFI Website" src="https://img.shields.io/badge/MFI_Polytechnic_Institute_Inc-1B3A8C?style=flat&logo=data%3Aimage%2Fpng%3Bbase64%2CiVBORw0KGgoAAAANSUhEUgAAABsAAAAcBAMAAABi%2F9neAAAAMFBMVEXv8vUAAACt3tOoq8yioqSVybjcqVxNZ59JWZghMIv8xl9bZaZlm6o7VJGzmXIlB7CrbJm3AAAAEHRSTlP%2BAP7%2B%2Ff7%2Bhln%2F%2F%2F%2Ftaf4XeZJDxQAAAVpJREFUeNpFjc8rg3EAh5%2Fv9%2F2O%2FWreNyFLvI2DX4dllOTwZrWy0%2B74B5S4uSAH4ihXpeWgOEgrzkuSQslBXN6mOSCxSWvyzuvA%2BNyenvo8wjvN38SqWNr8R21MCts27LuQYdghO5dSwMQ8%2BZqZswGAZYB9bYPAGp5LBWw01659%2BQCQQNlTRnYDoABm61NcBKqW2ywzv63l%2FyyeS5lScRXrJ67FovFK1UZM88cCWNLO5azqldb7BcGOKgaG%2Bs6z4ZHob3dQxQadSXRAuqCynw4cpwERfCfZYrX5bo5LaTUnHEVya%2BHaH7Eb08F30eTLJRtfSv633ZJpFtTHjuUEz%2FKVhsVrOk9l8YDTkXLEvB8uyK6CxlX4OeTOxp9fDnsyoLcdkdiToW1LZnUdQzgpLZE5yTMuhK6oa58i86RdjLfXCVfzicfbUfXwOdSzXvQiDNxi6%2BMiK%2FLVwP0GeYxtvRISp6MAAAAASUVORK5CYII%3D"></a>
  <a href="https://www.facebook.com/MFIPolytechnic"><img align="absmiddle" height="28" alt="Facebook" src="https://img.shields.io/badge/Facebook-0866FF?style=flat&logo=facebook&logoColor=white"></a>
  <a href="https://www.linkedin.com/school/mfi-polytechnic-institute-inc/home/"><img align="absmiddle" height="28" alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZmZmZiIgZD0iTTIwLjQ1IDIwLjQ1aC0zLjU2di01LjU3YzAtMS4zMy0uMDItMy4wNC0xLjg1LTMuMDQtMS44NSAwLTIuMTQgMS40NS0yLjE0IDIuOTR2NS42N0g5LjM0VjloMy40MXYxLjU2aC4wNWMuNDgtLjkgMS42NC0xLjg1IDMuMzctMS44NSAzLjYgMCA0LjI3IDIuMzcgNC4yNyA1LjQ2djYuMjh6TTUuMzQgNy40M2EyLjA2IDIuMDYgMCAxIDEgMC00LjEzIDIuMDYgMi4wNiAwIDAgMSAwIDQuMTN6TTcuMTIgMjAuNDVIMy41NlY5aDMuNTZ2MTEuNDV6Ii8%2BPC9zdmc%2B&logoColor=white"></a>
</p>
