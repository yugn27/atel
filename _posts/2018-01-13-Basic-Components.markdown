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


![]({{site.baseurl}}/images/Electronic/1/05.png)


To find the resistor value, we start by finding the voltage drop over the resistor.

Since there is a 2-volt drop over the LED, there will be a 7V drop over the resistor (9V - 2V equals 7V).

You have 7V over the resistor, and whatever amount of current flows through it will also flow through the LED. So by setting the resistor value to a value that gives you 15 mA, you’ll also get 15 mA through the LED.

To find the necessary resistor value we use Ohm’s law.

![]({{site.baseurl}}/images/Electronic/1/06.png)

By placing your hand over the R in the Ohm’s law triangle, you get that Resistance
equals voltage (V) divided by current (I). This means you get:

### R = 7V / 0.015 A = 467Ω

470Ω is a standard value close enough, so by choosing this resistor value you decide that the current flowing in your circuit is 15 mA.
 
 
