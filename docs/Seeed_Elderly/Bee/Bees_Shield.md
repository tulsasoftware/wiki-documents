---
description: Bees Shield
title: Bees Shield
keywords:
- Seeed_Elderly
image: https://files.seeedstudio.com/wiki/wiki-platform/S-tempor.png
slug: /Bees_Shield
last_update:
  date: 1/13/2023
  author: shuxu hu
---

![enter image description here](https://files.seeedstudio.com/wiki/Bees_Shield/img/bees%20shield.jpg)

Bees_Shield will make interfacing multiple Bee-style (XBee, GPRS Bee, Bluetooth Bee and etc) easier than ever before. Aside from two Bee-style 20p 2.0 pitch sockets, it also has a large prototyping area, and a customizable software serial port for easier prototyping.

[![Get one now](https://files.seeedstudio.com/wiki/Seeed-WiKi/docs/images/get_one_now.png)](https://www.seeedstudio.com/Bees-Shield-p-672.html)

## Versions
---------------

| Revision | Descriptions  | Release        |
|----------|--------------|----------------|
| v2.12| Initial public release| June 08, 2010  |


## Features
-------------------
- Dual Bee type socket
- 3 indicator LED(ON/Sleep, RSSI, ASSOC) for each Xbee
- Full size with free drills
- Reset button for each Xbee
- Reset button for base board
- Provide maximal 500mA under 3.3V
- Full break out for each Bee
- Switchable of communication with FTDI-USB /Base board

## Hardware Overview

![](https://files.seeedstudio.com/wiki/Bees_Shield/img/Bees%20Shield%20Hardware.jpg)

## Platforms Supported
-------------------

## Getting Started
-------------------
### Work with Bee1

#### Connection
- Plug the Xbee module into the Bee 1 socket, setting the jumpers as below. We use Bee1 SoftwareSerial for communication.

| Arduino Pins   | Bee1 Pins     |
| :------------- | :-------------|
| Digital Pin7   | Bee1_TX       |
| Digital Pin8   | Bee1_RX       |

- Plug Bees Shield into Arduino.
- Connect Arduino to PC via a USB cable.

#### Software
- Copy and Upload the code to Ardunio.

```
#include <SoftwareSerial.h>
SoftwareSerial mySerial(7, 8);

void setup() {
  Serial.begin(9600);
  Serial.println("Goodnight moon!");

  // set the data rate for the SoftwareSerial port
  mySerial.begin(9600);
  mySerial.println("Hello, world?");
}

void loop() {
  // run over and over
  if (mySerial.available())
    Serial.write(mySerial.read());
  if (Serial.available())
    mySerial.write(Serial.read());
}

```
- When it's uploaded, open the serial to monitor.

### Work with Bee2

#### Connection
- Plug the RFbee module into the Bee 2 socket, toggle switch to USB side.

:::note
    Toggle switch to the Atmega's side if you are not uploading a sketch to the Bee2. It does NOT work if the arduino is using ATmega168 – we need at least ATmega328 to pass serial communication through.
:::
- Plug Bees Shield into Arduino.
- Connect Arduino to PC via a USB cable.

#### Software
- Please Copy and Upload the code to Ardunio to disable Uart0 port of Atmega IC first.

```
void setup() {
   DDRD=0x00;
}

void loop() {}

```

### Wireless Arduino programming with Bee2

#### Connection
- Solder the JP1 block on the board for wireless programming.
- Plug Bees Shield into Arduino.

#### Software
- Download [Xbee setting profile](https://files.seeedstudio.com/wiki/Bees_Shield/res/Xbee%20setting%20profiles.zip) to transmitter Xbee by using X-CTU.
- Let's use the wireless programming.

#### Expansion function

- First we have to solder two 8-pin female headers and two 6-pin female headers on the Bees shield.
- After the expansion we can insert small shield like music shield on the Bees shield and we can control it wirelessly.

![](https://files.seeedstudio.com/wiki/Bees_Shield/img/Bees-Shield-expan2.jpg)


## Schematic Online Viewer

<div className="altium-ecad-viewer" data-project-src="https://files.seeedstudio.com/wiki/Bees_Shield/res/Bees_Shield_V2.12_Eagle_files.zip" style={{borderRadius: '0px 0px 4px 4px', height: 500, borderStyle: 'solid', borderWidth: 1, borderColor: 'rgb(241, 241, 241)', overflow: 'hidden', maxWidth: 1280, maxHeight: 700, boxSizing: 'border-box'}}>
</div>



## Resources
-------------------
- **[Eagle]** [Bees_Shield Eagle File ](https://files.seeedstudio.com/wiki/Bees_Shield/res/Bees_Shield_V2.12_Eagle_files.zip)
- **[PDF]** [Bees_Shield schematics](https://files.seeedstudio.com/wiki/Bees_Shield/res/Bees_Shield%20Sch.pdf)
- **[PDF]** [Bees_Shield PCB](https://files.seeedstudio.com/wiki/Bees_Shield/res/Bees_Shield%20PCB.pdf)
- **[Tools]** [Xbee setting profiles](https://files.seeedstudio.com/wiki/Bees_Shield/res/Xbee%20setting%20profiles.zip)

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
