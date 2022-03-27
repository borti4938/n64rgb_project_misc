# A small Flex-PCB
## N64 RCP-NUS breakout


## Purpose

This PCB enables you to apply conditioning resistors to the RCP output pins. This is useful for any CPLD and FPGA RGB Kit like viletims N64RGB (public and commercial), N64RGBv1, N64RGBv2, N64Advanced and many more variations spread over the internet.

## Pinout

From top to bottom (RCP on left, connector right)

| **Pin** | **Signal** |
|:-------:|:-----------|
| 17 | GND |
| 16 | D0 |
| 15 | D1 |
| 14 | D2 |
| 13 | D3 |
| 12 | D4 |
| 11 | D5 |
| 10 | D6 |
| 9 | #DSYNC |
| 8 | VCLK |
| 7 | GND |
| 6 | LRCLK (Audio, A2) |
| 5 | SDATA (Audio, A1) |
| 4 | SCLK (Audio, A0) |
| 3 | GND |
| 2 | Ctrl. (controller port pin 2, pin 16 PIF-NUS) |
| 1 | Rst (pin 27 PIF-NUS) |


## Preparation

You need

- four resistor arrays: 4x47ohm parallel, SMD1206, e.g. CAT16-47R0F4LF / CAY16-47R0F4LF
- if you have resistors at the input of your N64RGB modding board, you need to replace them with ferrite beads (see BOM if for proper replacements)

Assemble the board. The resistor arrays don't have an orientation.

## Installation

Solder the FPC board to the output pins 6 - 28 (pin 5 has a dot, pin 30 also) of the RCP-NUS.

Connect pad for Ctrl. and Rst. as stated in the table above. More information about appropriate solder points can be found in the Guide.

Use the pads to connect your modding kit. Note the pinout of the modding kit. If possible, keep/run VCLK separated from data wires.