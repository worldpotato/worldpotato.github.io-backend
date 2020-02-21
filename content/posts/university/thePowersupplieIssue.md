---
title: "The powersupply issue"
date: 2020-02-13T23:34:40+01:00
draft: false
tags: ["Nvidia TX2", "Student life", "Turtlebot2", "ROS", "Ubuntu"]
---

There is one story I need to tell you.
At a university project my team and I worked with a Nvidia TX2 board.
Our mission was to flash Ubuntu 18.04 on the TX2 board, install ROS Kinetic and control an oldish Turtlebot2.
The problem with this setup is that ROS Kinetic does not support the Turtlebot2 anymore.  
But sometimes you have luck and someone created a [github repository](https://github.com/gaunthan/Turtlebot2-On-Melodic) with everything you need.
That means we only need to flash the newer Ubuntu and install all dependencies.
Of course we also did some investigations how it is done and so on.
Every thing went fine at the first of our two robots. That was like in the middle of the semester.

What append then was not nice.
The micro-usb port on the second TX2 which is needed to flash the ubuntu broke away from the PCB.
Which forced us to ask in our soldering labour if they can help us.
Luckily they agreed, but the bests soldering experts struggled with that task.

After discussing with the professor we got a new board and tried to flash a new ubuntu on it.
But the recovery mode doesn't want to start.
We tried everything to force the recovery mode.
But nothing helped.
Until I used an external power supply instead of the roboter as power supply.

And it worked perfectly.
But can you imagine that the power supply prevents you from entering the recovery mode?

