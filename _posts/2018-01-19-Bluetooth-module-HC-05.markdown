---
layout: post
title:  "Bluetooth module HC-05"
description: Bluetooth module HC-05
categories: Electronic
---
 
 
### What is Bluetooth module?
Bluetooth is a technology for wireless communication. It is designed to replace cable connections .It uses serial communication to communicate with devices. It communicates with microcontroller using serial port (USART). Usually, it connects small devices like mobile phones, PDAs and TVs using a short-range wireless connection to exchange documents. It uses the 2.45GHz frequency band. The connection can be point-to-point or multi-point where the maximum range is 10 meters. The transfer rate of the data is 1Mbps.

![]({{site.baseurl}}/images/Electronic/chp19/01.jpg)

### Pin Description
The HC-05 Bluetooth Module has 6pins. They are as follows:
ENABLE: 
When enable is pulled LOW, the module is disabled which means the module will not turn on and it fails to communicate. When enable is left open or connected to 3.3V, the module is enabled i.e the module remains on and communication also takes place.
 
Vcc: 
Supply Voltage 3.3V to 5V
GND: 
Ground pin
TXD & RXD: 
These two pins acts as an UART interface for communication
STATE: 
It acts as a status indicator. When the module is not connected to / paired with any other bluetooth device, signal goes Low. At this low state, the led flashes continuously which denotes that the module is not paired with other device. When this module is connected to/paired with any other bluetooth device, the signal goes High. At this high state, the led blinks with a constant delay say for example 2s delay which indicates that the module is paired.
 
 
BUTTON SWITCH: 
This is used to switch the module into AT command mode. To enable AT command mode, press the button switch for a second. With the help of AT commands, the user can change the parameters of this module but only when the module is not paired with any other BT device. If the module is connected to any other bluetooth device, it starts to communicate with that device and fails to work in AT command mode.


![]({{site.baseurl}}/images/Electronic/chp19/02.jpg)

### Applications
1. Wireless communication between two microcontrollers
2. Communicate with Laptop, Desktops and mobile phones
3. Consumer applications
4. Wireless Robots
5. Home Automation


## Lets make:
Control an LED using a Phone
### Step1: Things you will need.
1 Arduino UNO
2 Bluetooth Module
3 Type A to B cable
4 LED
5 Jumpers
6 Android mobile



### Step2: Connections with Arduino UNO 


![]({{site.baseurl}}/images/Electronic/chp19/03.png)



### Step3: Code

<script src="https://gist.github.com/saylitechno/738244f008f93acaba6b95f84cddc5a6.js"></script>


### Step4: Upload the program 

### Step5:Download the App (HC-05 Terminal App) or search on google playstore 

### Step6: Pair your device with HC 05/06 Bluetooth module1) Turn ON HC 05/06 Bluetooth module2) Scan for available device3) Pair to HC 05/06 by entering default password 1234 OR 0000

### Step7: Install  LED application on your android device and Open the Application

### Step8: Press paired devices and Select your Bluetooth module from the List (HC 05)   
 
### Step9: After connecting successfully and Press ON button to turn ON LED and OFF button to turn OFF LED
 
### Step10: Disconnect button to disconnect from Bluetooth module
 
### Step11: Observe the output
![]({{site.baseurl}}/images/Electronic/chp19/04.jpg)
