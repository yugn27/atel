---
layout: post
title:  "Rain Drop Sensor"
description: Rain Drop Sensor
categories: Electronic
---
 
 
 
### What is Rain drop Sensor?
The raindrop sensor module is used for rain detection. It is also for measuring rainfall intensity. The module includes a rain board and a control board that are separate for more convenience.
It has a power indicator LED and an adjustable sensitivity though a potentiometer. The module is based on the LM393 op amp. It includes a printed circuit board(control board) that “collects” the rain drops. As rain drops are collected on the circuit board, they create paths of parallel resistance that are measured via the op amp. The lower the resistance (or the more water), the lower the voltage output. Conversely, the less water, the greater the output voltage on the analog pin. A completely dry board for example will cause the module to output five volts.

![]({{site.baseurl}}/images/Electronic/chap18/1.jpg)

### How Raindrop Sensor works?
This module allows you measure moisture via analog output pins and it provides a digital output when a threshold of moisture is exceeded .The module is based on the LM393 op amp.
It includes the electronics module and a printed circuit board(control board) that “collects” the rain drops .As rain drops are collected on the circuit board, they create paths of parallel resistance that are measured via the op amp. The lower the resistance (or the more water), the lower the voltage output. Conversely, the less water, the greater the output voltage on the analog pin. A completely dry board for example will cause the module to output five volts

### Hardware Connections

![]({{site.baseurl}}/images/Electronic/chap18/2.jpg)

First connect the control board to the rain drop sensor module as shown in the image and then connect the sensor module to Uno as follows:
Vcc to 5V
Gnd to Gnd
D0 to digital pin
Let’s Make:
Rain monitoring system
Step1: What you will need - Hardware
For this tutorial you will need:
Arduino uno
Breadboard
Raindrops Sensor module


### Step2: The Circuit

![]({{site.baseurl}}/images/Electronic/chap18/3.png)




The connections are pretty easy, see the image above with the breadboard circuit schematic.
Make sure to watch sensor from front side:
Connect the Vcc pin to 5 Volts (5V) if you use analog pin or connect Vcc pin to 3.3 Volts(3.3V) if you use digital pin
Connect the A0  pin to pin A0
Connect D0 pin to Digital pin 2
Connect the GND pin to ground (GND)
+ pin of sensor to + pin of module
- pin of sensor to - pin of module



### Step3: Code

<script src="https://gist.github.com/saylitechno/91b44114a33f645ec778347ef42b70c2.js"></script>


### Step4:Observe the result on Serial monitor
