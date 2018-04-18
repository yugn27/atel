---
layout: post
title:  "PROJECTS ARDUINO NANO"
description:  PROJECTS ARDUINO NANO
categories: project
---


# LIE SENSOR 

### Step 1: COMPONENTS REQUIRED
Arduino nano
Breadboard
2.21 kohm resistor
LED
Open build wire cable

![]({{site.baseurl}}/images/Project/NANO/nano1.png)


### Step 2: CODE

void setup()
{
    Serial.begin(9600);
    pinMode(2, OUTPUT);
    pinMode(3, OUTPUT);
    pinMode(4, OUTPUT);
    digitalWrite(2, HIGH);
    delay(500);
    digitalWrite(3, HIGH);
    delay(500);
    digitalWrite(4, HIGH);
    delay(500);
}
 
void loop()
{
    if (analogRead(A0) > 60)
    {
        digitalWrite(4, HIGH);
    }
    else
    {
        digitalWrite(4, LOW);
    }
    if (analogRead(A0) > 20)
    {
        digitalWrite(2, HIGH);
    }
    else
    {
        digitalWrite(2, LOW);
    }
    if (analogRead(A0) > 45)
    {
        digitalWrite(3, HIGH);
    }
    else
    {
        digitalWrite(3, LOW);
    }
    Serial.println(analogRead(A0));
    delay(20);
}




### Step 3: CIRCUIT DIAGRAM

![]({{site.baseurl}}/images/Project/NANO/nano2.png)




Projects on Arduino Nano
1 https://create.arduino.cc/projecthub/user269049/lie-sensor-d12993?ref=part&ref_id=11332&offset=15

2  https://www.hackster.io/TechWithZan/arduino-nano-lcd-stopwatch-without-potentiometer-7a2854

3  https://create.arduino.cc/projecthub/boaz/nano-ir-remote-for-dc-motors-6aa3a4?ref=part&ref_id=11332&offset=192

4  http://www.instructables.com/id/Arduinonano-Clap-Switch/

5  http://www.instructables.com/id/Arduino-Simple-Memory-Game/


