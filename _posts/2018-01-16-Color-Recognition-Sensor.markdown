---
layout: post
title:  "Color Recognition Sensorr"
description: Color Recognition Sensor
categories: Electronic
---
 



### What is Color Recognition Sensor?
The TCS3200 color sensor can detect a wide variety of colors based on their wavelength. This sensor is specially useful for color recognition projects such as color matching, color sorting, test strip reading and much more.

![]({{site.baseurl}}/images/Electronic/chap16/01.jpg)

### How does it work?
The light sensor works by shining a white light at an object and then recording the reflected color. It can also record the intensity of the reflection (brightness). Through red, green and blue color filters the photodiode converts the amount of light to current. The converter then converts the current to voltage which our arduino can read.

Pinout

![]({{site.baseurl}}/images/Electronic/chp16/02.jpg)

![]({{site.baseurl}}/images/Electronic/chp16/03.jpg)

 
Here’s the sensor pinout:                		

Pin Name
I/O
Description
GND (4)


Power supply ground
OE (3)
I
Enable for output frequency (active low)
OUT (6)
O
Output frequency 
S0, S1（1，2）
I
Output frequency scaling selection inputs
S2, S3（7，8）
I
Photodiode type selection inputs
VDD（5）


Voltage supply




### How TCS230 color Sensor works?
The TCS230 senses color light with the help of an 8 x 8 array of photodiodes. Then using a Current-to-Frequency Converter the readings from the photodiodes are converted into a square wave with a frequency directly proportional to the light intensity. Finally, using the Arduino Board we can read the square wave output and get the results for the color.
 
![]({{site.baseurl}}/images/Electronic/chp16/04.png)

### Applications
It is used for many purposes like in sorting out raw coffee beans of different shades, in sorting out a different color of candies, in the identification of easily verifying shades of color, etc…
 
## Let’s make:
How to connect Color Sensor TCS3200 to Arduino Uno?
### Step1: Hardware and Software Required
Color Sensor TCS3200 Module
Arduino Uno
Arduino IDE(1.0.6V)
 
### Step2: Hardware Connections
The color sensor should be connected to Arduino Uno as follows:
VCC to 5V
GND to GND
S0 to digital pin 8
S1 to digital pin 9
S2 to digital pin 12
S3 to digital pin 11
OUT to digital pin 10
In addition to this, connect red, green and blue led to digital pin 2,3 and 4 of Arduino Uno board.

### Step3: Code

<script src="https://gist.github.com/saylitechno/33daefe160dd549c4d06c9c9167d8c23.js"></script>

### Step4: Observe the Result on Serial monitor


