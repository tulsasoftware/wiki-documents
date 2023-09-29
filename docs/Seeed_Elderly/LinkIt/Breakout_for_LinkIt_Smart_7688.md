---
description: Breakout for LinkIt Smart 7688
title:  Breakout for LinkIt Smart 7688
keywords:
- Seeed_Elderly
image: https://files.seeedstudio.com/wiki/wiki-platform/S-tempor.png
slug: /Breakout_for_LinkIt_Smart_7688
last_update:
  date: 1/13/2023
  author: shuxu hu
---

![](https://files.seeedstudio.com/wiki/Breakout_for_LinkIt_Smart_7688/img/Breakout_for_LinkIt_Smart_7688_product_view_1200.jpg)

:::dangernote
Due to the closure of MediaTek Labs, all related links have become invalid. If you need to download relevant files, please search for them on the following link: [https://github.com/MediaTek-Labs](https://github.com/MediaTek-Labs).
:::

**Breakout for LinkIt Smart 7688** is a Grove port integrated expansion board for LinkItTM Smart 7688 development board. This breakout board will save a lot of work and makes prototyping easier through simplified wiring. It will assist a beginner to get started fast. It supports serial buses like  I2C, UART. It comes with USB, Ethernet and 3.5mm Audio ports.

[![](https://files.seeedstudio.com/wiki/Seeed-WiKi/docs/images/300px-Get_One_Now_Banner-ragular.png)](https://www.seeedstudio.com/Breakout-for-LinkIt-Smart-7688-p-2590.html)

##  Features
---
*   Grove interface makes wiring easier and allows expansions with Grove modules.

*   USB host

*   Audio Output

*   Ethernet port

*   Cost-effective.

##  Application ideas
---
*   IoT/Gateway Device.

*   Robotics

*   Smart multimedia devices

*   Teaching and learning

##  Specification
---
<table>
<tr>
<td> Input voltage </td>
<td> 5.0V(With USB Power port)
</td></tr>
<tr>
<td> Operating voltage </td>
<td> 3.3V
</td></tr>
<tr>
<td colspan="2"> Debug pins, Ethernet pins and USB type-A host pins conect with MT7688, Ohter pins connect with ATmega32U4.
</td></tr></table>

##  Hardware Overview
---
![](https://files.seeedstudio.com/wiki/Breakout_for_LinkIt_Smart_7688/img/Breakout_for_LinkIt_Smart_7688_components_1200_s.jpg)

**Grove interface**

<!-- Connect rich [Grove](/Grove_System) interfaced functional modules. With this kind of ports, you never need jumper wire or soldering work, and you can make more powerful applications with those functional modules. -->

:::note
    **Note** that we will add the function of audio recording for this board in next version of this product.
:::

This section will show those senior customers how to add recording funtion to this board.

1.Download the schematic file at bottom of this page. Open the file named **Breakout for LinkIt Smart7688 v1.0 brd.pdf**, and find the section **MIC Input**. Remove following components inductor L6 and capacitor C21. This will added recording function to this board. **Note** this way only works as you use LinkIt Smart 7688 firmware version 0.9.3 and above.


![](https://files.seeedstudio.com/wiki/Breakout_for_LinkIt_Smart_7688/img/To_use_recording_function_on_version_1.0.png)



2.For beginner, we recommend that you buy Breakout for LinkIt Smart 7688 v2.0 at [bazaar](https://www.seeedstudio.com/depot/Breakout-for-LinkIt-Smart-7688-v20-p-2641.html?cPath=122_142).


###  **Parts list**

<table>
<tr>
<th>Parts name   </th>
<th> Quantity
</th></tr>
<tr>
<td> Breakout for LinkIt Smart 7688 </td>
<td> 1PCS
</td></tr></table>

##  Get started

###  Material required

*   LinkIt Smart 7688 × 1

*   USB cable(type A to micro type-B) × 2

*   USB to Serial adapter × 1

*   Jumper wires × 3

*   Stereo(with 3.5 mm audio cable) × 1

*   USB flash driver(with audio file of MP3 format inside) × 1

###  Play music

<!-- 1.Refer [here](/LinkIt_Smart_7688#Getting_Started) to connect your LinkIt Smart 7688 to internet.
 -->

:::note
    - You can plug jumper wires to MT7688 UART2 port instead soldering them to Pin 8, Pin 9 and Pin GND.
    - In rare cases, you might not connect to internet successfully, reboot the embedded OS.
:::
2.Open a console with USB to Serial  adapter.

3.Connect all parts like follows:


![](https://files.seeedstudio.com/wiki/Breakout_for_LinkIt_Smart_7688/img/Breakout_for_LinkIt_Smart_7688_demo_connection_1200.jpg)

4.Enter folder of USB by type **cd /Media/USB-A1** in console.

5.Play music with utility **Madplay**(installed on OpenWRT) by typing **madplay filename.mp3** into console.

6.Now you will hear the music.



## Schematic Online Viewer

<div className="altium-ecad-viewer" data-project-src="https://files.seeedstudio.com/wiki/Breakout_for_LinkIt_Smart_7688/res/Breakout_for_LinkIt_Smart_7688_v2.0_schematic_files.zip" style={{borderRadius: '0px 0px 4px 4px', height: 500, borderStyle: 'solid', borderWidth: 1, borderColor: 'rgb(241, 241, 241)', overflow: 'hidden', maxWidth: 1280, maxHeight: 700, boxSizing: 'border-box'}}>
</div>



##  Resources

*   [Schematic files](https://files.seeedstudio.com/wiki/Breakout_for_LinkIt_Smart_7688/res/Breakout_for_LinkIt_Smart_7688_v2.0_schematic_files.zip)

<!-- *   [LinkIt smart 7688](/LinkIt_Smart_7688) -->

*   [OpenWrt](http://wiki.openwrt.org/doc/howto/user.beginner)

*   [Link](https://www.seeedstudio.com/depot/LinkIt-Smart-7688-p-2573.html?cPath=122_142) to buy a LinkIt Smart 7688.

## Tech Support & Product Discussion

Thank you for choosing our products! We are here to provide you with different support to ensure that your experience with our products is as smooth as possible. We offer several communication channels to cater to different preferences and needs.

<div class="button_tech_support_container">
<a href="https://forum.seeedstudio.com/" class="button_forum"></a> 
<a href="https://www.seeedstudio.com/contacts" class="button_email"></a>
</div>

<div class="button_tech_support_container">
<a href="https://discord.gg/eWkprNDMU7" class="button_discord"></a> 
<a href="https://github.com/Seeed-Studio/wiki-documents/discussions/69" class="button_discussion"></a>
</div>
