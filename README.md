# ZX-Max-128-Issue-3A June 2025
KiCAD created files for the ZX Max 128 Issue 3A designed by DonSuperfo

This Kicad project has only been done so as to allow for a proper ibom that 
includes tracks and vias to be created so as to make assembling easier.

I have tried to ensure that the footprints were located 
as close as possible to those in the original as well trying to follow 
the existing track and via locations. Some of the footprints that were 
downloaded from Digikey based on the parts in the official BOM do not fit 
exactly in their locations on the board. C15 is one example, I had to 
modify it's footprint to fit the pad dimensions. Some other capacitors also 
do not fit correctly but appear to be close enough.

As such, although I have tried to be as accurate as possible I would NOT 
use these gerbers to have a pcb manufactured without having another set of
eyes checking that the schematic that I have produced is correct to that 
produced by DonSuperfo and that the pcb data from Kicad reports no major errors 
with regards to copper tracing and via positions.

The KiCAD schematics 'should' be correct but nothing should be assumed as correct without checking with the original schematic and PCB layout. Although I have followed the original track and via layout further checking should be done before using these files to order a pcb with. Currently I would still order the pcb from PCBWay using the link from https://github.com/DonSuperfo/ZX-Max-128

Note that any part number for any device used in this project might not be the correct one from the original BOM as supplied from PCBWay as I had to change some parts to get a footprint that would fit in the space on the original pcb with the correct pin spacing. This required selecting a different part number or vendor. This applies mainly to capacitors. Some other parts are no longer available under that number from Digikey.

As always, measure twice and order one.

Use at your own risk.

For the jumpers/connectors on the board,

J1 8 Way Keyboard Connector

J2 5 Way Keyboard Connector

J3 ZX Expansion Connector

J4 DC Input - can be any polarity. 

J5 Video is a TRRS, Tip-Video,RR-Left/Right, Screen-Ground.

J6 Ear/Mic. Wired as per ZX Spectrum 128K +3. TRS. Tip-Mic, Ring-Ear, Screen-Ground.

J7 Not Used

J8 SCART, mates with a Sega megadrive cable.

J9 Not Used

J10 EEPROM/UVEPROM selection, EEPROM 2-4/1-3, UVEPROM 2-1/4-3.

J11 Speaker On/Off

J12 Not Used

J13 Not Used

J14 JTAG for the EPM7128 wired as standard to an Altera device.

J15 Not Used

J16 Disable DivMMC, close = enable DivMMC, open = disable DivMMC or need to update program on U17

SW1 RESET

From information on the original website ,

In order to make ACB output more balanced I would recommend following the -4.5dB 
panning law rule and make these updates:

R54, R55 = 470 Ohm
R51, R52 = 560 Ohm
R50, R53 = 330 Ohm

The ratio of 560 / 330 = 1.6969 is a close approximation of 1 / 10^(-4.5 / 20) = 1.6788. 
Also the resulting equivalent resistance is around 1000 Ohm which leads to less distortion on AY outputs.

mismatch between the value on the scheme and in the BOM for part R32 (INT)
on scheme it is 470R but in BOM 10k.
it looks like in BOM incorrect value.
