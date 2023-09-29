---
description: Xadow Tutorial - Acceleration Detector
title: Xadow Tutorial - Acceleration Detector
keywords:
- Seeed_Elderly
image: https://files.seeedstudio.com/wiki/wiki-platform/S-tempor.png
slug: /Xadow_Tutorial_Acceleration_Detector
last_update:
  date: 1/13/2023
  author: shuxu hu
---
We have made an acceleration detector, it detects the acceleration and reminds users by vibrating. When the acceleration changes, the Xadow Vibration will vibrate and the Oled will display the accelerometer value. You can also see the current battery voltage on the OLED display.

This demo required:

<!-- 
*   [Xadow Main Board](/Xadow_Main_Board/)

*   [Xadow OLED](/Xado_OLED_128multiply64)

*   [Xadow Vibrator Motor](https://wiki.seeedstudio.com/Xadow_Vibrator_Motor/)

*   [Xadow Accelerometer](/Xadow_3_Aixs_Accelerometer/) -->


![](https://files.seeedstudio.com/wiki/Xadow_Tutorial_Acceleration_Detector/img/Untitled2.jpg)

To complete the demo, you need to:

*   Connect Xadow Main Board,Xadow OLED, Xadow Vibrator and Xadow Accelerometer at the same direction with FFC cables.

<!-- *   Connect Xadow Main Board to PC with a Micro USB cable. Before uploading code, you need to install Xadow driver. Please click [here](/Xadow_Main_Board#Get_Start_with_Xadow_Main_Board) to learn the specific operation. -->

*   When you see "Now, you can program and use the Xadow as you use other Arduino boards", it means you have finished the preparations.

*   Downloading [the file: acceleDetector Library](https://files.seeedstudio.com/wiki/Xadow_Tutorial_Acceleration_Detector/res/AccelerationDetector.zip) and directly open acceleDetector INO file.

:::note
    Before compiling, you should make sure that there are [the library:OLED_Display12864](https://files.seeedstudio.com/wiki/Xadow_Tutorial_Acceleration_Detector/res/OLED_Display12864.zip) and [sleep_FromArduino](https://files.seeedstudio.com/wiki/Xadow_Tutorial_Acceleration_Detector/res/Sleep_FromArduino.zip) in Arduino Library. If not, please download them and put them on the libraries file of Arduino IDE in the path: ..\arduino-1.0.1\libraries after unzip._
:::
*   Compile code and upload it to xadow board. You need to select Seeed Xadow from the Tools | Board menu of the Arduino environment.
*   Then you can see the following picture:

![](https://files.seeedstudio.com/wiki/Xadow_Tutorial_Acceleration_Detector/img/Demo_1_effect_picture.jpg)

Change the acceleration value by shaking the sensor,you will see the sensor value on the OLED module

##  Resources

[Demo1 acceleDetectoe Code](https://files.seeedstudio.com/wiki/Xadow_Tutorial_Acceleration_Detector/res/AccelerationDetector.zip)

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
