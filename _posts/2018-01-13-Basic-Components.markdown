---
layout: post
title:  "Basic Components"
description: Basic Components
categories: Electronic
---
 
# What is a Resistor?
I didn’t understand the resistor in the beginning. It seemed like it didn’t do anything! It was just there, consuming power.

But eventually, I learned that the resistor is actually extremely useful.

You’ll see resistors everywhere. And as the name suggests, they resist the current.

![]({{site.baseurl}}/images/Electronic/1/01.jpg)

But you are probably wondering:

“What do I use it for?”

You use the resistor to control the voltages and the currents in your circuit.

![]({{site.baseurl}}/images/Electronic/1/02.png)

Let’s say you have a 9V battery and you want to turn on an LED. If you connect the battery directly to the LED, LOTS of current will flow through the LED! Much more than the LED can handle. So the LED will become very hot and burn out after a short amount of time.

But – if you put a resistor in series with the LED, you can control how much current is going through the LED.

![]({{site.baseurl}}/images/Electronic/1/03.png)

A rectangle or a zigzag line is used as a symbol for the resistor

A resistor is nothing magic. Take a long wire and measure the resistance, and you will realize that resistance is just a normal property of wires
Some resistors are made up of just that. A long wire.
But you can also find resistors made of other types of materials. Like this carbon film resistor
you can see a common example of how a resistor is used to control the current for protecting the LED.

![]({{site.baseurl}}/images/Electronic/1/04.png)

A standard LED can only handle up to around 20-30 mA. If the current it much big- ger than that, the LED will quickly die.

Let’s say the LED in the circuit above needs 15 mA to give a good light, and it has a voltage drop of 2 volts. (These values should be specified by the supplier when you buy an LED.)

If you have a 9 V battery that you would like to power it with, which resistor value do you need?

The voltage specified for the LED is the voltage drop the LED will have under normal conditions. That means you know you will have 2V over the LED.


To find the resistor value, we start by finding the voltage drop over the resistor.

Since there is a 2-volt drop over the LED, there will be a 7V drop over the resistor (9V - 2V equals 7V).

You have 7V over the resistor, and whatever amount of current flows through it will also flow through the LED. So by setting the resistor value to a value that gives you 15 mA, you’ll also get 15 mA through the LED.

To find the necessary resistor value we use Ohm’s law.

![]({{site.baseurl}}/images/Electronic/1/05.png)

By placing your hand over the R in the Ohm’s law triangle, you get that Resistance
equals voltage (V) divided by current (I). This means you get:

### R = 7V / 0.015 A = 467Ω

470Ω is a standard value close enough, so by choosing this resistor value you decide that the current flowing in your circuit is 15 mA.


# Capacitors
A capacitor (also called condenser, which is the older term) is an electronic device that stores electric energy. It is similar to a battery, but is smaller, lightweight and charges up much quicker.
Or a capacitor works like a tiny rechargeable battery with very very very low capacity.

Capacitors are used in many electronic devices today, and can be made out of many different types of material.

![]({{site.baseurl}}/images/Electronic/1/06.png)

### How does the Capacitors work?
So the capacitor can store charge. And it can release the charge when needed. But how does it do this? How does a capacitor work on a deeper level?
capacitor is made up of two metallic plates. With a dielectric material in between the plates.
When you apply a voltage over the two plates, an electric field is created. Positive charge will collect on one plate and negative charge on the other.

![]({{site.baseurl}}/images/Electronic/1/07.png)

### Charging and uncharged capacitor

![]({{site.baseurl}}/images/Electronic/1/08.png)

![]({{site.baseurl}}/images/Electronic/1/09.png)

Above  Shows the simple working of a capacitor.Capacitors have many uses in electronic and electrical systems. They are so ubiquitous that it is rare that an electrical product does not include at least one for some purpose.
 
# Diode

![]({{site.baseurl}}/images/Electronic/1/10.jpg)

### What is a Diode?
Well, a diode is an electronic component that conducts current in one direction and blocks current from flowing in the other direction.
The diode symbol looks like this:

![]({{site.baseurl}}/images/Electronic/1/11.png)

![]({{site.baseurl}}/images/Electronic/1/12.png)

 
n the circuit above the diode is connected in the right direction. This means current can flow through it so that the LED will light up.
But what happens if we connect it the other way around?
In this second circuit the diode is connected the wrong way. This means that no current will flow in the circuit and the LED will be turned OFF.

### What Is a Diode Used For?
Diodes are very often used in power supplies. From the power outlet in your wall you get alternating current (AC). A lot of the devices we use need direct current (DC). To get DC from AC we need a rectifier circuit. It’s a circuit that converts from alternating current (AC) to direct current (DC). Diodes are the main components in rectifier circuits.
You have to apply enough voltage in the “right” direction – from positive to negative – for the diode to start conducting. Usually this voltage is around 0.7V.
The diode have limits and cannot conduct unlimited amounts of current.
Diodes are not perfect components. If you apply voltage in the wrong direction, there will be a little bit of current flowing. This current is called “leakage current”.
If you apply a high enough voltage in the “wrong” direction, the diode will break down and let current pass in this direction too.
 
 
# Transistor
The transistor is like an electronic switch. It can turn a current on and off.
![]({{site.baseurl}}/images/Electronic/1/13.jpg)

