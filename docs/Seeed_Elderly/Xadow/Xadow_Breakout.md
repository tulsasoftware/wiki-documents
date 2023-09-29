---
description: Xadow - Breakout
title: Xadow - Breakout
keywords:
- Seeed_Elderly
image: https://files.seeedstudio.com/wiki/wiki-platform/S-tempor.png
slug: /Xadow_Breakout
last_update:
  date: 1/13/2023
  author: shuxu hu
---
![](https://files.seeedstudio.com/wiki/Xadow_Breakout/img/Xadow_Breakout_01.jpg)

Perhaps you want to connect various modules to Xadow. For example, an IR sensor which can detect whether someone is near by. You can connect the sensor to this Breakout Module.

[![](https://files.seeedstudio.com/wiki/Seeed-WiKi/docs/images/300px-Get_One_Now_Banner-ragular.png)](https://www.seeedstudio.com/Xadow-Breakout-p-1519.html)

## Specification
---
- A adapter
- Compatible with all Grove Module in hardware
- Dimensions: 25.43mm x 20.35mm

## Demonstration
---
Below is the Demo to control a buzzer. You need to connect Grove - Buzzer to Xadow Breakout with a Grove cable and connect Xadow Breakout to Xadow Main Board with a FFC cable.

![](https://files.seeedstudio.com/wiki/Xadow_Breakout/img/XadowBreakoutUsage.jpg)

Xadow breakout not only can control some modules which are IIC communication or Serial communication, but also can control other modules because the two Grove connectors can be used as Digital port or Analog port. In other words, it can control all Grove modules.

The demo code like this:
```
Void setup()
{
    DDRD |=0x04;
}
void loop()
{
    PORTD |=0x04;
    delay(500);
    PORTD &=~(0x04);
    delay(500);
}
```
Now you can hear the buzzer "Bi Bi Bi". You can replace it with Grove - LED and see the LED on/off.


## Schematic Online Viewer
<div className="altium-ecad-viewer" data-project-src="https://files.seeedstudio.com/wiki/Xadow_Breakout/res/Xadow%20-%20Breakout_eagle%20file.rar" style={{borderRadius: '0px 0px 4px 4px', height: 500, borderStyle: 'solid', borderWidth: 1, borderColor: 'rgb(241, 241, 241)', overflow: 'hidden', maxWidth: 1280, maxHeight: 700, boxSizing: 'border-box'}}>
</div>



## Resources
---
- [Xadow Breakout Eagle File](https://files.seeedstudio.com/wiki/Xadow_Breakout/res/Xadow%20-%20Breakout_eagle%20file.rar)

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
