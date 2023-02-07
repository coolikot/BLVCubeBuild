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

Sources: 
https://www.ifixit.com/Device/BLV_MGN_Cube by armysolo in discord
https://www.blvprojects.com/blv-mgn-cube-3d-printer

</pre>
