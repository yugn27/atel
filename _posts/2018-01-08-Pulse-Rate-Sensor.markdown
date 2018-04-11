---
layout: post
title:  "Pulse Rate Sensor"
description: Pulse rate Sensor
categories: Electronic
---


# What is Pulse Rate sensor and how it works?
Pulse rate Sensor is a well-designed sensor for arduino. The sensor clips onto a fingertip or earlobe and plugs right into Arduino. It also includes an open-source monitoring app that graphs your pulse in real time.

![]({{site.baseurl}}/images/Electronic/9/01.jpg)

The Pulse Sensor can be connected to arduino, or plugged into a breadboard. The front of the sensor is the pretty side with the Heart logo. This is the side that makes contact with the skin. On the front you see a small round hole, which is where the LED shines through from the back, and there is also a little square just under the LED. The square is an ambient light sensor, exactly like the one used in cell phones, tablets, and laptops, to adjust the screen brightness in different light conditions. The LED shines light into the fingertip or earlobe, or other capillary tissue, and sensor reads the light that bounces back. The back of the sensor is where the rest of the parts are mounted.


How  to use this Sensor?

![]({{site.baseurl}}/images/Electronic/9/02.jpg)


The Pulse Rate Sensor should be connected to Uno as follows:
Signal(S) to A0
Vcc(+) to 5V
Gnd(-) to Gnd
Note: The front side (Heart logo) of sensor should be in contact with the skin. The user need to wrap the sensor around the finger as shown in the image.


# Applications:
Heart beat sensor as the name suggest is used in medical applications.

# Let’s Make
## Shop from - http://technoventor.in/

## Arduino based heart beat monitor
### Step1: Materials you need
1.  Arduino Uno  Board  and USB Cable.
2. Pulse Sensor Arduino
3. Jumper Wires
4. LCD
5. Potentiometer 10K
6. 2 LEDs
7. Breadboard

### Step 2: Pin out Details
 ![]({{site.baseurl}}/images/Electronic/9/03.PNG)
 
you can see the s, + and - on pulse sensor's back view as shown in the picture above.
S : signal, connected to any of your microcontroller's digital pin.
+ : supply, 3V up to 5V
- : ground
### Step 3: Connections with arduino:
 
![]({{site.baseurl}}/images/Electronic/9/04.jpg)

1. Connect Pulse Sensor to Arduino Uno Board as following:
+  to  +5V
-  to GND
S to A0
2. Connect LCD to Arduino Uno Board as following:
VSS to +5V
VDD to GND
RS to 12
RW to GND
E to D11
D4 to D5
D5 to D4
D6 to D3
D7 to D2
A/VSS to +5V
K/VDD to GND
 
3. Connect 10K Potentiometer to LCD as following (refer image for potentiometer pin out):
GND to GND
Data to v0
VCC to +5V
4. Connect LED to Arduino as following:
LED1 (RED, blink Pin) to D13
LED2 (GREEN, fade Rate) to D8
 
### Step 4: Connect to Your Computer

![]({{site.baseurl}}/images/ckt01.png)

After you have completed your circuit, connect your Arduino Uno Board to your computer via USB Cable. You can see your LCD is on.
### Step 5: Library

![]({{site.baseurl}}/images/ckt01.png)

![]({{site.baseurl}}/images/ckt01.png)

You have to download this library before uploading the sample source code into your Arduino IDE to allow Arduino to communicate with LCD. Download the ZIP file below > Open Zip File > Extract to your Arduino Uno Library folder.


### Step 6: Sample Source Code
![]({{site.baseurl}}/images/ckt01.png)
![]({{site.baseurl}}/images/ckt01.png)


NOTE: DO NOT connect the Pulse Sensor to your body while your computer or arduino is being powered from the mains AC line. That goes for charging laptops and DC power supplies.


Step 7: Serial Monitor
![]({{site.baseurl}}/images/ckt01.png)
![]({{site.baseurl}}/images/ckt01.png)
When you open your serial monitor, make sure you change your baud rate to 115200; it has to match to the baud rate stated in the sample source code.




Step 8: Result

![]({{site.baseurl}}/images/ckt01.png)
![]({{site.baseurl}}/images/ckt01.png)

After it’s done uploading, you should see LED1 (red) blink in time with your heartbeat when you place your finger on the sensor. If you grip the sensor too hard, you will squeeze all the blood out of your fingertip and there will be no signal! If you hold it too lightly, you will invite noise from movement and ambient light. So, place your finger on the sensor lightly till you get a read on the LCD or serial monitor that shows signal is already transmitted. You will be able to get the reading on both serial monitor and LCD.

Below are the examples of Pulserate sensor. Enjoy making!!

https://circuitdigest.com/microcontroller-projects/heartbeat-monitor-project-using-arduino
http://www.circuitstoday.com/pulse-sensor-arduino

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
