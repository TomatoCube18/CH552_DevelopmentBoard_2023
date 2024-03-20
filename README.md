# CH552_DevelopmentBoard_2023
![alt text](https://github.com/TomatoCube18/CH552_DevelopmentBoard_2023/blob/main/images/Front_Back.png)
## Description
This CH552 USB Dongle Development board is designed to support our short, engaging, and cost-effective STEAM-related activity/workshop offered during the Penang International Science Fair. 

With an extremely tight budget, we had to explore alternative low-cost MCU options that still provided ample learning potential and aligned with the STEM curriculum suggested for the local STEM curriculum. 

The result is a low-cost development board that is Arduino compatible (C Language only). It allows participants to experience and explore the various topics in embedded software development using onboard sensors through a series of guided exercises.

## Features Overview
![alt text](https://github.com/TomatoCube18/CH552_DevelopmentBoard_2023/blob/main/images/FeaturesOverview.png)

## Installation

Automatic IDE integration is supported via the
Arduino Boards Manager. This is the recommanded way of installation now. 

Start the Arduino-IDE. In *File->Preferences*, *Settings* tab, enter

> https://raw.githubusercontent.com/TomatoCube18/ch55xduino/ch55xduino/package_tc_ch55xduino_mcs51_index.json

as an *Additional Boards Manager URL*.

* Open *Tools->Board:...->Boards Manager*
* Find Ch55xduino by typing 'tomato' into the search line
* Click on the list entry
* Click on *Install*.

Now you should find a new entry *CH55x Boards* in the list at
*Tools->Board:...*

* Choose *CH552 Board* from the list
* open the standard Blink example from *File->Examples->01. Basics->Blink*
* Change pin number in Blink example. For example, if you have LED on P3_0, you will write pin 30.
* compile it by hitting *Verify*
* If your board is never used with ch55xduino before, you need to make the ch55x chip enter bootloader mode. You need to disconnect USB and unpower ch55x, connect the pull-up resistor on D+ line (generally a 10K resistor between D+ and 5V, controlled by a push-button or adjacent pads). Then you connect USB. and hit *Upload*. Also, a blank new chip will enter the bootloader automatically.
* If you have used ch55xduino once and your code doesn't crash the USB subsystem, you can simply press *Upload*. Arduino and the firmware will kick the chip into the bootloader automatically.

