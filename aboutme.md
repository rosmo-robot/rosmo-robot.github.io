---
layout: page
title: Projects
---
## Smartcar 2.0 (In development)

The 'Modules' board v1 is for Pi Pico/ Waveshare ESP32-S3, It stacks on top of the Motors board using two of the common 40pin stacking headers. 

 ![Dual driver concept](https://raw.githubusercontent.com/rosmo-robot/smartcar_shield/master/extras/images/45smartcar.jpeg)


 ![Dual driver concept](https://raw.githubusercontent.com/rosmo-robot/smartcar_shield/master/extras/images/front-smartcar.jpeg)


 ![Dual driver concept](https://raw.githubusercontent.com/rosmo-robot/smartcar_shield/master/extras/images/pcb.jpeg)


Licence: CERN-OHL-P

## V1 Features;
 
 * Mounting space for Pi, Jetson Nano/orin carrier, OrangePi5, [AI-64](https://beagleboard.org/ai-64) or similar
 * Use of [MicroMod MCU](https://www.sparkfun.com/micromod#processor_boards)
 * Use of 3s LifePO4/ Lipo batteries
 * Dual motor drivers for 4x4/ mecanum drive
 * [UEXT socket](https://www.olimex.com/Products/Modules/)
 * [mikroBUS sockets](https://www.mikroe.com/mikrobus-shuttle-127mm-2x8-pin-box-header-smd-male)
 * I2C/ SPI connectors using [Breakout Garden](https://shop.pimoroni.com/collections/breakout-garden), [Qwiic](https://soldered.com/categories/easyc-2/)

## Target software

  * [Microblocks](microblocks.fun/)
  * [Micropython](https://github.com/Open-STEM/XRP_MicroPython)[mecanum](https://thepihut.com/blogs/raspberry-pi-tutorials/build-a-raspberry-pi-pico-robot-with-mecanum-wheels)
  * [Arduino](https://github.com/rosmo-robot/smartcar_shield)
  * [ROS2](https://robofoundry.medium.com/running-linorobot2-hardware-based-on-micro-ros-on-esp32-wroom-32d-using-wifi-transport-d971026f3e08)


[Read more](https://github.com/rosmo-robot/smartcar_shield)




## History of Rosmo project


![ROSmo tracked](https://pbs.twimg.com/media/FUa95gJXsAEfBqj?format=jpg)



We value modularity. The project started working with the M5stack system. The robot you see above is the culmination of that work. We built a [chassis](https://github.com/rosmo-robot/Rosmo_3D/tree/main/V2/2.10), [ESP32dev board](https://github.com/rosmo-robot/Open-Core-M5stack/tree/main/2.2) and [ESC](https://github.com/rosmo-robot/Rosmo_ESC) in this 5cmx5cm profile. We learnt a lot doing this. Unfortunately the parts crisis has meant that the ESC is not obtainable until at least 2023. We continue to test and develop using the small numnber of ESC boards we have produced.

We also identified some issues with the M5stack system, in particular the header is hard to obtain at resonable prices. We've therefore pivoted our work to do more work with the Feather footprint to give a wider array of add-on boards. Whilst the Feather is great it is very small. We made a Feather to Micro:bit converter the [Feather:bit board](https://github.com/rosmo-robot/Feather-Bit/tree/main/v1) the intention is to use this board in two versions of a ~10cm x ~10cm robot.

We also built a small 2WD platform to use it with [Rosmo:Bot](https://github.com/rosmo-robot/micro-bot/tree/master/Hardware/V3) which uses cheaper brushed motors. 
![Brushed](https://raw.githubusercontent.com/rosmo-robot/micro-bot/master/Hardware/V3/Front.JPG)



