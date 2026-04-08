# Software Configuration Guide

This guide covers flashing the GRBL firmware to the Arduino Uno and configuring the control software.

## 1. Arduino IDE Setup
To communicate with the hardware, you need the Arduino environment.
* **Download:** Install [Arduino IDE v2.x](https://www.arduino.cc/en/software).
* **Library Import:** 1. Download the [GRBL 1.1 ZIP](https://github.com/gnea/grbl/archive/master.zip).
    2. In Arduino IDE, go to **Sketch** > **Include Library** > **Add .ZIP Library**.
    3. Select the `grbl-master.zip` file.

## 2. Flashing the Firmware
"Flashing" is the process of uploading the machine's "operating system" (GRBL) to the Arduino brain.
1. Connect your Arduino Uno to your PC via USB.
2. In the IDE, go to **File** > **Examples** > **grbl** > **grblUpload**.
3. Select your Board (**Arduino Uno**) and the correct **Port**.
4. Click the **Upload** arrow button. 
5. Wait for the "Done uploading" message.

## 3. G-Code Sender Installation
The Arduino IDE flashes the brain, but you need a "controller" interface to move the motors.
* **Recommendation:** Download [Universal Gcode Sender (UGS)](https://winder.github.io/ugs_website/).
* **Connection:** Open UGS, set the Baud rate to **115200**, and click **Connect**.
