---
layout: post
title:  "Sound Playback Module"
description: Sound playback module
categories: Electronic
---


What is a Sound Playback Module?
 
Voice Record Module is base on ISD1820, which a multiple-message record/playback device. It can offer true single-chip voice recording, no-volatile storage, and playback capability for 8 to 20 seconds. The sample is 3.2k and the total 20s for the Recorder.
 
![]({{site.baseurl}}/images/Electronic/9/01.jpg)

This module use is very easy which you could direct control by push button on board or by Microcontroller such as Arduino, etc. From these, you can easy control record, playback and repeat and so on.
 
Pin description

![]({{site.baseurl}}/images/Electronic/9/01.jpg)
 
PLAYE – Playback, Edge-activated: When a HIGH-going transition is detected on continues until an End-of-Message (EOM) marker is encountered or the end of the memory space is reached.
REC – The REC input is an active-HIGH record signal. The device records whenever REC is HIGH. This pin must remain HIGH for the duration of the recording. REC takes precedence over either playback (PLAYL or PLAYE) signal.
Speaker Outputs – The SP+ and SP- pins provide direct drive for loudspeakers with impedances as low as 8Ω.
MIC – Microphone Input, the microphone input transfers its signals to the on-chip preamplifier.
REPLAY – loop play the record.
FT – Feed Through: This mode allows use of the speaker drivers for external signals.
ISD1820 – IC chip
Lead Out IO – VCC LED NC FT GND / VCC REC PLAYE PLAYL GND
P2 – default short connection ROSC to 100kΩ resistance, that’s means record duration is 10s
PLAYL – Playback, Level-activated, when this input pin level transits for LOW to HIGH, a playback cycle is initiated.

Control it with the Arduino
 
Shop from- http://technoventor.in/
 
In the following example we’ll use an IR sensor of this type:
 
![]({{site.baseurl}}/images/Electronic/9/01.jpg)
 
VDC - 3.3V or 5V from Arduino
GND - GND of Arduino
OUT - Pin 2 of the arduino

![]({{site.baseurl}}/images/Electronic/9/01.jpg)
 
When it detects a passage the Arduino will change the state of the pin 7 which will give the order to play the recorded sound. We will use this function (play the sound) in the immediate because it is the most interesting.
 
 
The arduino code:

              int inputSensor = 2; // Output pin of IR Sensor
              int PlayE = 7; // Voice recorder pin
              int irState = LOW; // IR Sensor is low by default
              int val = 0;
              void setup()
            {
                pinMode(inputSensor, INPUT); // Pin 2 en entrée
                pinMode(PlayE, OUTPUT); // Pin 7 en sortie
                Serial.begin(9600);
                Serial.println("init");
              }
               
               void loop()
           {
               val = digitalRead(inputSensor);
               if (val == HIGH) {
               if (irState == LOW) {
               digitalWrite(PlayE,HIGH);
               irState = HIGH;
            }
                } else
            {  
                if (irState == HIGH){
                digitalWrite(PlayE,LOW);
                irState = LOW;
             }
                }
                } 
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
