---
layout: home
title: Rosmo
subtitle: A small robot.
---

 ![ROSmo tracked](https://pbs.twimg.com/media/FUa95gJXsAEfBqj?format=jpg)

Rosmo is a project to make small openhardware robots for educational and hobbyist use. We aim to design capable robots which can be assembled without soldering. It's a modular set of open-hardware components that can be assembled into robots of different complexity and price. It's all based on ESP32 so should support MicroROS work.

We value modularity. The project started working with the M5stack system. The robot you see above is the culmination of that work. We built a [chassis](https://github.com/rosmo-robot/Rosmo_3D/tree/main/V2/2.10), [ESP32dev board](https://github.com/rosmo-robot/Open-Core-M5stack/tree/main/2.2) and [ESC](https://github.com/rosmo-robot/Rosmo_ESC) in this 5cmx5cm profile. We learnt a lot doing this. Unfortunately the parts crisis has meant that the ESC is not obtainable until at least 2023. We continue to test and develop using the small numnber of ESC boards we have produced.

We also identified some issues with the M5stack system, in partucular the header is hard to obtain at resonable prices.We've therefore pivoted our work to work with the Feather footprint to give a wider array of add-on boards. Whilst the Feather is great it is very small, so we're also working with some slightly larger daughter boards using our own pinout in 6cm x ~5-10cm.

We have some early drafts of this work underway with the [Feather:bit board](https://github.com/rosmo-robot/Feather-Bit/tree/main/v1) the intention is to use this board in two versions of a ~10cm x ~10cm robot.

The first variation is [Rosmo:Bot](https://github.com/rosmo-robot/micro-bot/tree/master/Hardware/V2.11) which uses cheaper brushed motors. 
![Brushed](https://raw.githubusercontent.com/rosmo-robot/micro-bot/master/Hardware/V2.11/v2.11.png)

The second variation will be '[Rosmo:BLDC](https://github.com/rosmo-robot/Rosmo_3D/tree/main/V4/BLDC)' using Brushless motors. We have a chassis and plan to use it initially with a very overpowered [rp2040 ESC](https://github.com/Twisted-Fields/rp2040-motor-controller)

 ![ROSmo BLDC](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/chonky.jpeg)
 
The idea is the Rosmo:Bit PCB can be 'upgraded' by removing the wheels and attaching it to this chassis. It will provide mounting for the Microcontroller, sensors and [daughter boards](https://github.com/rosmo-robot/Feather-Bit/blob/main/v1/daughter_concept/Readme.md). In time we hope to use or develop smaller and cheaper [SimpleFOC driver boards](https://community.simplefoc.com/) that are more suitable for this small robot.

Software wise our intention is to run MicroROS/ROS2 on both the Rosmo:bot and Rosmo:BLDC. Initial work has started using [Linorobot2](https://github.com/rosmo-robot/linorobot2_hardware). We're waiting on a couple of upstream bugs to be fixed before this can progress.

We're also interested in supporting [Smartcar_shield](https://github.com/platisd/smartcar_shield/) firmware on Rosmo:bot

# Tools
* 1x small phillips screwdriver

# Skills
* Mechanical assembly

