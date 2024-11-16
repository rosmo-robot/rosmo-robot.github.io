---
layout: page
title: Build the ROSMO robot
---

Build the ROSMO Robot
---------------

Welcome to the ROSMO robot assembly guide! This guide will walk you through the steps to build your ROSMO robot. By the end, you’ll have a fully operational robot, ready for exploration and experimentation. Whether you’re a beginner or experienced in robotics, this guide will provide all the details you need.
Table of Contents

   
Parts List
--------------

Before you begin, ensure you have all the necessary parts:

[Refer to the homepage](https://rosmo-robot.github.io) for comprehensive list & links to parts
    
Tools Needed
----------- 

You’ll need the following tools:

3mm Hex key (usually provided in M3 nut/bolt kits)
    

Assembly Steps
-----------


Mounting Motors and Wheels
---------

Install Motors: Place each motor into its designated slot on the frame, ensuring the encoder connections face inward.
Secure Motors: Use screws to fasten each motor firmly. 
Attach Wheels: Press-fit each wheel onto the motor shafts, pushing down and forward for a snug fit.

For 2WD configuration it looks like this:

IMG

For For 4WD configuration it looks like this:

IMG


Preparing the Chassis
-------


![]()![image](https://github.com/rosmo-robot/rosmo-robot.github.io/assets/400875/c72a1d5d-9fa8-44ec-a847-4611be88fc95)

The chassis is a two printed circuit boards with the battery sandwiched between. All the essential robot parts simplypress onto the headers to make assembly as simple as possible. You can also 3D print your own parts to attach to the chassis.

Frame Assembly: Start by assembling the two chassis plates. Align the chassis pieces and secure them with the standoffs provided.
This will make mounting other components easier and more accurate.

For 2WD configuration it looks like this:

IMG

For For 4WD configuration it looks like this:

IMG

![](https://raw.githubusercontent.com/rosmo-robot/rosmo/main/Images/V1/battery.jpeg)


Wiring and Connections
------------

Motor Connections: Connect the motors to the designated ports on the chassis.

For 2WD configuration it looks like this:

IMG

For For 4WD configuration it looks like this:

IMG


Installing the ESP32-S3 Processor
--------

Processor Placement: Position the ESP32-S3 processor on the headers. Ensure its mounted in the correct orientation

For 2WD configuration it looks like this:

IMG

For For 4WD configuration it looks like this:

IMG

Adding Sensors
-------------

IMU Sensor: Place the IMU sensor on the top frame section. connect using a Qwiic cable

For 2WD or 4WD configuration it looks like this:

IMG



Testing and Calibration
------------

Initial Test: Power on your robot and check each component (motors, sensors, etc.) for responsiveness.
Motor Alignment: Test the motors to ensure they rotate in the correct direction. Adjust if necessary.


![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/signal-2024-04-05-171808.jpeg)



Getting help
------------
We have set up a [Discord channel](https://discord.gg/8E9g6neBx4) where you can get help from our team as well as members
of the community using Rosmo & the Linorobot ROS2 software.



    
    
