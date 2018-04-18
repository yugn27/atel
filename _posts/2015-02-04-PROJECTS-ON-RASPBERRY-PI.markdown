---
layout: post
title:  "PROJECTS ON RASPBERRY PI"
description:  PROJECTS ON RASPBERRY PI
categories: project
---


# WEB CONTROLLED HOME AUTOMATION USING RASPBERRY PI
### COMPONENTS REQUIRED
Raspberry Pi 3 (Any other Version will be nice)
Memory card 8 or 16GB running Raspbian Jessie
5v Relays
2n222 transistors
Diodes
Jumper Wires
Connection Blocks
LEDs to test.
AC lamp to Test
Breadboard and jumper cables
220 or 100 ohms resistor
### SOFTWARE REQUIRED
Asides the Raspbian Jessie operating system running on the raspberry pi, we will also be using the WebIOPi frame work, notepad++ running on your PC and filezila to copy files from the PC to the raspberry pi, especially the web app files.
Also you dont need to code in Python for this Home Automation Project, WebIOPi will do all the work.
PREPARING THE RASPBERRY PI
Its an habit of some sort for me and i think it’s a good one, the first thing I do each time i want to use the Raspberry Pi is to update the PI. For this project, this section will comprise of the Pi updating procedures and installing the WebIOPi framework which will help us handle communication from the webpage to the raspberry pi. I Should probably state that this can also be done in an arguably easier way using the python Flask frame work but one of the interesting thing about DIY is when you take a look under the hood and make the difficult work. Thats where all the joy of DIY comes.
 
### To update the raspberry Pi below commands and then reboot the RPi;
sudo apt-get update
sudo apt-get upgrade
sudo reboot

![]({{site.baseurl}}/images/Project/RPI/01.png)
 
### With this done, the next thing is for us to install the webIOPi framework.
Make sure you are in home directory using;
cd ~
 
### Use wget to get the file from their sourceforge page;
wget http://sourceforge.net/projects/webiopi/files/WebIOPi-0.7.1.tar.gz
 
### When download is done, extract the file and go into the directory;
tar xvzf WebIOPi-0.7.1.tar.gz
cd WebIOPi-0.7.1/
 
### At this point before running the setup, we need to install a patch as this version of the WebIOPidoes not work with the raspberry pi 3 which I am using and I couldn’t find a version of the WebIOPi that works expressly with the Pi 3.
#### Below commands are used to install patch while still in the WebIOPi directory, run;
wget https://raw.githubusercontent.com/doublebind/raspi/master/webiopi-pi2bplus.patch
patch -p1 -i webiopi-pi2bplus.patch
 
### Then we can run the setup installation for the WebIOPi using;
sudo ./setup.sh

### Keep saying yes if asked to install any dependencies during setup installation. When done, reboot your pi;
sudo reboot


While I couldn’t lay my hands on relay modules, which I feel are easier to work with for hobbyists. So I am drawing here the schematics for ordinary standalone single 5v relays.
Connect your circuit as shown in the fritzing circuit above. You should note that COM, NO (normally open) and NC (normally Close) of your own relay may be located at different sides/points. Kindly use a millimeter to test it out. Learn more about relay here.
With our components connected, fire up your server, from a webpage, go to the IP of your Raspberry Pi and indicate the port as described earlier, login with your username and password, and you should see a webpage that looks exactly like the image below.
Now you can easily control four AC Home appliaces from anywhere wirelessly,  just by clicking on the buttons. This will work from Mobilephone, tablet etc. and you can add more buttons and relays to control more devices

![]({{site.baseurl}}/images/Project/RPI/02.png)






# LINE FOLLOWER ROBOT USING RASPBERRY PI

### COMPONENTS REQUIRED
Raspberry Pi 3 (any model should work)
IR Sensor (2Nos)
DC Gear Motor (2Nos)
L293D Motor Driver
Chaises (You can also build your own using cardboards)
Power bank (Any available power source)
 
![]({{site.baseurl}}/images/Project/RPI/03.png)

These two IR sensors will be placed one on either side of the line. 


![]({{site.baseurl}}/images/Project/RPI/04.png)



If left sensor comes on black line then the PI instructs the robot to turn left by rotating the right wheel alone.

![]({{site.baseurl}}/images/Project/RPI/05.png)

If right sensor comes on black line then the PI instructs the robot to turn right by rotating the left wheel alone.

![]({{site.baseurl}}/images/Project/RPI/06.png)



If both sensors comes on black line, robot stops.

![]({{site.baseurl}}/images/Project/RPI/07.png)

This way the Robot will be able to follow the line without getting outside the track. Now let us see how the circuit and Code looks like.
 
### CODE:

import RPi.GPIO as IO
import time
IO.setwarnings(False)
IO.setmode(IO.BCM)
IO.setup(2,IO.IN) #GPIO 2 -> Left IR out
IO.setup(3,IO.IN) #GPIO 3 -> Right IR out
IO.setup(4,IO.OUT) #GPIO 4 -> Motor 1 terminal A
IO.setup(14,IO.OUT) #GPIO 14 -> Motor 1 terminal B
IO.setup(17,IO.OUT) #GPIO 17 -> Motor Left terminal A
IO.setup(18,IO.OUT) #GPIO 18 -> Motor Left terminal B
while 1:
 
    if(IO.input(2)==True and IO.input(3)==True): #both while move forward     
        IO.output(4,True) #1A+
        IO.output(14,False) #1B-
        IO.output(17,True) #2A+
        IO.output(18,False) #2B-
    elif(IO.input(2)==False and IO.input(3)==True): #turn right  
        IO.output(4,True) #1A+
        IO.output(14,True) #1B-
        IO.output(17,True) #2A+
        IO.output(18,False) #2B-
    elif(IO.input(2)==True and IO.input(3)==False): #turn left
        IO.output(4,True) #1A+
        IO.output(14,False) #1B-
        IO.output(17,True) #2A+
        IO.output(18,True) #2B-
    else:  #stay still
        IO.output(4,True) #1A+
        IO.output(14,True) #1B-
        IO.output(17,True) #2A+
        IO.output(18,True) #2B-
        
        


![]({{site.baseurl}}/images/Project/RPI/08.png)



https://circuitdigest.com/microcontroller-projects/raspberry-pi-motion-detector-pir-sensor
https://circuitdigest.com/microcontroller-projects/raspberry-pi-obstacle-avoiding-robot
https://circuitdigest.com/microcontroller-projects/raspberry-pi-digital-lock

