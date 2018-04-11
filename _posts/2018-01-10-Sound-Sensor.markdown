---
layout: post
title:  "Sound Sensor"
description: Sound Sensor
categories: Electronic
---

# What is Sound Sensor?
The sound sensor module provides an easy way to detect sound and is generally used for detecting sound intensity. This module can be used for security, switch, and monitoring applications. Its accuracy can be easily adjusted for the convenience of usage.

![]({{site.baseurl}}/images/Electronic/11/01.jpg)

It uses a microphone which supplies the input to an amplifier, peak detector and buffer. When the sensor detects a sound, it processes an output signal voltage 
which is sent to a microcontroller then performs necessary processing.

# Pin Description

![]({{site.baseurl}}/images/Electronic/9/02.png)

Parameter
Value
VCC
5 Vdc from your Arduino
Ground
GND from your Arduino
Out
Connect to Digital Input Pin
Power LED
Illuminates when power is applied
Sound Detection LED
Illuminates when sound is detected
Sound Set Point Adjust
CW = More Sensitive
CCW = Less Sensitive

# Applications of Sound Sensor
Given that this device measures whether or not sound has exceeded a threshold,  you’re basically left with determining what it is you want to do.   What I mean by this is that you can do something when it is quiet and/or you can do something when it is loud.  For example:
You could detect whether or not a motor is running.
You could set a threshold on pump sound so that you know whether or not there is cavitation.
In the presence of no sound,  you might want to create an ambiance by turning on music.
In the presence of no sound and no motion, you may go into an energy savings mode and turn off the lights.

# Let’s make
## Shop from- http://technoventor.in/

Turn ON the lights when Sound is detected
### Step 1: Things you need
Arduino uno
Sound Sensor module
Jumpers 
LED
A to B Cable

### Step2: Wiring
VCC : 5VDC from your Arduino
GND:  GND from your Arduino
Out : Connect to digital input pin3
Connect LED to pin 13


### Step3:Code
int Led = 13 ;// define LED Interface
int buttonpin = 3; // define D0 Sensor Interface
int val = 0;// define numeric variables val
 void setup ()
{
 pinMode (Led, OUTPUT) ;// define LED as output interface
 pinMode (buttonpin, INPUT) ;// output interface D0 is defined sensor
}
 void loop ()
{
val = digitalRead(buttonpin);// digital interface will be assigned a value of pin 3 to read val
if (val == HIGH) // When the sound detection module detects a signal, LED flashes
{
digitalWrite (Led, HIGH);
 }
 else
 {
digitalWrite (Led, LOW);
  }
}

### Step 4: Observe the result

Below are the examples of Sound sensor. Enjoy making!!
https://www.hackster.io/dandt_matt/sound-wave-starting-gun-0b774e
http://www.instructables.com/id/How-to-turn-ON-AC-light-and-Fan-by-clap-using-Ardu/

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
