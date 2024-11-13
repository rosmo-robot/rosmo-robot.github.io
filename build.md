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

    ESP32-S3 development board
    Motors with encoders
    Wheels and mounting hardware
    USB Battery 
    Cables and connectors
    Standoffs

[Refer to the homepage](https://rosmo-robot.github.io) for comprehensive list & links to parts
    
  Tools Needed
  ----------- 

You’ll need the following tools:

    Screwdriver set
    Hex key set
    Pliers
    Tweezers (optional, for handling small components)

Assembly Steps
   -----------
Preparing the Chassis


  ![]()![image](https://github.com/rosmo-robot/rosmo-robot.github.io/assets/400875/c72a1d5d-9fa8-44ec-a847-4611be88fc95)


The chassis is a two-layer design that holds all of the robot components. It is designed
using the Open Robot Platform hole spacing that is designed to make adding additional components easy and without
the need for tools. All the robot parts simply screw onto the chassis to make assembly as
simple as possible. You can also 3D print your own parts to attach to the chassis.

    Frame Assembly: Start by assembling the two chassis plates. Align the chassis pieces and secure them with the standoffs provided.
    Check Stability: Make sure the frame is solid and stable. This will make mounting other components easier and more accurate.

    ![](https://raw.githubusercontent.com/rosmo-robot/rosmo/main/Images/V1/battery.jpeg)


Mounting Motors and Wheels
-

    Install Motors: Place each motor into its designated slot on the frame, ensuring the encoder connections face inward.
    Secure Motors: Use screws to fasten each motor firmly. Ensure all connections are fully seated to avoid loose parts.
    Attach Wheels: Press-fit each wheel onto the motor shafts, pushing down and forward for a snug fit.

Installing the ESP32-S3 Processor
-

    Processor Placement: Position the ESP32-S3 processor on the mounting slot above the motors.
    Secure Processor: Use screws to fasten the processor. Ensure it’s firmly seated and all ports are accessible.

Adding Sensors
-

    IMU Sensor: Place the IMU sensor on the top frame section, securing it with screws.
    Rangefinder: Mount the rangefinder sensor at the front, ensuring it faces forward for accurate distance measurements.

Wiring and Connections
   ------------

    Motor Connections: Connect the motors to the designated ports on the chassis.
    Sensor Connections: Attach each sensor to its respective port, as shown in the wiring diagram.
    Battery: Connect the battery to the USB-C breakout, then plug the breakout into to the chassis

Warning: Double-check all connections before powering on to avoid short circuits.

Testing and Calibration
   ------------

    Initial Test: Power on your robot and check each component (motors, sensors, etc.) for responsiveness.
    Calibrate Sensors: Run the calibration script provided in the software to ensure accurate sensor readings.
    Motor Alignment: Test the motors to ensure they rotate in the correct direction. Adjust if necessary.



![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/signal-2024-04-05-171808.jpeg)






Getting help
------------
We have set up a `[Discord channel](https://discord.gg/8E9g6neBx4) where you can get help from our team as well as members
of the community using Rosmo & the Linorobot ROS2 software.


Further reading
----------------------------

[60019 at Imperial](https://www.imperial.ac.uk/computing/current-students/courses/60019/) has some [Notes online](http://www.doc.ic.ac.uk/~ajd/Robotics/index.html)


This user guide is partly derived from the [XRP User guide](https://github.com/Open-STEM/XRPUsersGuide/tree/main) and is released under the GNU General Public License v3.0
    
    
