---
layout: post
title:  "Ultrasonic Sensor"
description: Ultrasonic Sensor
image: 'https://yugn27.github.io/atel/images/design/3dprinterpost.jpg'
categories: Electronic
---
 

 
We’ve all had fun shouting into a cave or large space and hearing our voice coming back (echo) to us at some point during our childhood. And if you’re like me, a fully grown adult who still does it now and then, it’s still pretty fun. The reason behind this is fairly simple. A sound is merely a wave of pressure moving through the air at approximately 340 meters/second (m/s). It’s a mechanical wave, which means that it will bounce off objects. The further away from you the objects are, the longer it takes for your voice to reach them, and then to bounce back to your ears. This principle has been understood for a long time now, and many things around us are built on that same principle, including ultrasonic sensors.

### What is Ultrasonic Sensor and how it works?

As the name indicates, ultrasonic sensors measure distance by using ultrasonic waves.
The sensor head emits an ultrasonic wave and receives the wave reflected back from the target. Ultrasonic Sensors measure the distance to the target by measuring the time between the emission and reception.

![]({{site.baseurl}}/images/Electronic/15/01.jpg)

Ultrasonic sensors, whilst fancy and high-tech are fairly simple devices. They emit sounds waves, wait for them to bounce off objects, and then measure the time it took for the wave to be picked up by the receiver. If you half that time (it has to go out and back), you get the time it took for the wave to reach the object you’re measuring. 
The HC-SR04 is a low-cost sensor which has a range of  2cm-500cm and a resolution of  0.3cm. 


![]({{site.baseurl}}/images/Electronic/15/02.png)


### How will you use this Sensor?

The HC-SR04 Ultrasonic Module has 4 pins, Ground, VCC, Trig and Echo. The Ground and the VCC pins of the module needs to be connected to the Ground and the 5 volts pins on the Arduino Board respectively and the Trig and Echo pins to any Digital I/O pin on the Arduino Board.

![]({{site.baseurl}}/images/Electronic/15/02.jpg)


VCC – We have to connect this pin to 5V of Arduino
TRIG- Connect this pin to Digital I/O pin of Arduino board
ECHO- Connect this pin to Digital I/O pin of Arduino board
GND- Connect this pin to Ground

### Pin Description
VCC- Connects to 5V of positive voltage to power.
TRIG- A pulse is sent here for sensor to go into the ranging mode for object detection.
ECHO- the Echo sends a signal back if an object has been detected or not. If a signal is returned, an object has been detected.
GND- Completes electrical pathway of the power.

### Applications:
Some applications of Ultrasonic sensor are: It is used as distance measurement, water level detection, obstacle detection etc

## Let’s Make
### Shop from-  http://technoventor.in/

#### Distance sensing using ultrasonic sensor
Things you will need
Arduino UNO 
Ultrasonic Sensor
Solderless bread board
Jumpers
Type A to B cable

### Step1: Gather your material

![]({{site.baseurl}}/images/Electronic/15/04.jpg)





### Step2: Connections with Arduino

![]({{site.baseurl}}/images/Electronic/15/05.jpg)


The circuit: *
VCC connection of the sensor attached to +5V
GND connection of the sensor attached to ground
TRIG connection of the sensor attached to digital pin 2
ECHO connection of the sensor attached to digital pin 4
 

### Step3: Programming Arduino
const int trigPin = 2;
const int echoPin = 4;
void setup() {
Serial.begin(9600);}
void loop()
{
long duration, inches, cm;
pinMode(trigPin, OUTPUT);
digitalWrite(trigPin, LOW);
delayMicroseconds(2);
digitalWrite(trigPin, HIGH);
delayMicroseconds(10);
digitalWrite(trigPin, LOW);
pinMode(echoPin, INPUT);
duration = pulseIn(echoPin, HIGH);
inches = microsecondsToInches(duration);
cm = microsecondsToCentimeters(duration);
Serial.print(inches);
Serial.print("in, ");
Serial.print(cm);
Serial.print("cm");
Serial.println();
delay(100);
}
long microsecondsToInches(long microseconds)
{return microseconds / 74 / 2;
}
long microsecondsToCentimeters(long microseconds)
{return microseconds / 29 / 2;}

### Step4: Check result on Serial monitor

![]({{site.baseurl}}/images/Electronic/15/06.jpg)


Below are the examples of ultrasonic sensor. Enjoy making!!

https://create.arduino.cc/projecthub/NicoB1/display-ultrasonic-sensor-and-servo-7e5fea

https://create.arduino.cc/projecthub/Bill_Mougios/arduino-controlled-car-with-hc-sr04-a8e57d


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

