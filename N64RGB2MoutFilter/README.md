N64RGB2MoutFilter
---

A **flexible** PCB which connects the MultiOut with the [N64 Advanced PCB](https://github.com/borti4938/n64adv_pcb) or [N64RGB PCB](https://github.com/borti4938/n64rgb_pcb).
The connection PCB must be soldered on both ends - one end goes to the MultiOut, the other to the modding board.
To support older PCBs, I decided to go with the solder solution.
I future updates I may replace that and go with a FFC connector on the modding board side.

### Ordering the PCB

You can order the PCB from any manufacturer you like.
OSHPark flex service is fine, also the flex service from PCBWay does a great job.


### Assembly

Order the PCB and source the components as requested by the [BOM sheet](./doc/N64RGB2MoutFilter_BOM.xlsx).
Assembly should be straight forward.
You may print the [assembly sheet](./doc/n64rgb2multiout_assembly_sheet_top.pdf) for your orientation.

Please note that you have the option to include the [Filter AddOn](../FilterAddOn) on the flexible PCB or just leave it.
I recommend using the filter.

If you use a PCBA service, you may use the provided mounting file ([with filter](./doc/n64rgb2moutfilter_filteroption.mnt) or [without filter](./doc/n64rgb2moutfilter_nofilter.mnt)).

### Installation

Please read the installation guide of the [N64 Advanced PCB](https://github.com/borti4938/n64adv_pcb) or [N64RGB PCB](https://github.com/borti4938/n64rgb_pcb).

### Jumper Description

Use of SJ1 and SJ3 is also described in the installation guide of the [N64 Advanced PCB](https://github.com/borti4938/n64adv_pcb) or [N64RGB PCB](https://github.com/borti4938/n64rgb_pcb).
Just follow this guide and you came across to the point where you work with them.

#### SJ1

Sync source at MultiOut
 - SJ1.1 closed: forward sync to pin 7 of the MultiOut
 - SJ1.2 closed: forward sync to pin 3 of the MultiOut
 - you are allowed to close both sides of this jumper

#### SJ2

flex assembly setup (see [BOM sheet](./doc/N64RGB2MoutFilter_BOM.xlsx))
 - close all three jumpers if you do not use the filter assembly

#### SJ3

Sync source at the modding board
 - J3.1: Use TTL C-Sync (true TTL setup)
 - J3.2: Use 75ohm Sync (75ohm setup)
 - Never use both!
