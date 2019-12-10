# TSL2561 - Build Instructions 
# Table of Contents 

[Introduction](https://github.com/simransaini1999/Lumi-Monitor#Introduction)

[Schedule](https://github.com/simransaini1999/Lumi-Monitor#Schedule)

[Budget](https://github.com/simransaini1999/Lumi-Monitor#Budget)

[PCB and Soldering](https://github.com/simransaini1999/Lumi-Monitor#PCB-and-Soldering)

[Assembly](https://github.com/simransaini1999/Lumi-Monitor#Assembly)

[Power Up](https://github.com/simransaini1999/Lumi-Monitor#Power-Up)

[Testing](https://github.com/simransaini1999/Lumi-Monitor#Testing)



# Introduction
![](Images/Casing/IMG-0004.jpg)
Welcome to the build instructions of the TSL2561 Lumnosity sensor. In these instructions we will be using a broadcom development platform aka Raspberry Pi and will need a case  at the end to put all the components in.
# System Diagram
![](Images/UML.JPG)
# Time commitment
Estimated time to finish this project if this build instruction is followed: 
- Setting up the raspberry pi with OS: 45min - 1hr considering the download speed on your WIFI
- testing sensor with breadboard: 20 minutes  
- PCB designing:30 minutes 
Send out the [PCB](Electronics/Fritzing/printing_PCB.fzz) file to get the PCB made from the [Company](http://support.seeedstudio.com/). 
- Laser cutting the case: 20 minutes
For laser printing you can send out the [Corel Draw File](Mechanical/FINAL1999.cdr) to a company and get it made. 
- PCB power up: 10 minutes
- Assebling the case with raspberry pi in it: 10 - 15 minutes
This project should be able to be finished over the weekend considering that you have all the materials ready to connect. 
# Budget
![](Images/Budget.JPG)
Below here are the links to the materials that will be needed for the project. 

[TSL2561 Luminosity Sensor](https://bit.ly/2l9bKFb)

[Raspberry Pi 3](https://amzn.to/2CayCcg)

[USB to Ethernet Cable](https://amzn.to/2KhWU8z)

[Ethernet cable](https://amzn.to/2qSPrWv)

[Keyboard ](https://amzn.to/3565wHF)

[Clear Acrylic](https://amzn.to/2LEbLLd)

[Sockets](https://amzn.to/2RwjQFD)
# PCB and Soldering 
### PCB Design 
The design for this PCB can be found [here](Electronics/Fritzing/printing_PCB.fzz)
![](Images/printing_PCB_pcb.png)
### PCB final Look
This is how your PCB and sensor suppose to look like after it is soldered and ready to mount on the raspberry pi.
![](Images/IMG-0112.jpg)

# Assembly 
### Set up Raspberry Pi
[How to install the OS on SD card](https://www.youtube.com/watch?v=jsi50bCo_W4)
If the video above is not availible, here is a few of the important steps talked about in the video.
1. Download the full desktop verion of [rasbian](https://www.raspberrypi.org/downloads/raspbian/)
2. Downlad the [SD card formater](https://www.sdcard.org/downloads/formatter/)
3. insert SD card into computer
4. After running the SD card formater upload the rasbian download you downloaded on the SD card formater and click format. 
### Set up Sensor on breadboard
This is how the connection from your sensor is suppose to be with the raspberry pi.
![](Images/Fritzing/with_raspberrypi_bb.jpg)
To reffer to the pinout of the rapberry pi you can check the [pinout.xyz](https://pinout.xyz/)
### Casing for the project 
The casing desing is made on corel draw. The file for the casing can be found [here](Mechanical/FINAL1999.cdr).

The case for this project will look with the all the componets in it is:

![](Images/Casing/IMG-0004.jpg)

# Power Up
Once everything is connected, power up the raspberry pi.
1. check your I2C bus adress by typing in terminal ```python i2cdetect -y 1```
2. This is how the output is suppose to look like: 

![](Images/I2CBus.png)
## Setting up the sensor on your Raspberry pi
To set up the TSL2561 Sensor with your raspberry pi, [this](https://learn.adafruit.com/tsl2561/python-circuitpython) page will explain a step by step proccess on how to set it up with your raspberry pi. 
# Testing 
To run this file you will have to save the code file on your raspberry pi. For example saving it on desktop. 
Open terminal
```
cd Desktop // this is the location where your file is saved 
python3 'filename'.py
```
After testing the output with more light will have a big lux value  
![](Images/sensor_light.jpg)
The output with less light will have a less lux value 
![](Images/sensor_covered.jpg)




