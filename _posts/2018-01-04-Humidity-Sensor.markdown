---
layout: post
title:  "Humidity Sensor"
description: Humidity Sensor
categories: Electronic
---

# What is a Humidity Sensor?
A Humidity sensor (or hygrometer) senses, measures and reports the relative humidity in the air. It therefore measures both moisture and air temperature.

![]({{site.baseurl}}/images/Electronic/5/01.jpg)

# How does the Sensor works?
The sensor is composed of two metal plates and contains a non-conductive polymer film between them. This film collects moisture from the air, which causes the voltage between the two plates to change. These voltage changes are converted into digital readings showing the level of moisture in the air.





### Pin Description
![]({{site.baseurl}}/images/Electronic/5/02.jpg)
VCC    3.3V to 5V
Data    Outputs both Temperature and Humidity through serial data
GND    Connected to the ground of the circuit 

# Applications for Humidity sensor:
Humidity sensors can be used as a monitoring and preventive measure in homes for people with illnesses that are affected by humidity. They are also found as part of home heating, ventilating, and air conditioning systems (HVAC systems). They can also be found in offices, cars, humidors, museums, industrial spaces and greenhouses and can be used in meteorology stations to report and predict weather. Dew sensors are used in the coating industry because the application of paint and other coatings may be extremely sensitive to dew point.


# Let’s Make    
## Shop from -  http://technoventor.in/


## Check temperature and humidity of your room.

### Step1: Things you need

1. Arduino uno
2. Sensor (DHT11)
3. Type A to B cable

### Step2: Wiring

![]({{site.baseurl}}/images/Electronic/5/03.png)

### Step3: Code
We will be using a Library that is available for this sensor. Once you have the library, just go ahead and extract it to the Library folder inside your Arduino IDE software folder.
You can download the DHT Library we used here: DHT-Library

#include "DHT.h"
#define dht_apin A0 // Analog Pin sensor is connected to
 dht DHT;
  void setup()
{
   Serial.begin(9600);
   delay(500);//Delay to let system boot
   Serial.println("DHT11 Humidity & temperature Sensor\n\n");
   delay(1000);//Wait before accessing Sensor
 }//end "setup()"
 void loop()
{
  //Start of Program 
    DHT.read11(dht_apin);
    Serial.print("Current humidity = ");
    Serial.print(DHT.humidity);
    Serial.print("%  ");
    Serial.print("temperature = ");
    Serial.print(DHT.temperature); 
    Serial.println("C  ");
    delay(5000);//Wait 5 seconds before accessing sensor again.
  //Fastest should be once every two seconds.
 }// end loop()


### Step4: Observe Result on Serial monitor



# Below are the examples of Humidity sensor. Enjoy making!!
 
 
http://www.instructables.com/id/DHT11-Temperature-Humidity-Sensor-With-LCD-Display/
https://www.electronicshub.org/dht11-humidity-sensor-arduino/

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
