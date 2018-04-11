---
layout: post
title:  "Temperature Sensor"
description: Temperature Sensor
categories: Electronic
---


# What is a temperature Sensor?
A temperature sensor is a device which is designed specifically to measure the hotness or coldness of an object. LM35 is a precision IC temperature sensor with its output proportional to the temperature (in °C).
The operating temperature range is from -55°C to 150°C.

![]({{site.baseurl}}/images/Electronic/9/01.jpg)

LM35 Temperature Sensor which is a semiconductor based sensor. LM35 is an integrated analog temperature sensor whose electrical output is proportional to Degree Centigrade. LM35 Sensor does not require any external calibration or trimming to provide typical accuracies. The LM35’s low output impedance, linear output, and precise inherent calibration make interfacing to readout or control circuitry especially easy.


# Pin Description

![]({{site.baseurl}}/images/Electronic/9/01.jpg)


# Let’s make
## Shop from- http://technoventor.in/

### “Temperature monitoring system”

### Step1:
Things you need.
Arduino UNO, Leonardo or equivalent
Breadboard
Jumper Wires
USB Cord
LM35 temperature sensor
### Step2: Wiring

![]({{site.baseurl}}/images/Electronic/9/01.jpg)


### Step3: Code
float temp;
int tempPin = 0;
void setup()
{
Serial.begin(9600);
}
void loop()
{
temp = analogRead(tempPin);
temp = temp * 0.48828125;
Serial.print("TEMPRATURE = ");
Serial.print(temp);
Serial.print("*C");
Serial.println();
delay(1000);
}


### Step4: Result

Load the code into to your board and open the serial monitor you should see both Fahrenheit and Celsius.
# Below are the examples of Temperature sensor. Enjoy making!!
 
https://www.hackster.io/Jasleen1429/temperature-sensor-to-control-servo-motor-b770f9
http://www.circuitstoday.com/lm35-and-arduino-interfacing
http://www.instructables.com/id/Arduino-LCD-Thermometer-with-LM35-Temp-Sensor/
 

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

