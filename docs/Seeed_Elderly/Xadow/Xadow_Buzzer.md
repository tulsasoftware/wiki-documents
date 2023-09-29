---
description: Xadow - Buzzer
title: Xadow - Buzzer
keywords:
- Seeed_Elderly
image: https://files.seeedstudio.com/wiki/wiki-platform/S-tempor.png
slug: /Xadow_Buzzer
last_update:
  date: 1/13/2023
  author: shuxu hu
---
![](https://files.seeedstudio.com/wiki/Xadow_Buzzer/img/Xadow_buzzer.jpg)

This is a Xadow module which can emit a tone. To drive it, you need to give control to two pins simultaneously: this is different from Grove - Buzzer which uses one pin to control. It is petite but loud! It can be used for making beeps, tones and alerts.

Xadow is a small but perfectly formed Arduino(TM) compatible board series containing several modules. It's a kit extremely suitable for space-sensitive projects such as wearable devices & arts designs, which have higher request on size, weight and flexible cascade connection. You can find more modules here.

[![](https://files.seeedstudio.com/wiki/Seeed-WiKi/docs/images/300px-Get_One_Now_Banner-ragular.png)](https://www.seeedstudio.com/Xadow-Buzzer-p-1599.html)

## Specification
---
- Work Voltage: 3.3V
- FundamentalFrequency: 2700Hz
- Sound Pressure Level: >75dB
- Dimensions: 25.43mm x 20.35mm

## Demonstration
---
There is an easy demo to show how to drive buzzer sound. If you have successfully used it, then you can apply it to your great projects, such as detecting the battery status: the buzzer will emit a sound when Xadow Main Board is in low battery.

![](https://files.seeedstudio.com/wiki/Xadow_Buzzer/img/Buzzer_Usage.jpg)

```
void setup()
{
    DDRB |= 0x06;
}

void loop()
{
    //turn on the buzzer
    PORTB |= 0x06;
    delay(1);
    //turn off the buzzer
    PORTB &= ~(0x06);
    delay(1);
}
```


## Schematic Online Viewer

<div className="altium-ecad-viewer" data-project-src="https://files.seeedstudio.com/wiki/Xadow_Buzzer/res/Xadow_Buzzer_eagle_file.zip" style={{borderRadius: '0px 0px 4px 4px', height: 500, borderStyle: 'solid', borderWidth: 1, borderColor: 'rgb(241, 241, 241)', overflow: 'hidden', maxWidth: 1280, maxHeight: 700, boxSizing: 'border-box'}}>
</div>


## Resource
---
- [Xadow Buzzer Eagle File](https://files.seeedstudio.com/wiki/Xadow_Buzzer/res/Xadow_Buzzer_eagle_file.zip)

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
