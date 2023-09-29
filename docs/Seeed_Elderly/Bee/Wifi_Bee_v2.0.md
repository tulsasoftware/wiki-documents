---
description: Wifi Bee v2.0
title: Wifi Bee v2.0
keywords:
- Seeed_Elderly
image: https://files.seeedstudio.com/wiki/wiki-platform/S-tempor.png
slug: /Wifi_Bee_v2.0
last_update:
  date: 1/13/2023
  author: shuxu hu
---
![](https://files.seeedstudio.com/wiki/Wifi_Bee_v2.0/img/Wifi_bee_v2_01.jpg)

Wifi Bee v2.0 is the update version of Wifi Bee v1.0. We replace transceiver module MRF24WB0MA which is SPI interface with RN-171 used UART interface. Wifi Bee v2.0 module incorporates 802.11 b/g radio, 32 bit processor, TCP/IP stack, real-time clock, crypto accelerator, power management unit and analog sensor interface. It can directly plug into the Bee sockets and use the UART port for communication. You can also use AT command for advanced configuration to meet your unique requirement.

[![](https://files.seeedstudio.com/wiki/Seeed-WiKi/docs/images/300px-Get_One_Now_Banner-ragular.png)](https://www.seeedstudio.com/Wifi-Bee-v2.0-p-1637.html)

##  Specification
---
*   Compatible with any Bee socket

*   Host interface： UART

*   Transmit power: 0dBm to 12dBm

*   Frequency：2402~2480 MHz

*   Channal：0~13

*   Integrated TCP / IP protocol stack

*   On-board Multilayer Chip Antenna

##  Demonstration
---
In this section, we will use Wifi Bee to create a Web server as an sample application. Let's follow the steps below to make it work!
Note: In order to configure this module, you will need an adapter or Xbee shield that lets you communicate with the module, before you can plug it and use on other modules.

###  Hardware Installation

Here's all the hardware needed.


*   1) Wifi Bee

*   2) An adaptor，such as [SBee](https://www.seeedstudio.com/depot/xbee-shield-v20-p-1375.html?cPath=98_16Uart),  [Grove -Xbee Carrier](https://www.seeedstudio.com/depot/grove-xbee-carrier-p-905.html?cPath=98_16)， [Xbee Shield](https://www.seeedstudio.com/depot/xbee-shield-v20-p-1375.html?cPath=98_16)

*   3) Mini USB cable


Plug wifi bee into the Bee Socket of your adaptor, and connect adaptor to your computer via Mini USB cable. Before wifi bee donot connect to your network, the ASSOC indicator is in flash state.

![](https://files.seeedstudio.com/wiki/Wifi_Bee_v2.0/img/Wifi_Beev2.0.jpg)

###  Configure Wifi Bee

We need a serial monitor for configuring the Wifi Bee. So before configuring Wifi bee, you need perpare a serial tool. In this case, we choose usual [SSCOM3.2](https://files.seeedstudio.com/wiki/Wifi_Bee_v2.0/res/Sscom32E.zip)

![](https://files.seeedstudio.com/wiki/Wifi_Bee_v2.0/img/Serial_Tool.png)

*   1) Choose the right serial port and click "Open Com" button，shown above, set the baud rate to 9600.

*   2) Donot select "SendNew", and send AT command $$$to the wifi Bee and it will reply "CMD" to indicate that it enter the configure mode properly.

*   3) Select "SendNew" after entering to configure mode，send AT command set u b 9600 to set the baud rate as 9600. Of cource，you can also set it as 38400.

*   4) Type show net   and it will show current network settings.

*   5) Type scan  to view a list of Wifi networks around.

![](https://files.seeedstudio.com/wiki/Wifi_Bee_v2.0/img/Serial_Tool_Scan_net.png)

*   6) Send AT command  set wlan join 1，if the serial port reply "ADK" which indicates Wifi Bee enters to Auto control mode.

*   7)Type join your router's SSID (like join Seeed-STU)to connect to associate with an open access point. If we join a a secure network type like this:

set wlan ssid your router's SSID

set wlan pass your router's password

save

reboot

And the monitor replies with current ip address and opened port. It can be easily figured out that the ip address of my Wifi Bee is 192.168.0.28 and the port is 2000.

![](https://files.seeedstudio.com/wiki/Wifi_Bee_v2.0/img/Join_network.png)

*   8) Use Web browser to access "http://ip:port", like:"http://192.168.0.28:2000", and the monitor receives the http request from the Web browser shown below. However, the Web browser will not receive anything due to the wifi bee replies nothing.

![](https://files.seeedstudio.com/wiki/Wifi_Bee_v2.0/img/Web_access.png)

For more command, please view the Wifly Command Reference of Resource part.

###  Connect the TCP server and Wifi Bee

Here we select [TCPUDPbg](https://files.seeedstudio.com/wiki/Wifi_Bee_v2.0/res/TCPUDPDbg.zip) to work as an TCP client and send commands to the Wifi Bee.

*   1） Download and run TCPUDPbg. Click "CreatConnection", we can see this picture：

![](https://files.seeedstudio.com/wiki/Wifi_Bee_v2.0/img/TCPUDPTool.png)

*   2）After selecting TCP Type, type IP address and port of Wifi Bee and click "Create".

*   3）Click"Connect" button in left sidebar，Now you could send commands via the TCP client simulated by TCPUDPbg to the wifi bee. Thus TCPUDPbg will receive the strings sent from the Serial monitor also！

![](https://files.seeedstudio.com/wiki/Wifi_Bee_v2.0/img/Communication.png)

##  Version Tracker
---
<table>
<tr>
<th>  Revision
</th>
<th> Descriptions
</th>
<th> Release
</th></tr>
<tr>
<td width="300px"> Wifi Bee v1.0
</td>
<td width="500px"> transceiver module MRF24WB0MA which is SPI interface, and using a Atmega328p
</td>
<td width="200px"> Dec 13, 2011
</td></tr>
<tr>
<td width="300px"> Wifi Bee v2.0
</td>
<td width="500px"> replace MRF24WB0MA with RN-171, cancel Atmega328p chip
</td>
<td width="200px"> Nov 11, 2013
</td></tr></table>


## Schematic Online Viewer

<div className="altium-ecad-viewer" data-project-src="https://files.seeedstudio.com/wiki/Wifi_Bee_v2.0/res/Wifi_Bee_v2.0_Eagle_File.zip" style={{borderRadius: '0px 0px 4px 4px', height: 500, borderStyle: 'solid', borderWidth: 1, borderColor: 'rgb(241, 241, 241)', overflow: 'hidden', maxWidth: 1280, maxHeight: 700, boxSizing: 'border-box'}}>
</div>


##  Resource
---
*   [Wifi Bee v2.0 Eagle File](https://files.seeedstudio.com/wiki/Wifi_Bee_v2.0/res/Wifi_Bee_v2.0_Eagle_File.zip)

*   [RN-171 Datasheet](https://files.seeedstudio.com/wiki/Wifi_Bee_v2.0/res/WiFly-RN-171.pdf)

*   [Wifi Command Reference](https://files.seeedstudio.com/wiki/Wifi_Bee_v2.0/res/WiFly-RN-UM.pdf)

*   [Antenna Datasheet](https://files.seeedstudio.com/wiki/Wifi_Bee_v2.0/res/Antenna_Datasheet.pdf)

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
