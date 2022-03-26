RCP2Pads
---

A tiny **flexible** PCB which helps you to wire the [N64 Advanced PCB](https://github.com/borti4938/n64adv_pcb) or [N64RGB PCB](https://github.com/borti4938/n64rgb_pcb) to the video interface of the N64 RCP-NUS (graphical processor).
This board is also suitable for any other CPLD based N64RGB mod.

This PCB enables you to apply resistor based buffering to the RCP output pins for N64RGB installs (legacy board) or a IC based based buffer.


### Ordering the PCB

You can order the PCB from any manufacturer you like.
OSHPark flex service is greate for this boards and provides an unbeatable price for this small sized PCB.

### Pad Pinout

From top to bottom (RCP on left, connector right)

| **Pin** | **Signal** |
|:-------:|:-----------|
| 13 | GND |
| 12 | D0 |
| 11 | D1 |
| 10 | D2 |
| 9 | D3 |
| 8 | D4 |
| 7 | D5 |
| 6 | D6 |
| 5 | #DSYNC |
| 4 | VCLK |
| 3 | GND |
| 2 | Ctrl. (controller port pin 2, pin 16 PIF-NUS) |
| 1 | Rst (pin 27 PIF-NUS) |


### Preparation

You need components as listed in [BOM sheet](./doc/RCP2N64RGB_BOM.xlsx).
Assemble the board, which is rather straight forward.
The ferrite bead / resistor arrays don't have an orientation.

You may print the [assembly sheet](./doc/rcp2pads_assembly_sheet_top.pdf) for your orientation.
If you use a PCBA service, you may use the provided [mounting file](./doc/rcp2pads.mnt).


### Installation

Solder the FPC board to the output pins 8 - 28 (pin 5 has a dot, pin 30 also) of the RCP-NUS.

Connect pad for Ctrl. and Rst. as stated in the table above.
More information about appropriate solder points can be found in the installation guide of the [N64 Advanced PCB](https://github.com/borti4938/n64adv_pcb) or [N64RGB PCB](https://github.com/borti4938/n64rgb_pcb).

Use the pads to connect your modding kit.
Note the pinout of the modding kit.
If possible, keep/run VCLK separated from data wires.