Transistors are devices that control the movement of electrons, and consequently, electricity. not only do they start and stop the flow of a current, but they also control the amount of the current. With electricity, transistors can both switch or amplify electronic signals, letting you control current moving through a circuit board with precision.
There are different types of transistors. A very common one is the “bipolar junction transistor” or “BJT”. It has three pins: Base (b), collector (c) and emitter (e). And it comes in two versions: NPN and PNP. The schematic symbol for the NPN looks like this:

![]({{site.baseurl}}/images/Electronic/1/14.jpg)

### How transistors work
The transistor works because of something called a semiconducting material. A current flowing from the base to the emitter “opens” the flow of current from the collector to the emitter.

![]({{site.baseurl}}/images/Electronic/1/15.png)

In a standard NPN transistor, you need to apply a voltage of about 0.7V between the base and the emitter to get the current flowing from base to emitter. When you apply 0.7V from base to emitter you will turn the transistor ON and allow a current to flow from collector to emitter.

![]({{site.baseurl}}/images/Electronic/1/16.png)

 
In the example above you can see how transistors work. A 9V battery connects to an LED and a resistor. But it connects through the transistor. This means that no current will flow in that part of the circuit until the transistor turns ON.
To turn the transistor ON you need to apply 0.7V from base to emitter of the transistor. Imagine you have a small 0.7V battery. (In a practical circuit you would use resistors to get the correct voltage from whatever voltage source you have)
When you apply the 0.7V battery from base to emitter, the transistor turns ON. This allows current to flow from the collector to the emitter. And thereby turning the LED ON!
 
 
# Integrated Circuit

![]({{site.baseurl}}/images/Electronic/1/17.png)

Fig: An Integrated Circuit (IC) connected on a breadboard

An integrated circuit is any kind of circuit that is integrated onto a chip. It can be a radio transmitter, a microcontroller, an audio amplifier or any other circuit you can think of.

By making a circuit on a small chip, it’s much easier to make advanced projects. Let’s say you want to make a tracking device for your car. You can find a GPS chip for positioning, a GSM chip to send text messages, and a microcontroller chip to control everything.

To figure out exactly what a specific IC does, you need to check its datasheet. The datasheet is a document that comes with every IC. You can find the datasheet for almost any IC by just searching for the chip name +“datasheet” in Google.

The datasheet explains what each of the pins does, how much voltage it needs, and often contains an example circuit to show you how to connect it.

![]({{site.baseurl}}/images/Electronic/1/18.png)

Figure : The symbol for an IC is often a box with pins. But it can also be the symbol of the func- tion of the IC (like a logic gate or an operational amplifier).

### Example
The 555 timer is a very useful and popular Integrated Circuit. You can use it to blink  a light, to create sound, to create a clock signal, add a countdown timer and a lot of other things.

A simple example is to blink an LED. By carefully selecting the values of the capaci- tor and resistors on the input side, you can control how fast the light should blink.

![]({{site.baseurl}}/images/Electronic/1/19.png)
Figure 24: This circuit will make the LED blink
The circuit shown in Figure 24 will blink an LED about once per second.

The resistors R1 and R2, together with the capacitor C1, set the output frequency of the output pin. The frequency is the number of times the output goes high per second. So an output frequency of 5 Hz would mean the output goes high 5 times per second.

You can find the output frequency of your circuit by using the following formula:

Frequency=1.44÷(R1+R2+R2)×C1
![]({{site.baseurl}}/images/Electronic/1/20.png)

To find the frequency, just replace R1, R2, and C1 with the values you use, and put it all into a calculator.
Let's say you have a circuit with the following component values: R1 = 100 kΩ
R2 = 10 kΩ C1 = 10 µF
The resistor values are in ohms, and the capacitance is in farads. That means R1 = 100 000Ω, R2 = 10 000Ω, and C1 = 0.00001 F.

Frequency = 1.44 / ((100 000Ω + 10 000Ω + 10 000Ω) * 0.00001 F)
Frequency = 1.44 / ((120 000Ω) * 0.00001 F)
Frequency = 1.2 Hz

According to this calculation, the output should turn on and off 1.2 times per se- cond with those values.

                                                                       


# LED
LED ( light emitting diode) is a two terminal semiconductor device. It is a type of diode that converts electrical energy  into light. It emits light when electric current pass through it.

![]({{site.baseurl}}/images/Electronic/1/21.png)

It has two terminals ,one is positive(anode) and other one is negative (cathode) as shown above.


### APPLICATIONS:
There are many applications of LED and are also used to make different electronics projects.
1. LED is used as a bulb in home.
2. LED are used in motorcycles and cars
3. These are used in mobile phones to display messages
1 . It is used in traffic light signals


 
 
