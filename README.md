# BLVMGNCube_Build

<pre>

============================================
BUILD STATUS: IN PROGRESS
============================================

I've come to inherit an old project from FB market place which was free when I bought a used ender 3 (05/13/2021).
He said he was planning to transfer the electronics parts on the E3 to the BLV MGN Frame and take it from there. 
Unfortunately he lost the bed that came with the kit and the project was put on hold. 
His wife got fed up that his project was just taking up space in their home so he had to let it go. 

</pre>

![image](https://user-images.githubusercontent.com/85612975/217283968-1fb5ded9-ec86-429c-8207-0e14b95588f8.png)

<pre>

Here's the BOM when I got the kit.
Extrusions: Full BLV Frame All metal kit from AliExpress (url https://www.aliexpress.us/item/2255801095103872.html?spm=a2g0o.productlist.main.111.a67a516934a58A&algo_pvid=694ec4a6-d118-4e1b-82b6-2a246fdb2c44&algo_exp_id=694ec4a6-d118-4e1b-82b6-2a246fdb2c44-55&pdp_ext_f=%7B%22sku_id%22%3A%2210000015591032066%22%7D&pdp_npi=2%40dis%21USD%21307.43%21307.43%21%21%21%21%21%4021224e9b16751041953849000d0666%2110000015591032066%21sea&curPageLogUid=wZVW1dkNe8kX&gatewayAdapt=glo2usa4itemAdapt&_randl_shipto=US)
Mobo: BTT SKR Mini E3 v1.2
ABL: Inductive Proximity Probe
Stepper Motors: 5 Generic Motors
PSU: 12V Generic
Extruder: All Metal MK8
Hotend: V6 Clone 

Getting the frame it was already pre built and square. I'll have to tear it down to be sure that it would be square.

The project was also put on the shelf on my end as there was no good alternative for the corroded rails at the time. Up until a few months ago, so here we are. trying to make this build with the cheap parts i have around.


PSU Wiring
https://howchoo.com/media/nj/hl/nz/ender-3-meanwell-psu-wiring.jpeg?width=900&auto=webp&quality=70

Timeline:

Ordered Parts:


Arrived:
02/08/2023 - Meanwell LR350 24v () 
02/08/2023 - 310x310mm Aluminum HotBed, no 350mm available at my end that was cheap and fast.
 - Silicon Bed spacer
 - M3x35mm bed screw
 - Dual Z Adapter Board
 - Bed Insulation
 - Magnetic PEI Spring Steel Sheet textured
 - PEI Sheet smooth 
 - 5x 400mm Linear Rails
 - SSR 040DA
 - EP2 Grease for Lead Screw
 - Optical End Switch
 - Cable Sleeve
 - DIN Rail
02/19/2023 - Frame is Built but chains are grinding. refitted gear teeth height.
02/20/2023 - All parts have arrived aside from the PEI Spring steel sheet plate

As per testing the bed was work but found out that the SKR Mini E3 Board I got has a broken mosfet in the FAN0.

doing a little search i was able to find this thread. Which looks like a common issue of this board. 
https://www.reddit.com/r/BIGTREETECH/comments/k00zkt/bypassing_burnt_heatbed_mosfet_on_skr_mini_e3_v12/

Broken Q2 Mosfet suitable replacement: 
IPD036N04LG 036N04L TO-252 data sheet ([IPD036N04L-Infineon.pdf](https://github.com/coolikot/BLVMGNCube_Build/files/10678586/IPD036N04L-Infineon.pdf))
https://datasheetspdf.com/pdf/1456904/Infineon/IPD036N04LG/1

AO3400A SOT23 (Same layout)
https://www.digikey.com/en/products/detail/alpha-omega-semiconductor-inc/AO3400A/1855772

Reported Issue under:
https://github.com/bigtreetech/BIGTREETECH-SKR-mini-E3/issues/238

SKR mini E3 v1.2 manual
([BTT SKR MINI E3 V1.2manual.pdf](https://github.com/coolikot/BLVMGNCube_Build/files/10678599/BTT.SKR.MINI.E3.V1.2manual.pdf))
https://github.com/bigtreetech/BIGTREETECH-SKR-mini-E3/blob/master/hardware/BTT%20SKR%20MINI%20E3%20V1.2/BTT%20SKR%20MINI%20E3%20V1.2manual.pdf

Will still try to fix said SKR Mini E3 v1.2 but for now will run the config below

XY Endstop : Optical Endswitch
Z Endstop : BL Touch
Extruder : Orig BMG will convert to Orbiter 2.0 with filament Runout sensor
Motherboard : SKR Mini E3 V3.0
Hotend : V6 Clone will upgrade to Phaetus Dragon once proper thermistor/heating cartridge arrive
ToolHead : Minimalistic Fan Duct in DD Config

02/20/2023 : All built and moving figuring out the firmware. Currently getting dragged when trying to home
02/21/2023 : Figured out what's causing the drag, the BTT SKR mini E3 V3 official firmware is causing it. Made my own marlin config everything is now okay.
02/22/2023 : Bed offsets are properly configured, as I am using at 310x310mm bed instead of 350x350.
Firmware Guide: 
Home Offset Explanation: https://www.youtube.com/watch?v=8MQRxBISYmU
CoreXY Marlin Setup : https://www.youtube.com/watch?v=tK_YqSbDpZ4&

Additional Print Parts: 
LCD: https://www.printables.com/model/189754-ender-5-rotatable-lcd-holder-with-lcd-cover/files


Things left to do.
***Wiring harness to be done (2meter)
1.) Fans:
HotEnd Fan
Fan1
Fan2
2.) 5V YSplit for Optical EndSwitch
3.) Change Thermistor end port connection to 2PIN JST
4.) BLTouch extender to 5Pin JST
5.) Endstop Switches from dupont to 2PIN JST
6.) Change XYZZ Motor Connectors from Dupont to 6pin JST
***Wiring
***Filament Holder
***Tuning
***PANELS?

Design/Find Models for:
Make PSU Cover with Switch and Plug Control
Make Mobo Mount
Make LCD Mount
Cable Chains
Removable Bed stops
Bed Cable Support


To add: Built in eibos filament dryer.

Sources: 
https://www.ifixit.com/Device/BLV_MGN_Cube by armysolo in discord
https://www.blvprojects.com/blv-mgn-cube-3d-printer

</pre>
