---
layout: post
title:  "PIR Motion Sensor"
description: PIR Motion Sensor
categories: Electronic
---


# What is PIR Motion Sensor and how it works?

As the name suggest, PIR Sensor allows you to sense motion, almost always used to detect whether a human has moved in or out of the sensors range. 
The term PIR is the short form of the Passive InfraRed. The term “passive” indicates that the sensor does not actively take part in the process, which means, it does not emit the referred IR signals itself, rather passively detects the infrared radiations coming from the human body in the surrounding area.

![]({{site.baseurl}}/images/Electronic/8/01.jpg)


These detected signals are converted into electrical signals then, fed to the output pin of the device which becomes applicable to an external circuit .The PIR sensor range is up to 10 meters at an angle of +150 or -150.


# How will you use this sensor?
Below is the connections rather pin connections of PIR Sensors.

![]({{site.baseurl}}/images/Electronic/8/02.jpg)

The Passive infrared sensors consist of three pins as indicated in the diagram shown above.
Pin1 corresponds to the drain terminal of the device, which should be connected to the positive supply 5V DC.
Pin2 corresponds to the source terminal of the device, which should be connected to the ground terminal via a 100K or 47K resistor. The Pin2 is the output pin of the sensor, and the detected IR signal is carried forward to an amplifier from the pin 2 of the sensor.
Pin3 of the sensor is connected to the ground.
 
 
#Pin Description

![]({{site.baseurl}}/images/Electronic/8/03.png)

Pin Diagram of PIR Sensor
Pin 1 – GND
We have to connect this pin to Ground.
Pin 2 – Output
This pin gives output (3.5V) when the motion is detected.
Pin 3 – VCC
This pin provides supply voltage(+5v) to PIR element and internal circuit.
 
# Changing Sensitivity and Delay time 
There are two potentiometers on PIR motion sensors board: Sensitivity Adjust and Time delay adjust.
It is possible to make PIR more sensitive or Non-Sensitive Enough. The maximum sensitivity can be achieved up to 6 meters.
Time Delay Adjust potentiometer is used to adjust the time set.
Clockwise Movement makes PIR more Sensitive.

# PIR Sensor Testing
## Let’s make a circuit to test our sensor. All you need is a breadboard, an LED, 9V battery, Jumpers and a PIR Sensor.

![]({{site.baseurl}}/images/Electronic/8/04.png)

Now whenever PIR detect motion, the LED will glow else it will remain OFF.
 
### Applications
Highly reliable Security Application, Industrial Application, Safety related application.
PIR Module to be integrated in LED fixtures, any electronics cards, educational electronics projects
 
# Let’s Make
## Shop from- http://technoventor.in/
 
## PIR Sensor Arduino Alarm
Things you will need:
Solderless breadboard
Arduino UNO
PIR Sensor
Piezo Buzzer
Jumper Wires
LED
 
 
 
### Step1: Gather your Parts
 
 ![]({{site.baseurl}}/images/Electronic/8/05.jpg)

 
### Step2: Wire the Arduino to the Breadboard
 
![]({{site.baseurl}}/images/Electronic/8/06.jpg) 

 
Step3: Connect your Motion Sensor
 
![]({{site.baseurl}}/imagesElectronic/8/07.png)
 
Step4: Plug in the LED
 
 ![]({{site.baseurl}}/images/Electronic/8/08.jpg)
  
Step5: Connect the buzzer
 
 ![]({{site.baseurl}}/images/Electronic/8/09.jpg)

Step6: Program the Arduino:
 
 ![]({{site.baseurl}}/images/Electronic/8/10.jpg)
 ![]({{site.baseurl}}/images/Electronic/8/11.jpg)
 
Step7: Test your Alarm
 
 ![]({{site.baseurl}}/images/Electronic/8/12.jpg)
 
 
 
  
# Below are the given examples on PIR Sensor. Enjoy making!!
https://www.electronicshub.org/automatic-room-lights-using-arduino-pir-sensor/
https://makezine.com/projects/pir-sensor-arduino-alarm/
 
Abbreviation

DC – Direct Current
GND – Ground 
O/P- Output
I/P- Input
LED- Light Emitting Diode
VCC-  Supply voltage for electronics circuit.
LCD- Liquid crystal display
IC- Integrated circuit
USB- Universal Serial Bus
