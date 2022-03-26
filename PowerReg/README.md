Power Regulator for N64RGB DAC
---

### Purpose

This little PCB is designed to used with
- [viletims N64RGB](http://etim.net.au/n64rgb/) project
- older boards from the [N64RGBv1 project](https://github.com/borti4938/n64rgb/tree/master/generalRGBmod/Main-PCB/v1)

This PCB has a regulator on board which generated 3.3V power supply for the mentioned mod-boards. It has been discussed at the [Shmups forums](https://shmups.system11.org/viewtopic.php?f=6&t=61455) that the output suffers from digital noise probably depending on CPU, PPU and APU load.  
Power the replacement RGB DAC from a different power supply source may help to 'decouple' this noise from the analog part.

##### Note
**[1]** Future releases may have a regulator on board. It has not been designed yet.

### Buiding the PCB

You may use any PCB prototype service of your choice or use a pre-existing [OSHPark project](https://oshpark.com/shared_projects/ofIFYk5I).  
**Order the board as thin as possible**; <1.0mm should be fine. This means for OSHPark service use 0.8mm substrate thickness.

### BOM

- U1: one of the following ICs, all SOT223 package (may named differently for each manufacturer)
  - NCP1117ST33T3G
  - TLV1117-33IDCYR
  - SPX1117M3-L-3-3/TR
- C1: 10-100uF/16V+ (SMD0805-1210)
- C2: 10-100uF/6.3V+ (SMD0805-1210)
- C3: 2.2uF / 6.3V+ (SMD0603)

### Installation

0. If not already done: assemble the PCB.
1. If you have an existing installation, first disconnect the 3.3V power supply wire from the modding board.  
   (Please look onto the pin out diagrams if you use viletims board - it may be one wire of the ribbon cable)
2. Solder the PCB under the power switch of the N64 mainboard (upper part) such that the PCB ranges to the inner side.
3. Connect the 3.3V output to the modding PCB

## ENJOY!!!!

### Acknowledgement

Many thanks to Womi ([circuit-board.de](https://circuit-board.de/forum/) user) for testing and giving feedback.  
Also many thanks to the shmups community for the discussion, especially but not limited to leonk, Syntax, kel, viletim, Thomas83lin, and many more...
