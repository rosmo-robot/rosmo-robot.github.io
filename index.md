---
layout: home
title: Rosmo
subtitle: A small robot.
---

 ![ROSmo tracked](https://pbs.twimg.com/media/FUa95gJXsAEfBqj?format=jpg)

Rosmo is a project to make small openhardware robots for educational and hobbyist use. We aim to design capable robots which can be assembled without soldering. It's a modular set of open-hardware components that can be assembled into robots of different complexity and price. 

We value modularity. The project started working with the M5stack system. The robot you see above is the culmination of that work. We built a [chassis](https://github.com/rosmo-robot/Rosmo_3D/tree/main/V2/2.10), [ESP32dev board](https://github.com/rosmo-robot/Open-Core-M5stack/tree/main/2.2) and [ESC](https://github.com/rosmo-robot/Rosmo_ESC) in this 5cmx5cm profile. We learnt a lot doing this. Unfortunately the parts crisis has meant that the ESC is not obtainable until at least 2023. We continue to test and develop using the small numnber of ESC boards we have produced.

We also identified some issues with the M5stack system, in particular the header is hard to obtain at resonable prices. We've therefore pivoted our work to do more work with the Feather footprint to give a wider array of add-on boards. Whilst the Feather is great it is very small. We made a Feather to Micro:bit converter the [Feather:bit board](https://github.com/rosmo-robot/Feather-Bit/tree/main/v1) the intention is to use this board in two versions of a ~10cm x ~10cm robot.

We also built a small 2WD platform to use it with [Rosmo:Bot](https://github.com/rosmo-robot/micro-bot/tree/master/Hardware/V3) which uses cheaper brushed motors. 
![Brushed](https://raw.githubusercontent.com/rosmo-robot/micro-bot/master/Hardware/V3/Front.JPG)

Currently working on a larger 4x4 platform for both Brushed and Brushless motors. [The Smartcar 2.0](https://rosmo-robot.github.io/aboutme/)
