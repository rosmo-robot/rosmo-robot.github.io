---
layout: page
title: Build the ROSMO robot
---




Introduction
============

This documentation is very work in progress. 

Rosmo Robot aims to level the STEM playing field globally and create a future generation of STEM innovators 
and technology leaders.

The robot kits are designed to operate autonomously and perform 
basic tasks. Its simple, tool-free assembly means robots can be built quickly, 
As part of this platform, we will provide virtual support through online courses and will guide students 
and teachers through the new system, including the ability to scale up using 
the same hardware with free software updates. 

This user guide is derived from the [XRP User guide](https://github.com/Open-STEM/XRPUsersGuide/tree/main) and is released under the GNU General Public License v3.0


Two robots in one
=================
Rosmo can be used for two different applications:

* A **STEM learning platform using microblocks** with custom tools designed 
  to learn and experiment with robotics. Included is a curriculum to help learn
  about robotics and programming. This use of the Rosmois described in this document.
  
* A robot to introduce new **Students and hobbyists to ROS2 programming** with
  the same tools, languages, and libraries used in professional and industrial robots.
  To learn about using the Rosmo Robot for ROS2, you should refer
  to the `[ROS2 documentation](https://rosmo-robot.github.io/)

Software Tools
==============

There are several software tools available to the programmer for the Rosmo Robot. There are general-purpose tools that will work with the Rosmo.

Programming Languages
---------------------

The Rosmo team currently supports two programming pardigms for the Rosmo Robot

**Microblocks**
![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/microblocks.png)
    A graphical programming system based on Scratch to make
    it easier to start coding your robot without the need to
    the syntax of Python or C+. Internally, a Microblocks program is
    translated to a virtualmachine and saved on the robot. 


**ROS2**
![](https://miro.medium.com/v2/resize:fit:1400/1*V1VzU9uVHSBT9zl8gpiPag.png)
    Python a object-oriented text-based programming language used throughout
    industry and taught in many classrooms. Other languages utilised in ROS2 include C and C++. There are other languages that can also work 
with the ESP32 microprocessor in Rosmo.

Here are some primary features of the Rosmo Robot

•	The default drive function to control speed, direction, and power applied to the four motors. It can handle driving and turning, with and without sensors such as the IMU, for making accurate point turns.

•	The sensors on the robot, such as the motor encoders, rangefinder, reflectance sensor, and IMU (Inertial Measurement Unit), which can get the robot heading and accelerations as it is driving.

•	The WiFi connection so that programs can create a web server on the robot that can be used to display a dashboard on a connected phone, tablet, or computer. It is designed for displaying program status, driving controls for teleoperation, and buttons to run user functions when pressed for more control of user robot programs.

•	Utility functions for sensing, the user buttons, operating the LED, and robot program timing

•	Several small sample programs to help illustrate how the various components are used to operate.



Getting help
------------
We have set up a `[Discord channel](https://discord.gg/8E9g6neBx4) where you can get help from our team as well as members
of the community using Rosmo & the Linorobot ROS2 software.


Building the Rosmo Robot
------------

Assembling the Rosmo robot is easy, but be sure to follow the steps here to be sure that
the wiring is correct and all the pieces are added correctly to the chassis.


The Rosmo Robot kit 
------------

The Rosmo Robotkit contains all the parts you need to assemble and use a basic version of the robot. Alternately a full list of parts is available on the homepage, including a number of optional parts.

 The contents of the kit are shown to help you identify the parts during assembly.

Robot chassis
-----------
  ![]()![image](https://github.com/rosmo-robot/rosmo-robot.github.io/assets/400875/c72a1d5d-9fa8-44ec-a847-4611be88fc95)


The chassis is a single-piece design that holds all of the robot components. It is designed
using the Open Robot Platform hole spacing that is designed to make adding additional components easy and without
the need for tools. All the robot parts simply screw onto the chassis to make assembly as
simple as possible. You can also 3D print your own parts to attach to the chassis.


The robot chassis has headers to mount a ESP32-S3 microprocessor that reads the sensors inputs, runs
the Python or Microblocks program and drives the actuators (motors). You can add additional
components to sense accelerations and headings of the robot, and communicate over WiFi
with your laptop or phone.


Assembling the Rosmo Robot
========================

Assembling the Rosmo robot can be done with a small flat head screwdriver. The total process should take about 25 minutes, especially once you
understand how it goes together.

Each of the following sections has a time reference for the video at the top of this page so you
can see how to assemble that part. We suggest that you view the entire video before starting the
assembly so you can get a good overview of how it goes together.

Inserting ESP32 into the chassis (1:18)
------------------------------------------------------
Insert the ESP32-S3 into the chassis as shown in the following picture.
Observe the orientation of the board where the USB connections are towards the left of the
robot as shown.

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/signal-2024-04-05-171808.jpeg)

Then push down and foward on the back edges of the board so that the front corners
are completely seated in the female headers





Adding the motors
-----------------
The  motors  include encoders (sensors to measure wheel rotation) to
make it easy to program the robot to drive for specific distances and speeds. This will give your
robots more control and accuracy as your are writing progams to operate it.

Installing the motors into the chassis (4:09)
---------------------------------------------

The motors screw into the chassis from the bottom once the wheels and cables are installed. T
.
Ideally you should push the wires from the motor through the opening in the chassis to the top of the
chassis so they can be attached to the Motor driver. Then seat the end of the motor opposite the
cable end, then snap the wheel side of the motor into place. Repeat for both motors.


Putting the wheels onto the motors (3:22)
-----------------------------------------

The wheels press fit onto the  motor shafts. Notice that the motor shafts have two flat sides
that correspond to the flat edges in the center of the wheel. The wheel is pressed over the
motor shaft so that the center part of the wheel that sticks out is closest to the motor body and
that the wheel is pressed all the way onto the motor shaft.

   

Connecting the motor cables & encoders to the chassis
------------------------------------------------
The motor cables connect the motor to the Motor driver so that it can drive the drive the motors

The ESP32-S3 microcontroller must receive data from the motor encoder sensors that provide position and speed information for
your robot program. This encoders all the robot to drive at a desired speed and drive for a desired
distance.

    

Photo of the Breakout headers
-----------------------------
Many of the following instructions require attaching cables to the connectors on the
Breakout headers on the robot. The printing on the board identifying the purposes of
each of the connectors and the pins is very small to fit on the small board. To make
assembly easier, refer to the following photograph of the board if needed.




Installing the battery pack (1:39)
----------------------------------
The battery pack is installed by placing it on the bottom PCB plate and attaching the bottom and top plates together with hex spacers, gently squeezing the battery between the two plates

![](https://raw.githubusercontent.com/rosmo-robot/rosmo/main/Images/V1/battery.jpeg)



Attaching the IMU (optional - recommended) (5:11)
------------------------------------------------
The IMU board is connected to the  as shown in the picture
The connectors simply push over the sensor pins. Be sure that they are fully seated as shown in the picture and video
to ensure a good connection.

The servo is a special type of motor such that when programmed with a position
the shaft will automatically move to the specified angle. This is used to power the arm
on your robot it can move to predetermined angles all by itself.


Wiring the line following sensors (optional) (5:11)
------------------------------------------------
The line following sensor can detect lines on the driving surface that have a different reflectivity.
These are typically used in robot applications to follow lines or locating interesting places on a
board or mat. It has two pairs of LEDs and photo sensors to emit infrared light and measure the
reflected brightness.

The sensor board is connected to the line following (reflectance) sensor as shown in the picture
below. Be sure to observe the order and color of the wires connecting to the sensor. The connectors
simply push over the sensor pins. Be sure that they are fully seated as shown in the picture and video
to ensure a good connection.


Wiring the ultrasonic distance sensors (optional) (5:11)
------------------------------------------------

The ultrasonic rangefinder uses sound to measure the distance to objects in front of the sensor.
An ultrasonic (inaudible high frequency) short sound is sent from one of the transducers which
is reflected back by nearby objects and received by the second transducer. The time of the
sound round-trip is measured to determine distance to nearby objects.

There are two approaches to distance sensors  wired by attaching the four wires from the sensor cable to the pins on the rangefinder
as shown in the picture below. Be sure to connect the wires to the pins in the right order.


        
Wiring the laser distance sensors (optional) (5:11)
------------------------------------------------
There are two approaches to distance sensorsis wired by attaching the four wires from the sensor cable to the pins on the rangefinder
as shown in the picture below. Be sure to connect the wires to the pins in the right order.

    .. image:: assembly/reflectance_with_wires.jpeg
        :width: 200
        :alt: Reflectance sensor with wires attached



Attaching the Lifting bucket (Optional)
-------------------
The servo is used to rotate the arm to the desired position. It has the advantage
over a normal motor in that it has sensors inside of it to allow it to move to
a desired position that you can program.


Attaching the grabber claw (Optional) (7:29)
-----------------------------------------------------------
The servo is attached to the robot by first inserting the ball end of the bracket into the upper
slot on the back rail, then snapping the bottom part of the bracket over the bottom part of the rail.

    .. image:: assembly/ball_end_of_servo.jpg
        :width: 200
        :alt: Inserting the ball end of the servo bracket into the slot into the top slot on the chassis rail

    .. image:: assembly/top_servo_bracket.jpg
        :width: 200
        :alt: Pushing the bottom part of the servo bracket over the bottom part of the chassis rail

Attaching the Lidar (Optional and only supported when using ROS2)
----------------------------------------------
The servo snaps into the servo bracket as shown in the photo below.

    .. image:: assembly/servo_on_bracket.jpg
        :width: 200
        :alt: The servo mounted in the bracket ready to snap onto the robot


Troubleshooting the robot build
===============================
Generally the build of the robot is very strightforward, but from feedback we have compiled this section
that describes some of the common issues we have seen as people are building Rosmo.



Driving
=======

Robot driving
-------------
The Rosmo Robotis a mobile robot platform where driving from one place to
another is central to the design of any program. The
differential_drive class makes driving easy and has functions to:

* **Set the motor efforts**, which is the power or average voltage
  applied to the motors. The range of values can be set from -1 for
  full effort in reverse, to 0 for no voltage or stopped,
  to +1 for full effort in the forward direction.

* **Specify a speed to drive** in centimeters per second for each wheel.
  The robot will try to maintain the specified speed as best it can
  using the drive motor encoders.

* **Drive for a specified distance** using the drive motor encoders to
  sense how far the robot has traveled.

* **Make point turns** for a desired number of degrees, either clockwise
  or counterclockwise.

Effort vs. Speed
----------------
Throughout this document, we refer to the effort and speed of the
drivetrain. Although they seem similar, they are distinguished as
follows:

**Effort**
    The effort reflects the amount of power (or average voltage)
    supplied to the motors. For a given effort, the speed will
    vary depending on things like the driving surface, the
    battery voltage, and the slope (either flat, uphill or downhill).

**Speed**
    The speed is the actual number of centimeters per second that
    the robot will travel. When set in a program, the software will
    automatically adjust the motor effort within its capability to
    keep the robot moving at the desired speed.

Driving for a distance
----------------------
The following program fragments show how to program the robot to drive forward for 10 centimeters with an effort of 0.5 or 50 percent power. This function uses the encoders to determine when the robot has traveled the requested 10cm. In addition, this function will ensure that the robot drives in a straight line by varying the speed of the left or right motors if one is slightly faster.


Driving with an effort
----------------------
This program will set the effort on the left and right drive motors
to 50 percent, wait for 3 seconds, and stop the motors. The
set_effort() function has parameters for the left and right
drive motors to allow them to be set independently. No motor speed
control is provided, so different driving surfaces, slopes, or
battery voltage will affect the driving speed of the robot.
The value of effort ranges from -1 for 100 percent backward to
0 for no effort or stopped to +1 for 100 percent effort forwards.

.. image:: images/Picture8.png
    :width: 400

.. image:: images/Picture6.png
    :width: 300


Driving at a speed
------------------
Set_speed() attempts to maintain some linear speed in centimeters
per second. The maximum speed is measured to be approximately 
60cm/s tested on a flat surface.

This program will set the robot speed to 5 cm per second, in
centimeters per second, of the left and right wheels separately.
If both motors are set to the same speed, the robot will drive
straight. If they are different, the robot will turn in a direction
away from the faster wheel.

.. image:: images/Picture7.png
    :width: 300

.. image:: images/Picture7b.png
    :width: 300

Point turns
-----------
.. image:: images/PointTurn.gif
    :width: 300

The robot can turn in place around a point directly centered between 
the two drive wheels. This is done by driving the left and right drive
motors in opposite directions at the same speed. If the left wheel is
spinning in the forward direction, the robot will rotate clockwise
or to the right. If the right wheel is spinning in the forward
direction, the robot will rotate counterclockwise or to the left.

The turn function specifies the number of degrees to turn, with a
positive number indicating a counterclockwise turn, and a negative number
indicating a clockwise turn. The second parameter specifies effort from
-1 to 1.

.. image:: images/Picture9.png
    :width: 300

.. image:: images/Picture10.png
    :width: 300

When you use the turn function, the IMU (Inertial Measurement Unit)
gyro sensor on the robot will determine when the robot has completed
the requested turn. This means the turn will continue until complete
and is not affected by wheel slip. 

.. note:: 
    If you were to pick up the robot while it is doing a turn,
    the wheels will continue turning until the gyro senses that the
    robot has turned the desired number of degrees.

Swing turns
-----------
This type of turn is where one wheel moves forward, and the other
is stationary. The robot will pivot on the stationary wheel,
making it the center of rotation. The circle's diameter traveled by
the moving wheel will be twice the wheel track (the distance between
the two wheels).

.. image:: images/SwingTurn.gif
    :width: 300

Smooth turns
------------
Smooth turns are where the two wheels move in the same direction
so that the robot drives in an arc, eventually completing a full
circle. The circle's radius depends on the speed difference between
the two wheels. The larger the difference, the smaller the circle
diameter.

.. image:: images/SmoothTurn.gif
    :width: 300



    Motors
======
Motor classes
-------------
The Rosmo Robot has two or four drive motors connected to the ports Motor 1 and
Motor 2 on the Motor driver board. The board also supports
two additional motors labeled Motor 3 and Motor 4. These motors
can be used to create additional mechanisms for the Rosmo.

There are four classes related to motors:

**Motor**
    The motor class handles a single motor with a single method
    for setting the effort between -1 and 1.

**Encoder**
    The encoder class is responsible for measuring the current position
    of a motor. This is useful to derive the speed of the motor, or the
    distance traveled by the motor.

**EncodedMotor**
    Encoded motors contain a motor and an encoder, and has higher
    level logic for functionality that incoporate both objects.
    This class supports features like resetting and getting the motor
    position, setting the effort and speed of the motor, and configuring
    what controller is used for closed-loop speed control.

**MotorGroup**
    It is often desirable to treat several motors as if they
    were one. For example, in a four wheel drive robot, the
    left side motors usually get the same settings when driving
    the robot. A motor_group is created with multiple motors, and
    functionality like setting effort can be applied to all the motors
    in the motor group.

Since the Rosmo Robotbot is built with an encoder on each motor, it usually
is not necessary to directly deal with Motor or Encoder objects.
Instead, use EncodedMotor or MotorGroup for higher level functionality.

Using EncodedMotor
------------------
Interacting with EncodedMotor objects is often the most convenient way
to control motors on the Rosmo. The RosmoLib.defaults module provides two
ready-made EncodedMotor objects, left_motor and right_motor, which
allow for fully independent control over the drive motors of the robot.

There are four motor controllers total on the Rosmo, numbered 1-4. 
1 and 2 are the left and right motors, and 3 and 4 are labeled
on the Motor driver board. left_motor and right_motor objects
are provided by default in the RosmoLib.defaults module. Let's take
a look at how we can use the left_motor object to set the left motor
to an effort of 0.75.

.. image:: images/PictureLeftMotor.png
        :width: 300

.. image:: images/LeftMotor.png
        :width: 300

Alternatively, you may also construct your own EncodedMotor objects,
which is needed to control motors 3 and 4. The following code sets
Motor 3 to an effort of 0.75.

.. image:: images/PictureMotor3.png
        :width: 300

In Microblocks, constructing motor objects is not necessary. Under the
"Individual Motors" category, each block takes in a parameter to specify
which motor to use. This is all that is needed to set Motor 3 to an effort
of 0.75 in Microblocks:

.. image:: images/PictureMotor3Microblocks.png
        :width: 300

Methods for EncodedMotor objects
--------------------------------

**set_effort(effort_value)**

As seen earlier, this method spins the motor at some raw effort. The
effort value ranges from -1 to +1, where negative efforts spin the
motor in reverse, and positive efforts spin the motor forwards. An
effort of 0 stops the motor.

.. image:: images/Wheel.png
        :width: 300

The programs shown below set Motor 3 to 80 percent effort for 5
seconds, then afterwards, back to 0 percent effort to stop the motor. 
This example uses motor 3, but any motor can be used in its place.

.. image:: images/Picture12.png
    :width: 300

.. image:: images/Picture13.png
    :width: 300


**set_speed(speed_rpm)**

Unlike the Drivetrain object which uses cm/second, the motor objects handle speed in rotations per minute. 
They reads from the encoder to determine the current speed, and adjust
based on a closed-loop controller, which by default is a PID controller.
Similarly to set_effort(), the sign of the speed determines the direction
of the motor.

The example programs below set a speed of 60 rpm for the left motor:

.. image:: images/PictureMotorSpeed1.png
    :width: 300

.. image:: images/PictureMotorSpeed2.png
    :width: 300

**set_speed_controller(controller)**

The set_speed() function relies on a controller to determine how to vary
the effort of the motor to maintain the specified speed. By default, the
controller is a PID controller, but it can be changed to any object that
implements the Controller abstract class.

The example below sets the speed controller with custom PID tunings. For
more information on controllers, refer to the page under Miscellaneous Topics.
Currently, there is no support for custom controllers in Microblocks.

.. image:: images/PicturePID.png
    :width: 300

.. image:: images/motorcommands.png
    :width: 300

**get_speed() -> float**

Returns the current speed of the motor in rotations per minute, as measured
by the encoder.

**get_position() -> float**

Returns the current position of the motor in rotations, as measured by the
encoder.

**get_count() -> integer**

Returns the current position of the motor in encoder counts, as measured by the
encoder.

**reset_encoder_position()**

Resets the encoder counts to 0. get_position() and get_count return the difference in
distance since the last reset.

Sensing the environment
=======================

.. image:: images/DevBoard.png
    :width: 300

Measuring the distance to an object
-----------------------------------
The Rosmo Robotincludes an ultrasonic rangefinder that can measure the
distance to objects in front of it.  The sensor has two transducers;
one acts as a speaker, and the other acts as a microphone. It does
it by sending a burst of ultrasonic sound out of the speaker that
hits an object in front of the robot. The sound reflects off the
object back to the sensor and is captured by the microphone. The
time for that round trip determines the distance to the object.
Understanding how well the sound reflects off various objects of
different sizes, profiles, and materials is important for using
the sensor. A good exercise is to test the sensor by printing
returned values at various distances from any object you want the
robot to detect.

.. image:: images/Ultrasonic.jpg
    :width: 300

.. note::
    It is important to wire the sensor correctly, as described in
    the assembly instructions, to ensure it works properly.
    Interchanging the trigger and echo wires is a common
    error using that part.

RosmoLib has a rangefinder class that takes care of the sending and
receiving signals to the sensor. All the program has to do is request
the distance, and the library returns it. There is a single method
called distance() that returns the distance to the nearest object
in centimeters. The range of operation is from 2cm to 4m.

Example use of the rangefinder
-------------------------------
The following program drives the Rosmo Robotforwards until the code
detects an object within 10cm of the ultrasonic rangefinder.
Then it stops.  

.. image:: images/Picture15.png
    :width: 300

.. image:: images/Picture16.png
    :width: 300

This program stops the motors when the object is detected. A
better way of solving the same problem might be to use proportional
or PID control to gradually bring the robot to a stop to avoid
overshoot, where inertia might carry the robot beyond the 10cm
set point before it comes to rest.

Following lines
---------------

.. image:: images/LineFollower.png
    :width: 300

.. image:: images/RobotFront.png
    :width: 300

A reflectance sensor that can be used for line following is included
with the Rosmo. It has two pairs of LEDs and light sensors. The LEDs
emit infrared light that reflects off the driving surface. The light
sensor measure the reflected light intensity, which depends on the
surface below the sensor. Electrical tape is typically used to make
a line that the robot can follow and has a different reflectivity
than the surface, usually a whiteboard or tabletop. With a pair of
sensors, the robot can read the reflectance value and tell where it
is relative to the taped line.

The class reflectance has methods get_right() to retrieve the
right reflectance value and get_left() to retrieve the left
reflectance value. The reflectance ranges from 0 (white) to 1 (black).

Line following example program
------------------------------
The following program uses proportional control with the line
sensors to follow a line across the driving surface for the robot.
The Kp variable sets the gain for the controller.

.. image:: images/Picture19.png
    :width: 500

.. image:: images/PictureLinePython.png
    :width: 400

.. image:: images/linefollowing.gif
    :width: 300


    Using the arm
=============

Setting up the arm on the servo
-------------------------------
The servo motor used to attach the arm on the Rosmo Robothas about 200
degrees of rotation and can move to a desired position using
internal sensors. When attaching the arm to the servo, it is
important that one end of its range is with the arm relatively
horizontal inside the robot chassis and the other end of the
rotation outside the back of the robot for picking up objects.
The full range of arm rotation is shown in the two images below.

.. image:: images/ArmIn.png
    :width: 300

.. image:: images/ArmOut.png
    :width: 300

To position the arm correctly, install it in any position and use
it to rotate the servo to the full clockwise direction, as seen in
the top photo. Then reinstall the arm so that it is in the shown
position. Then the software will be able to move it to any position
in between the two photos above.

Moving the arm under program control
------------------------------------
Use the servo class to move the servo motor to the desired position.
The method set_angle() sets the servo position to the desired angle.
Below is an example program that moves the servo position from one
end of its motion to the other.

.. image:: images/Picture22.png
    :width: 300

.. image:: images/Picture23.png
    :width: 300

Further reading
----------------------------

[60019 at Imperial](https://www.imperial.ac.uk/computing/current-students/courses/60019/) has some [Notes online](http://www.doc.ic.ac.uk/~ajd/Robotics/index.html)
    
    
When the servo is controlled from the program, it is held in the
position it was last set to. To free it, that is to allow it to be
moved by hand, the free() function may be called, and the program
will stop sending the position signal to the servo.
