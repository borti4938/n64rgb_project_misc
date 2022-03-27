# Filter Add On for N64 RGBv2 and N64 Advanced

This filter board is meant to use with the N64RGBv2 and N64 Advanced.
It can be used to filter the video signal coming out of the ADV7125 or to adjust signal levels such that one can use SNES PAL RGB cables.

The PCB can be sourced on every manufacturer you like.
Use a **PCB substrate thickness** as small as possible; e.g., 0.8mm at OSHPark.

- OSHPark: [my profile](https://oshpark.com/profiles/borti4938) -- get this PCB with 0.8mm (or less) substrate thickness
- PCBWay.com: [Link](http://www.pcbway.com/), [Affiliate Link](http://www.pcbway.com/setinvite.aspx?inviteid=10658)

## Filter Settings

The board utilizes the THS7368 with selectable filters.
The setup is done via inputs _F1_ and _F2_.

### N64RGBv2

- Leave _F1_ and _F2_ open or short the to GND to use the filter.
- Connect _F1_ and _F2_ to Vcc, i.e. +5V, to effectively bypass the filter.

### N64Advanced

Connect _F1_ and _F2_ to the modding board and use _J1_ to set it up.

## Jumper J1

With the jumper _J1_ you are able to forward composite sync input to either MultiOut pin 3 or pin 7.  
The composite sync input _/CS_ **is not** passed through the THS7386.
You can either connect TTL level sync or 75ohm attenuated sync, here.

## Additional Information

Please be referred to the [N64 Advanced PCB](https://github.com/borti4938/n64adv_pcb) or [N64RGB PCB](https://github.com/borti4938/n64rgb_pcb) repository for more information.

## BOM

- U1: THS7368
- C1: 0.1uF SMD0603 ceramic cap
- C2: 22uF SMD1206 ceramic cap
- RN1: 4x 75ohm resistor array SMD1206
- RN2:
  - NTSC cable:: 4x 75ohm resistor array SMD1206
  - PAL cable:: 4x 39ohm resistor array SMD1206
  
Assembly should by straight forward.
In [documentation folder](./doc/) you will find an excel sheet with the BOM as well as mounting files if you plan to use a PCBA service.

## Installation

This boards sits on the MultiOut pins.
Before you start, check the cable setup you plan to use.

Free the sync pin from the MultiOut, which means that you have to trace back the copper track from the MultiOut pin and make sure that there is nothing connected to.
- pin 3 (raw sync cable): usually unconnected. Only connected in earlier NTSC console (-CPU-01 to -CPU-03)
- pin 7 (luma sync cable): usually connected. Search for a nearby resistor or trace back to the DENC-NUS or MAV-NUS and lift the luma pin. Remove the resistor or lift the pin at the DENC-NUS or MAV-NUS. 

Solder the PCB to its place on the MultiOut pins such that pins align correctly.
Pin 1 on the PCB is marked with the square via on the MultiOut footprint.
The N64RGB or N64Adv modding board will be connected via the outer pads.
See the installation documentation of the respective board for more details.
