---
title: 433Mhz RF Link Kit
nointro:
keywords:
  - docs
  - docusaurus
image: https://wiki.seeedstudio.com/433Mhz_RF_Link_Kit/
slug: /433Mhz_RF_Link_Kit
last_update:
  date: 02/03/2022
  author: gunengyu
---

![](https://files.seeedstudio.com/wiki/433Mhz_RF_Link_Kit/img/113990010%201.jpg)

The kit is consisted of transmitter and receiver, popular used for remote control.

[![](https://files.seeedstudio.com/wiki/Seeed-WiKi/docs/images/300px-Get_One_Now_Banner-ragular.png)](https://www.seeedstudio.com/depot/433mhz-rf-link-kit-p-127.html?cPath=139_140)

## Specification
---
- Frequency: 433Mhz.
- Modulation: ASK
- Receiver Data Output: High - 1/2 Vcc, Low - 0.7v
- Transmitter Input Voltage: 3-12V (high voltage = more transmitting power)
- Receiver Input Voltage : 3.3-6V (high voltage = more receiving power)

## Usage
---
The popular link is like this: MCU -> Encoder -> Transmitter ------ Receiver -> Decoder -> MCU

PT2262(Encoder) and PT2272(Decoder) are optional, their existence is to 1)avoid confusing when multiple RF links in range 2) isolate disturbance. You can integrate the encoding and decoding work to the MCUs on both side. Whenever there is no 315Mhz devices around, you may use it as direct cable connection.

Excuse for the documentation, we will work on them. Before that, please consult us for any details, we are happy to find the answer for you ^^ We tried them using the guide from Sparkfun, it's compatible. The only difference is in package, of some excess GND pins.

More over, we will make more RF modules ourselves with different frequency and capacity. The next one in plan is based on cc1100 Please suggest us about your need :)

## Support

If you have questions or other better design ideas, you can go to our [forum](https://community.seeedstudio.com/) discuss.

## Resources

- [Demo Scheme](https://files.seeedstudio.com/wiki/433Mhz_RF_Link_Kit/res/315MRFlink.pdf)
- [VirtualWire 1.3](https://files.seeedstudio.com/wiki/433Mhz_RF_Link_Kit/res/VirtualWire.rar)
- [Documentation For 1.3](https://files.seeedstudio.com/wiki/433Mhz_RF_Link_Kit/res/VirtualWire.pdf)
- [example from sparkfun](https://files.seeedstudio.com/wiki/433Mhz_RF_Link_Kit/res/KLP_Walkthrough.pdf)
- [example running rf modules](http://winavr.scienceprog.com/example-avr-projects/running-tx433-and-rx433-rf-modules-with-avr-microcontrollers.html)


## Licensing

This documentation is licensed under the Creative Commons [Attribution-ShareAlike License 3.0](https://creativecommons.org/licenses/by-sa/3.0/) Source code and libraries are licensed under [GPL/LGPL](http://www.gnu.org/licenses/gpl.html), see source code files for details.
External Links

Links to external webpages which provide more application ideas, documents/datasheet or software libraries
- [RCSwitch - Arduino Library to control 433Mhz remote power sockets](http://code.google.com/p/rc-switch)

## Tech Support & Product Discussion
 if you have any technical issue.  submit the issue into our [forum](http://forum.seeedstudio.com/). 
Thank you for choosing our products! We are here to provide you with different support to ensure that your experience with our products is as smooth as possible. We offer several communication channels to cater to different preferences and needs.

<div class="button_tech_support_container">
<a href="https://forum.seeedstudio.com/" class="button_forum"></a> 
<a href="https://www.seeedstudio.com/contacts" class="button_email"></a>
</div>

<div class="button_tech_support_container">
<a href="https://discord.gg/eWkprNDMU7" class="button_discord"></a> 
<a href="https://github.com/Seeed-Studio/wiki-documents/discussions/69" class="button_discussion"></a>
</div>