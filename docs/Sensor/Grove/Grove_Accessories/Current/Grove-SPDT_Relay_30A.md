---
description: Grove - SPDT Relay(30A)
title: Grove - SPDT Relay(30A)
keywords:
- Grove
image: https://files.seeedstudio.com/wiki/wiki-platform/S-tempor.png
slug: /Grove-SPDT_Relay_30A
last_update:
  date: 1/10/2023
  author: jianjing Huang
---

<div align="center"><img width={1000} src="https://files.seeedstudio.com/wiki/Grove-SPDT_Relay_30A/img/SPDT_Relay_01.jpg" /></div>

The SPDT Relay(30A) is a high quality Single Pole Double Throw Relay(SPDT).The Relay consists of a coil, 1 common terminal, 1 normally closed terminal, and one normally open terminal. When the coil of the relay is at rest (not energized), the common terminal and the normally closed terminal have continuity. When the coil is energized, the common terminal and the normally open terminal have continuity. This relay's coil is rated up to 5V and the contact is rated up to 30A (@250VAC, 30VDC).You can use it to control high current devices.

## Feature

---

- High Switching Current
- SPDT Relay
- Normally closed relay

:::tip
  More details about Grove modules please refer to [Grove System](https://wiki.seeedstudio.com/Grove_System/)
:::

## Specification

---
|Item| Min| Typical |Max |Unit|
|---|---|---|---|---|
|working Voltage| 4.75| 5.0| 5.25 |VDC|
|Current |-|185|-| mA|
|Pull-In Voltage(Max) |-|3.75|-| VDC|
|Operation Time(Max)|-| 15|-| ms|
|Release Time(Max)|-| 10|-| ms|
|Operating Ambient Temperature| -25| - |70 |°C|

## Usage

---
**With Arduino**

Why do we want to use a relay and do we really need to? Anytime you want to switch on/off a device which draws more current or works with a high voltage, you'll need to use a relay. That is to say, the relay is "a high voltage or current switch controlled by low voltage". The coil of an SPDT relay that we most commonly use draws very little current (the [Grove - Relay](https://wiki.seeedstudio.com/Grove-Relay/)supports 10A). Now, with this 30A relay, you can control much more high-current switch devices such as headlights, parking lights, horns, etc.

The SPDT Relay internal structure:

<div align="center"><img width={1000} src="https://files.seeedstudio.com/wiki/Grove-SPDT_Relay_30A/img/Relay_Struction.jpg" /></div>

You may see that the common terminal and the normally closed terminal have continuity When the coil of the relay is at rest.

But when the coil is energized, the common terminal and the normally open terminal will have continuity.

Hardware Installation can refer to the following picture:

<div align="center"><img width={1000} src="https://files.seeedstudio.com/wiki/Grove-SPDT_Relay_30A/img/SPDT_Relay.jpg" /></div>

The coding to control this relay is the same as the [Grove - Relay](https://wiki.seeedstudio.com/Grove-Relay/)

Good luck to you for controlling your air-condition or washing machine, with Arduino and the Grove - SPDT Relay(30A).

**With Raspberry Pi**

1.You should have got a raspberry pi and a grovepi or grovepi+.

2.You should have completed configuring the development enviroment, otherwise follow [here](https://wiki.seeedstudio.com/GrovePi_Plus#Introducing_the_GrovePi.2B).

3.Connection

- Plug the sensor to grovepi socket D4 by using a grove cable.

4.Navigate to the demos' directory:

```
   cd yourpath/GrovePi/Software/Python/
```

To see the code

```
   nano grove_spdt_relay.py   # "Ctrl+x" to exit #
```

```
import time
import grovepi

# Connect the Grove SPDT Relay to digital port D4
# SIG,NC,VCC,GND
relay = 4

grovepi.pinMode(relay,"OUTPUT")

while True:
    try:
        # switch on for 5 seconds
        grovepi.digitalWrite(relay,1)
        print "on"
        time.sleep(5)

        # switch off for 5 seconds
        grovepi.digitalWrite(relay,0)
        print "off"
        time.sleep(5)

    except KeyboardInterrupt:
        grovepi.digitalWrite(relay,0)
        break
    except IOError:
        print "Error"
```

5.Run the demo.

```
   sudo python grove_spdt_relay.py
```

## Schematic Online Viewer

<div className="altium-ecad-viewer" data-project-src="https://files.seeedstudio.com/wiki/Grove-SPDT_Relay_30A/res/Grove_-_SPDT_Relay(30A)_Eagle_File.zip" style={{borderRadius: '0px 0px 4px 4px', height: 500, borderStyle: 'solid', borderWidth: 1, borderColor: 'rgb(241, 241, 241)', overflow: 'hidden', maxWidth: 1280, maxHeight: 700, boxSizing: 'border-box'}}>
</div>

## Resource

---

- [Grove - SPDT Relay(30A) Eagle File](https://files.seeedstudio.com/wiki/Grove-SPDT_Relay_30A/res/Grove_-_SPDT_Relay(30A)_Eagle_File.zip)
- [SLA-05VDC-SL-C Datasheet](https://files.seeedstudio.com/wiki/Grove-SPDT_Relay_30A/res/SLA-05VDC-SL-C_Datasheet.pdf)

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

