---
layout: post
title:  "ARDUINO UNO PROJECTS"
description:  ARDUINO UNO PROJECTS
categories: project
---


                                                     
# ARDUINO AND ULTRASONIC SENSOR BASED DISTANCE MEASRUREMENT
Ultrasonic sensors are great tools to measure distance without actual contact and used at several places like water level measurement, distance measurement etc. This is an efficient way to measure small distances precisely. In this project we have used an Ultrasonic Sensor to determine the distance of an obstacle from the sensor. Basic principal of ultrasonic distance measurement is based on ECHO. When sound waves are transmitted in environment then waves are return back to origin as ECHO after striking on the obstacle. So we only need to calculate the travelling time of both sounds means outgoing time and returning time to origin after striking on the obstacle. As speed of the sound is known to us, after some calculation we can calculate the distance.   

### STEP 1: Components Used
Arduino Pro Mini
Ultrasonic sensor Module
16x2 LCD
Scale
Bread board
9 volt battery
Connecting wires
#### Ultrasonic Sensor Module
Ultrasonic sensor HC-SR04 is used here to measure distance in range of 2cm-400cm with accuracy of 3mm. The sensor module consists of ultrasonic transmitter, receiver and the control circuit. The working principle of ultrasonic sensor is as follows:
High level signal is sent for 10us using Trigger.
The module sends eight 40 KHz signals automatically, and then detects whether pulse is received or not.
If the signal is received, then it is through high level. The time of high duration is the time gap between sending and receiving the signal.
#### Distance= (Time x Speed of Sound in Air (340 m/s))/2

![]({{site.baseurl}}/images/Project/UNO/01.png)

 
### STEP 2 :CIRCUIT DIAGRAM AND EXPLANATION
![]({{site.baseurl}}/images/Project/UNO/02.png)

The circuit diagram for arduino and ultrasonic sensor is shown above to measure the distance. In circuit connections Ultrasonic sensor module’s “trigger” and “echo” pins are directly connected to pin 18(A4) and 19(A5) of arduino. A 16x2 LCD is connected with arduino in 4-bit mode. Control pin RS, RW and En are directly connected to arduino pin 2, GND and 3. And data pin D4-D7 is connected to 4, 5, 6 and 7 of arduino.
 
First of all we need to trigger the ultrasonic sensor module to transmit signal by using arduino and then wait for receive ECHO. Arduino reads the time between triggering and Received ECHO. We know that speed of sound is around 340m/s. so we can calculate distance by using given formula:
Distance= (travel time/2) * speed of sound
Where speed of sound around 340m per second.
A 16x2 LCD is used for displaying distance.
 
### STEP 3:  ULTRASONIC CODE FOR DISTANCE MEASUREMENT
CODE
 
#include<LiquidCrystal.h>
 
#definetrigger18
#defineecho19
 
LiquidCrystallcd(2,3,4,5,6,7);
 
floattime=0,distance=0;
 
voidsetup()
{
 lcd.begin(16,2);
 pinMode(trigger,OUTPUT);
 pinMode(echo,INPUT);
 lcd.print("Ultrasonic");
 lcd.setCursor(0,1);
 lcd.print("DistanceMeter");
 delay(2000);
 lcd.clear();
 lcd.print("CircuitDigest");
 delay(2000);
}
 
voidloop()
{
 lcd.clear();
 digitalWrite(trigger,LOW);
 delayMicroseconds(2);
 digitalWrite(trigger,HIGH);
 delayMicroseconds(10);
 digitalWrite(trigger,LOW);
 delayMicroseconds(2);
 time=pulseIn(echo,HIGH);
 distance=time*340/20000;
 lcd.clear();
 lcd.print("Distance:");
 lcd.print(distance);
 lcd.print("cm");
 lcd.setCursor(0,1);
 lcd.print("Distance:");
 lcd.print(distance/100);
 lcd.print("m");
 delay(1000);
}

### STEP 4 :

![]({{site.baseurl}}/images/Project/UNO/03.png)

 
 
# Project II
# ARDUINO LIGHT SENSOR CIRCUIT USING LDR

### STEP 1: COMPONENTS REQUIRED
Arduino UNO
LDR (Light Dependent Resistor)
Resistor (100k-1;330ohm-1)
LED - 1
Relay module - 5v
Bulb/CFL
Connecting wires
Breadboard
 
 
### STEP 2: CIRCUIT DIAGRAM
![]({{site.baseurl}}/images/Project/UNO/04.png)
 
 
### STEP 3: Controlling Relay using LDR with Arduino
![]({{site.baseurl}}/images/Project/UNO/05.png)
  
 
Instead of controlling an LED according to the brightness and darkness, we can control our home lights or any electrical equipment. All we have to do is connect a relay module and set the parameter to turn ON and OFF the any AC appliance according to the intensity of the light. If the value falls below 700, which means it Dark, then the relay operates and the lights turns ON. If the value is greater than 700, which means its day or bright, then the relay will not operate and the lights remain OFF. Learn more about relay here and how to connect an AC appliance to relay.
![]({{site.baseurl}}/images/Project/UNO/06.png)
 
 
### STEP 4 :
CODE: 
#define relay 10
int LED = 9;
int LDR = A0;
void setup() 
{
Serial.begin(9600);
pinMode(LED, OUTPUT);
pinMode(relay, OUTPUT);
pinMode(LDR, INPUT);
}
void loop() {
int LDRValue = analogRead(LDR);
Serial.print("sensor = ");
Serial.print(LDRValue);
if (LDRValue <=700) 
{
digitalWrite(LED, HIGH);
digitalWrite(relay, HIGH);
Serial.println("It's Dark Outside; Lights status: ON");
}
else 
{
digitalWrite(LED, LOW);
digitalWrite(relay, LOW);
Serial.println("It's Bright Outside; Lights status: OFF");
}
}


 
 

1. https://create.arduino.cc/projecthub/maverick/pathfinder-229d5d?ref=part&ref_id=8233&offset=1
2 . https://create.arduino.cc/projecthub/abishek-bhalaaji/arduino-based-digital-temperature-sensor-76e16c?ref=tag&ref_id=sensor&offset=66
3. https://www.electroschematics.com/9683/arduino-night-security-alarm-pir-sensor/
4. https://create.arduino.cc/projecthub/will-su/touchless-automatic-motion-sensor-trash-can-bbeed1?ref=tag&ref_id=servo&offset=4
5. https://create.arduino.cc/projecthub/mitov/arduino-and-visuino-control-servo-with-buttons-18a527?ref=tag&ref_id=servo&offset=8
6.  http://www.instructables.com/id/Secret-Knock-Detecting-Door-Lock/
7. https://circuitdigest.com/microcontroller-projects/arduino-light-sensor-using-ldr
8. https://create.arduino.cc/projecthub/smart-tech/the-perfectautomatic-lighting-system-using-arduino-ldr-e3c0f7?ref=tag&ref_id=arduino&offset=217
9. https://create.arduino.cc/projecthub/jasmeet-singh/poseidon-the-water-saver-8ddb58?ref=tag&ref_id=gsm&offset=3
10. https://circuitdigest.com/microcontroller-projects/arduino-calculator-using-4x4-keypad
11.https://circuitdigest.com/microcontroller-projects/diy-arduino-robotic-arm-tutorial
