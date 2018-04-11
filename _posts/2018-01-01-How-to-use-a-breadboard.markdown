
---
layout: post
title:  "How to use a breadboard?"
description: How to use a breadboard? 
categories: Electronic
---



# What is a breadboard?
A breadboard is a rectangular plastic board with a bunch of tiny holes in it. These
holes let you easily insert electronic components to prototype (meaning to build
and test an early version of) an electronic circuit
The connections are not permanent, so it is easy to remove a component if you
make a mistake, or just start over and do a new project. This makes breadboards
great for beginners who are new to electronics. You can use breadboards to make
all sorts of fun electronics projects, from different types of robots or any
electronics based projects. 
# Where does the name &quot;breadboard&quot; come from?
You might be wondering what any of this has to do with bread. The
term breadboard comes from the early days of electronics, when people would
literally drive nails or screws into wooden boards on which they cut bread in order
to connect their circuits. Luckily, since you probably do not want to ruin all your
cutting boards for the sake of an electronics project, today there are better options.

Here is a nice illustration:
![]({{site.baseurl}}/images/ckt01.png)

# How are the holes connected?
## Horizontal Rows
![]({{site.baseurl}}/images/Electronic/2/02.png) 

You can see that the horizontal rows are connected on the inside.

![]({{site.baseurl}}/images/Electronic/2/03.png)

When you put your IC chip on board it should hurdle the center divider

## Vertical Columns
![]({{site.baseurl}}/images/Electronic/2/04.png)
Vertical columns on the side of the breadboard are for power and ground.

These power rails are also isolated to the right and left side of the breadboard. If you have to manage two different power supplies or voltages, they can be isolated by keeping them on either side of the board.

For ease of use many people link left and right side of the board so voltage and ground are handy on both sides of the center.

![]({{site.baseurl}}/images/Electronic/2/05.png)
Jumpers to make access to +V and G handy
 
# What is a breadboard diagram?
A breadboard diagram is a computer-generated drawing of a circuit on a breadboard. Unlike a circuit diagram or a schematic (which use symbols to represent electronic components; see the Advanced section to learn more), breadboard diagrams make it easy for beginners to follow instructions to build a circuit because they are designed to look like the "real thing." For example, this diagram  shows a basic circuit with a battery pack, an LED, a resistor, and a pushbutton, which looks very similar to the physical circuit:

![]({{site.baseurl}}/images/Electronic/2/06.PNG)


Sometimes,  breadboard diagrams might be accompanied by (or replaced with) written directions that tell you where to put each component on the breadboard. 

# What is a Circuit diagram?
Circuit diagrams, or schematics, are a way to represent a circuit using symbols for each component. Circuit diagrams, as opposed to breadboard diagrams, are used by professional engineers when designing circuits, and they are much more convenient for more complicated circuits. For example, this circuit diagram shows a basic circuit with a battery, a switch, an LED, and a resistor.

![]({{site.baseurl}}/images/Electronic/2/07.png)

However, unlike breadboard diagrams, circuit diagrams only show electrical connections between components. They do not necessarily correspond to the physical layout of the components on a breadboard. 


# Let’s build a circuit
## Basic Pushbutton LED Tutorial
## Step 1
Attach the battery pack to the power and ground rails of the breadboard.
## Step 2
Plug the switch into the breadboard. This picture shows it hurdling the center line but the top and bottom pins are connected when the button is pushed rather than the left and right. This position simply leaves us lots of room to route the other wires.
## Step 3
Insert the LED with the anode (long leg) towards the top of the board.
## Step 4
Insert the resistor into the board with one end in the same horizontal row as the LED’s cathode (short) leg and the other a few rows down. The resistor is not polarized so it does not matter which direction you insert it.
## Step 5
Wire up the positive leads using red jumper wires. Then connect from the positive rail of the breadboard to the same horizontal row as the top leg of the switch. Now connect from the row that houses the bottom leg of the switch to the row that houses the anode of the LED.
## Step 6
Wire up the ground lead from row that houses the bottom of the resistor to the ground rail of the breadboard. Check your work against the diagram below.
![]({{site.baseurl}}/images/Electronic/2/08.png)

Press the button and the LED should light up.  Congratulations, you've assembled your first breadboard circuit.
