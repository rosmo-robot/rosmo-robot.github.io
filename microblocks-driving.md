Robot Driving: Module Overview
==============================

In this module students will:

* Learn how to make the robot drive at different speeds
* Understand the relationship between the wheel speeds and the robot's motion
* Be introduced to motor encoders and how to use them to measure the robot's movements
* Learn about the built in driving functions which help make complicated motions easy


At the end of this module, students will be able to...

* Make the robot drive in straight lines, turn corners, and turn in place
* Write and use basic functions in the Python programming language
* Use different types of loops in Python
* Break down a large, repetitive movement sequence into components and then convert into code

Understanding Your Robot's Drivetrain
=====================================

Introduction
------------

The main body of your Rosmo is called the *drivetrain*. We call it this because it
holds the two wheels which drive your robot around. Specifically, the Rosmo has a 
*differential drivetrain*. This is the same kind of drivetrain that you would 
see on a skid-steer loader. 

.. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/skidSteerLoader.png)
  :width: 300

.. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/RosmoImage.jpeg
  :width: 300

The Rosmo robot turns using skid-steering which means that while the robot is turning
some of the wheels, sometimes the front casters, will be skidding. This requires
more energy to complete the turns and depends on the friction of the front casters
and the particular driving surface.

Each wheel of your Rosmo's drivetrain has a motor attached to it. We can use code 
to tell this motor what we'd like it to do. Getting the robot to move in a desired
path is done by setting the speeds of the two drive motors. There are a lot of
variations in how these motors can be set. Here are some basic examples:

Driving straight
----------------
The most fundamental common driving that the robot will do is traveling straight.
To do this, both wheels move forward at the same speed so that
the robot moves straight.

.. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/forwardsdriving.png)
  :width: 300

Turning in an arc
-----------------
Robots can turn in an arc-shaped turn, where one wheel drives faster than the other,
causing the robot to turn away from the faster wheel. As the difference in speed
between the two wheels increases, the turn tightens. If the turn continues, the robot
will drive in a complete circle. In this case, the radius of the circle decreases
as the wheel speed differences increase.

.. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/arcturn.png)
  :width: 300

Turning in place
----------------
One advantage the Rosmo has over a car steering system is that it can turn in place
where the robot turns on a point roughly between the two wheels. This
allows the robot to easily get out of tight spaces without having to make a wide
arc turn. The point turn is often used for navigating the robot between two places
since it follows an easily predictable path.

.. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/pointturn.png)
  :width: 300

Turning on one wheel
--------------------
If one wheel drives forward or backward, and the other wheel remains stopped, the
robot will turn in place, with the turning center being the stationary wheel. This
is often called a swing turn because the robot swings around the non-moving wheel.
With a swing turn, the diameter of the circle traced by the outside wheel is
double the wheel track.

.. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/swingturn.png
  :width: 300



Effort
------

There are several ways we can tell the motors what to do. The most basic thing 
we can control is the *effort* the motor should be applying.

Imagine you are riding a bike on a flat surface, pedalling at a normal speed. 
Now imagine you encounter a hill. If you keep pedalling at the same speed, you
won't slow down when you go up the hill. However, this is not easy! You'd need 
to pedal *harder* to go the same speed up the hill.

Now instead imagine that when you get to the hill, you keep pedalling as hard as 
you were on the flat section. You'll go up the hill slower, but you won't be as 
tired. This is what we mean by the *effort* of the motor. You're not telling the
motor how fast it should move, but rather how hard it should work. If you tell 
your robot's motors to work at a constant effort, your robot's speed will change
depending on whether it is driving on a flat surface or an inclined one.

.. youtube:: z6aIVpf3qN0

.. youtube:: Zcr83kcO_Pk

In both videos, the robot is using the same effort. In the first video, the robot is slowly moving uphill because gravity is fighting against
its effort. In the second video, the robot is moving quickly downhill because gravity is working in the
same direction as the effort. The force output from the motors is the same, but the speed will depend on
resistance to the force.

.. tip:: 

    Effort is also like the throttle in a car. If you're going up a hill, you 
    need to push the throttle more to maintain the same speed on the hill. If 
    you don't push the throttle more, you'll slow down.

First movements
---------------

.. note:: 

    Elevate your Rosmo on top of a box or other object so that the wheels aren't touching anything and can spin freely.

Before driving the robot around, let's write some simple code to spin one of the
wheels. This will help you get familiar with the Rosmo programming environment and
check that your Rosmo itself is working properly.

.. admonition:: Try it out

    Create a new file in the IDE called :code:`spin_wheels.py`. Add the 
    following code to it:

    .. code-block:: python

        from RosmoLib.defaults import *

        left_motor.set_effort(0.5)

    Run the code and see what happens.

Let's break down the code line by line:

:code:`from RosmoLib.defaults import *` tells your robot to load code from 
**RosmoLib**. Don't worry too much about what all the commands in this line mean 
right now, just know that you'll put this line at the top of most of your Rosmo
programs.

:code:`left_motor.set_effort(0.5)` uses a *function* provided for you in **RosmoLib** 
called :code:`set_effort` that is applied to the left motor. The :code:`0.5` is a *parameter* to 
this function which tells it that we'd like the motor to apply 50% effort. 
On the Rosmo, we write percentages as decimal numbers between 0 and 1, with 1 being 100%.

.. Explain functions in greater depth later on (pinwheel activity?)
.. A *function* is a block of code that can be used multiple times in your program
.. to make complicated tasks easier. For example, the
.. :code:`left_motor.set_effort()` function tells the left motor to apply an effort
.. you as the programmer specify.

.. :code:`left_motor.set_effort` is a function that we provide for you in
.. **RosmoLib**. Later in the course you will see how you can write your own
.. functions to make it easy to make the robot do complicated sequences of actions.

.. When you want to use a function, you *call* it by writing its name in your code.
.. This causes the function's code to start running.

.. The number you put between the parenthesis is a *parameter* (sometimes also
.. called called an *argument*) of the function. These allow you to tell the
.. function how it should do its job. As the programmer, you must provide a *value*
.. for each *parameter*. If we wanted to make the robot drive forwards at full
.. speed, we would *call* the function like this:

Now that we've tested the left motor, let's test the right one! How do you think
you would modify the code to spin the right motor? Simply replace
:code:`left_motor` with :code:`right_motor`.

.. admonition:: Try it out

    Modify your code and run it on the robot. Make sure the right wheel spins.
    
    Push an object like a pencil against the wheel to add some resistance.
    Notice how the wheel slows down when you do this, since it would need more
    effort to keep going the same speed.


Going backwards
---------------

We've gotten the wheels spinning forwards, but what if we want to go backwards?
To do this, we simply have to pass in a *negative* number for the effort
parameter. This means that we can use any number between -1 and 1 for the effort
value. -1 will be full effort backwards, 1 will be full effort forwards, and 0 
will stop the motor.

.. admonition:: Try it out

    Try to write code that makes both wheels spin backwards.

This table shows some different effort values and what the wheel would do:

.. list-table::
   :header-rows: 1

   * - Speed value
     - Wheel action
   * - 1
     - Wheel spins forwards at 100% effort
   * - 0.5
     - Wheel spins forwards at 50% effort
   * - 0
     - Wheel stops spinning
   * - -0.5
     - Wheel spins backwards at 50% effort
   * - -1
     - Wheel spins backwards at 100% effort
    

Getting the Robot Moving
========================

Basic driving
-------------

In the last lesson we learned how to set the effort of each of your robot's 
motors individually. Since both of the motors make up the robot's drivetrain,
there's an easier way to write code to move the robot.

.. note:: 

    For this lesson, put your Rosmo on a flat surface like a table or the floor.

Getting your Rosmo robot to move is simple! Here is some code you can use to drive both the left and right motors at 50% 
effort:

.. tab-set:: 

    .. tab-item:: Python

        .. code-block:: python

            from RosmoLib.defaults import *

            drivetrain.set_effort(0.5, 0.5)

    .. tab-item:: Blockly

        .. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/seteffortexample.png
            :width: 300

:code:`0.5` and :code:`0.5` are the parameters of the function.
The functions you used before only had one parameter, but functions can have as
few or as many parameters as you want, or even none at all.

.. hint:: 

    Parameters are inputs to a function that can dictate attributes like distance or angle to vary its behavior.


.. admonition:: Try it out
    
    Add the code to your program to see your robot drive.

    Try using different values to make the robot move at different speeds. What 
    happens if you use different values for the left and right wheels?

    Afterward, place the robot on a ramp and run it again. Take notice of how
    the robot moves slower when on the ramp. Why does this happen?

You may notice that your Rosmo does not drive perfectly straight even though you 
used the same effort value for both motors. This is because the motors on the 
Rosmo aren't perfect. Every motor is a little bit different. Some of them have 
more friction inside them than others. In the next module we'll learn some ways 
to solve this problem so your robot goes straight every time.


Driving a Distance
==================

Controlling your speed
----------------------

In addition to setting the effort of the drivetrain's motors, we can also set 
their *speed*. Remember, effort is not the same as speed. We can also ask the 
Rosmo's motors to go a certain speed. When using this function, the Rosmo will
actively measure the speed of the wheels using the motor's *encoder*. If the 
speed falls too low, the motor will automatically increase the effort it applies
to speed back up.

.. tip:: 

    Don't worry if you've never heard of an *encoder*. We'll talk more about 
    them later in the lesson.

To set the speed of the drivetrain motors, we use a new function:

.. tab-set:: 

    .. tab-item:: Python

        .. code-block:: python

            from RosmoLib.defaults import *

            drivetrain.set_speed(5, 5)

    .. tab-item:: Blockly

        .. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/setspeedexample.png
            :width: 300

This tells the drivetrain to set the speed of each drivetrain wheel to travel at
5 centimeters per second. This means if you put the robot down and let both motors
drive at this speed, the robot would move 5 centimeters forwards each second.

.. admonition:: Try it out

    Add the code to your program and run it. Try the same exercise of pushing 
    something up against the wheels of your Rosmo. Notice how as you add 
    resistance, the motor will increase its effort to keep the speed constant.
    When you remove the resistance, the effort will go back down.

Since both wheels are now going the same speed, your robot should now also drive
straight, unlike when using the :code:`set_effort` function.

.. tip:: 
    
    If you want the robot to go backwards, use a negative speed value just like
    you did with the effort value.

Driving a distance
------------------

We know that we can ask the wheels to spin at a certain speed using a function, 
but what if we want to make the robot drive a certain distance?

We could ask the robot to move at some speed, and if we know how far it will 
move each second (for this example we are using a speed of 5 cm/s), we can calculate
how many seconds we should drive for to reach that distance.

Let's use :math:`d` to represent the distance we want to drive in cm. But, we want
a number in seconds, so we need to convert by the means of *dimensional analysis*.

To do this, write an expression for the known value with units included:

.. math::
    (d  \text{ cm})

Dimensional analysis involves multiplying this expression by special representations
of "1" to convert units. In this case, our speed is 5 cm per second, so we can equate
:math:`5 \text{ cm} = 1 \text{ second}`. Rearranging, we have our special representation of 1:

.. math:: 

    \frac{1 \text{ second}}{5 \text{ cm}} = 1

We can now multiply our expression with this special representation of 1:

.. math::
    (d \text{ cm}) \cdot \frac{1 \text{ second}}{5 \text{ cm}}

Cancelling out units and simplifying, we obtain:

.. math::
    (d  \cancel{\text{ cm}}) \cdot \frac{1 \text{ second}}{5 \cancel{\text{ cm}}} = \frac{d}{5} \text{ seconds}


This resultant expression makes sense! If we want to go 5 cm, we plug in d = 5, and :math:`\frac{5}{5} = 1`,
so we drive for one second. If we want to go 2.5 cm, we plug in d = 2.5, and :math:`\frac{2.5}{5} = 0.5`,
so we drive for half a second.

Keep in mind that this equation is only valid if the robot is moving at 5 cm per
second. If you change that speed to be faster or slower, you'll need to change
the denominator of the fraction to that speed to fix the equation.

.. admonition:: Try it out

    Calculate how many seconds you need to drive for to go one meter if your 
    robot is moving at 5 cm per second. Remember, there are 100 cm in a meter.

To put the above theory into practice, we need to learn about a new function in Python: 
:code:`sleep`, which makes the Rosmo wait for some number of seconds before 
continuing to the next instruction in the code.

.. tab-set:: 

    .. tab-item:: Python

        .. code-block:: python

            from RosmoLib.defaults import *
            from time import sleep # We need to import the speed function to use it.

            drivetrain.set_speed(5, 5)
            sleep(x) # replace x with the time you calculated to go one meter.
            drivetrain.stop() # This is another function which makes it easy to stop the robot


    .. tab-item:: Blockly

        .. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/setspeedandsleep.png
            :width: 300

.. tip:: 
    
    The :code:`#` symbol in Python creates a *comment*. If you add one to a line
    of code, anything that comes after it on that line will be ignored by the 
    robot. You can use it to leave notes for yourself, or to quickly disable a 
    line of code while debugging problems.

    We use comments in our examples to give you hints about how to write your
    code. You don't need to copy our comments into your code, but you should
    write your own so that you can easily remember what your code does.

.. admonition:: Try it out

    Add the code to your program and try it out. Remember to replace :code:`x` 
    with the value you calculated. Try running your robot next to a meter stick
    to see how accurately your robot drives!

This code you wrote is pretty useful, but what if you wanted to drive other 
distances?

Let's say that we want to drive three distances in a row: 25, 50, and 75 cm.
How could we program the robot to do this? The easy solution is to copy and 
paste the code you wrote before three times, and modify it each time:

.. add blockly tab once math can be inputted into "sleep" block
.. code-block:: python

    from RosmoLib.defaults import *
    from time import sleep

    # Drive 25 cm
    drivetrain.set_speed(5, 5)
    sleep(25 / 5) # Notice how we can write math directly in our program!
    drivetrain.stop()

    # Drive 50 cm
    drivetrain.set_speed(5, 5)
    sleep(50 / 5)
    drivetrain.stop()

    # Drive 75 cm
    drivetrain.set_speed(5, 5)
    sleep(75 / 5)
    drivetrain.stop()

This looks pretty repetitive. Most of this code is exactly the same. In fact,
the only change between each block is the parameter we are passing to the
:code:`sleep` function. This is a perfect example of why we have functions.
Let's write our own function to drive the robot a certain distance.

.. tab-set:: 

    .. tab-item:: Python

        Python uses the keyword :code:`def` to let you, the programmer, tell it that you
        would like to *define* a new function. A full function definition looks like 
        this:

        .. code-block:: python

            def function_name(parameter1, parameter2, parameter3):
                # put your code here
                # code in your function can use the parameters by name like this:
                print(parameter1 / 5)

        In this example function, there are three parameters. Functions can have as 
        many or as few parameters as you want, or even have no parameters at all.

    .. tab-item:: Blockly

        In Blockly, you create functions by dragging a block that looks like the picture
        below. The interface allows you to specify the function name, and pass *parameters*
        to the function body. Here, we have a function called some_task (which you should rename
        based on what your function does) that takes in a parameter called :code:`text`, and uses
        prints the :code:`text` value. Functions can have as  many or as few parameters as you want,
        or even have no parameters at all.

        .. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/blocklyfunctiondefinition.png
            :width: 300

        The below blocks *calls* the function we defined above to run it. The value "Hello" is passed
        to the :code:`text` parameter, which results in "Hello" being printed to the console.

        .. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/blocklyfunctioncall.png
            :width: 300


.. admonition:: Try it out

    Define a function called :code:`drive_distance` that takes in one parameter: 
    :code:`distance_to_drive`. Use the parameter in your function as the 
    numerator of your fraction.

    Use your function to make the robot drive 3 distances in a row.

.. tip:: 

    Define your functions towards the top of your file, underneath the 
    :code:`import` statements. This way, code later in the file will be able to 
    use them.


    The Encoders
============

In the last lesson we mentioned *encoders*. What are they and what do they do?

Encoders are sensors which measure how far each motor (and thus each wheel) has
rotated. We mentioned that our motors aren't perfect, so when we tell them to go
a certain effort we don't know how fast it is actually rotating. Encoders 
measure exactly what the motor is doing and report this information back to the 
Rosmo.

.. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/blog017-image001-disks-resolution.jpg

An encoder uses a disk like the one above with alternating clear and black 
squares. The disk is attached to the output shaft of the motor. A small light 
is shined through the edge of the disk, and a sensor on the other side sees the
light. When a black part of the disk is in front of the light, the sensor sees
nothing. When a clear part of the disk is in front of the light, the sensor can
see the light. As the disk rotates, the sensor constantly switches from seeing 
and not seeing the light. The Rosmo can automatically count how many times it has
switched between seeing and not seeing the light, and can use this to calculate 
how far the wheel has moved.

The size of the black and clear squares determines how *precise* the encoder is.
As the squares get smaller, the light switches more times for the same amount of
rotations of the wheel, and thus we can more precisely measure the distance. The
downside of having really tiny squares is that the Rosmo's processor needs to work
harder to keep up with counting all the switches. In the image above you can see
some disks with different levels of precision.

.. tip:: 

    The disk and sensor in the Rosmo is hidden inside the motor's plastic case, so
    you won't be able to see them.

The Rosmo handles doing all the math to convert these switches into a real 
distance measurement for you, so you don't have to worry about it. We can use 
some new :code:`drivetrain` functions to see what the encoders are measuring:

.. tab-set:: 

    .. tab-item:: Python

        .. code-block:: python

            from RosmoLib.defaults import *
            from time import sleep

            while True:
                print(drivetrain.get_left_encoder_position())
                sleep(1)

    .. tab-item:: Blockly

        .. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/encoder.png
            :width: 300

This code uses something new: a :code:`while` *loop*. A :code:`while` loop will
run the code underneath it until a *condition* is no longer equal to
:code:`True`. In this case, the *condition* is the keyword :code:`True`, which
means that this code will run until :code:`True` doesn't equal :code:`True`.
Since this will never happen, the code will run forever unless you stop it 
manually on your computer.

.. tip:: 

    You will learn more about loops and conditions later in the course.

The code should run forever, display the drivetrain's left encoder position, and
then wait for one second. Then, it repeats and does this forever. If we didn't 
wait for one second, the Rosmo would read and send the encoder position to your 
computer as fast as it could (very fast!) which would be too much data for your 
computer to display at once on the screen.

.. admonition:: Try it out

    Try running this code to see what happens. Spin the left wheel of the Rosmo
    by hand and notice how the number changes.

Calculating distance
--------------------

Let's learn a bit about how the Rosmo uses the encoder to calculate how far the 
robot has moved.

The Rosmo knows the diameter of the robot's wheels; every Rosmo has the same wheels!

If a car's wheel rolls on the ground one full revolution, how far does the car
move? The car moves by one *circumference* of the circle:

.. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/Circle-Graphic-1024x576-2.png

.. tip:: 

    Reminder that the circumference of a circle is the distance around it.

    The circumference is calculated as :math:`C = \pi \cdot d`, where :math:`d`
    is the *diameter* of the circle.

If a car wheel (which is a circle with a circumference of 100 inches) rotates 5
times, how far does the car go? How would you find that?

.. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/P316_1-1.png
 
You would rotate the wheel once, and find that it has traveled 100 inches,
because the wheel would trace out it's circumference on the ground. Then, you
would rotate it a second time, and see it move another 100 inches. Then a third,
a fourth and a fifth time, and see the wheel has traced out it's circumference
on the ground 5 times. 

The amount it has traveled is 5 times the circumference. This can be used for
any number of rotations. If you rotate the wheel 3 times, you would move forward
3 times the circumference (300 inches), if you rotated it 1 and a half times,
you would move forward one and a half times the circumference (150 inches). 

.. math:: 
    
    d\text{ cm} = (\text{number of rotations}) \cdot (\text{circumference})

The Rosmo uses this equation to automatically calculate how far the wheels have 
moved in centimeters using the encoders.

Driving a distance (again)
--------------------------

In the last lesson you used a constant speed and a time to drive a distance. 
Now that you know that the encoders actually measure the distance, it would be 
better to use them for your :code:`drive_distance` function. We can modify your 
function to use a :code:`While` loop:

.. tab-set:: 

    .. tab-item:: Python

        .. code-block:: python

            def drive_distance(distance_to_drive):
                while drivetrain.get_left_encoder_position() < distance_to_drive:
                    drivetrain.set_speed(5, 5)
                    time.sleep(0.01)
                drivetrain.stop()

    .. tab-item:: Blockly

        .. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/drivedistanceencoder.png
            :width: 300
    

This code block uses a loop to constantly check if the left encoder position is
less than the distance you want the robot to go. Once it is no longer less than 
this distance, the loop stops running and the code moves on to the next line.
In this case, the next line tells the robot to stop.

.. admonition:: Try it out

    Replace your :code:`drive_distance` function with this new one. Try it out
    next to a meter stick. Is it more or less accurate than before?

.. admonition:: Challenge

    This code only checks the left encoder. Since both wheels are moving the
    same speed, this *should* be fine, but as we said, the motors aren't
    perfect. Can you think of a way to combine both encoder values together?

    To read the right encoder, you use
    :code:`drivetrain.get_right_encoder_position()`

Turning to a heading
---------------------

Once you know how to drive a certain distance with the Rosmo, it is easy to turn to a certain heading with it. 
First, you need to calculate the distance that a wheel must travel so that you are facing the correct heading,
and then simply rotate the Rosmo until the encoders have traveled that distance.

Calculating the necessary distance is complicated, but we can break down this problem into steps.

first, lets make a fraction that represents from 0.0 to 1.0 how far around the robot's circumference 
the wheels need to travel. In this case 0.0 is 0 degrees and 1.0 is 360 degrees. 

Now to get the distance the wheel travels, we need to multiply this fraction by the total distance the wheel
travels to rotate 360 degrees, this number is the circumference of a circle with the diameter same diameter 
as the robot. We can calculare this by multiplying the wheel track distance by pi. 

finally, to get the number of wheel rotations, we need to divide this distance by the circumference of 
the wheel, or pi times the wheel diameter. We can cancel pi from both sides of this division and that
leaves us with.  

.. math:: 

    \frac{\text{target degrees} \cdot \text{robot wheel track}} {360 \cdot \text{wheel diameter}}

Now that we have the number of wheel rotations, the rest of the program is easy. just turn the robot in the direction of the turn, and stop once
the number of rotations has exceeded the calculated rotation goal.

.. tab-set::
    .. tab-item:: Python
        .. code-block:: python
            def turn(target):
                global rotations
                differentialDrive.reset_encoder_position()
                rotations = (target * 15.5) / (360 * 6)
                if target > 0:
                    differentialDrive.set_effort((-0.3), 0.3)
                else:
                    differentialDrive.set_effort(0.3, (-0.3))
                while not math.fabs(motor1.get_position()) >= math.fabs(rotations):
                
                differentialDrive.stop()

    .. tab-item:: Blockly
        .. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/encoder-turn-blockly.png
            :width

            Helpful Drivetrain Functions
============================

Throughout this module, we've explored different ways to drive forwards
and turn, through setting efforts, speeds, and reading the encoders. However,
RosmoLib also provides some handy functions to make it easy for the user.
These functions use more complicated calculations to ensure that the Rosmo 
drives smoothly and exactly to the right distance every time.

.. tab-set:: 

    .. tab-item:: Python

        .. code-block:: python

            drivetrain.straight(20, max_effort = 0.5, timeout = None)

    .. tab-item:: Blockly

        .. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/straight.png
            :width: 300

This function will drive the robot straight forward for a distance in
centimeters that you specify. The other two parameters are *optional*. You can 
provide a value for them, but if you don't, the default value will be used.

Calling the function like this: :code:`drivetrain.straight(20)` will make the
robot go straight 20 centimeters, and use the default values for everything
else, meaning a maximum effort applied of 50% and no timeout.

You can also use a negative value for distance to drive backwards.

The :code:`max_effort` parameter specifies how much effort the robot is allowed
to apply while driving. By default it is 50%, which is a good effort for normal
driving on a flat surface.

The :code:`timeout` parameter specifies a time, in seconds, that the robot
should try to drive before giving up. For example, what if your robot runs into
something while driving, and the wheels get stuck? The robot will use the
encoders to measure the wheels and notice that it never arrived at the distance
you set, so it will try forever and none of your code will run afterwards. The
timeout lets you set a maximum time that the Rosmo should try for before giving
up. Usually, you won't need to use this, but it is there if you need it.

.. tab-set:: 

    .. tab-item:: Python

        .. code-block:: python

            drivetrain.turn(90, max_effort = 0.5, timeout = None)

    .. tab-item:: Blockly

        .. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/turn.png
            :width: 300

This function is similar to the :code:`straight` function, except that it
rotates the robot instead of driving it forwards.

The :code:`turn_degrees` parameter lets you tell the robot how many degrees it
should turn. Positive values will turn counterclockwise, and negative values turn
clockwise.

.. admonition:: Try it out

    Write code to drive the robot straight for 20 centimeters and then turn 90
    degrees clockwise. Don't forget to add the 
    :code:`from RosmoLib.defaults import *` statement at the top of your program.

    Driving With Geometry
=====================

The Rosmo's driving and turning functions can also be used to draw geometric patterns!
By driving a set distance and turning by a certain angle several times, you can draw a 
shape with as many sides as you want.

.. tip:: 

    To see the path your Rosmo has driven, you can place a dry-erase marker between the
    robot's wheels and trace your pattern on a whiteboard.


To draw any polygon, you just need to know the size of the shape's exterior angles,
and you need to decide how long the sides should be. Then, you just have to drive straight with the distance
of a side length and turn the number of degrees of the corresponding exterior angle.
Repeat this until the shape is finished.

.. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/exterior-angle.png

Triangle
--------

For a triangle, the interior angles measure 60 degrees and the exterior angles measure 120 degrees.
We can trace a triangle with side lengths of 30 cm by having our robot drive straight for 30 cm
three times and turn 120 degrees in between each drive straight.


.. tab-set::

    .. tab-item:: Python

        .. code-block:: python

            from RosmoLib.defaults import *

            differentialDrive.straight(30, 0.5)
            differentialDrive.turn(120, 0.5)
            differentialDrive.straight(30, 0.5)
            differentialDrive.turn(120, 0.5)
            differentialDrive.straight(30, 0.5)

    .. tab-item:: Blockly

        .. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/triangle-blockly.png
            :width: 300


Square
------

The process for tracing a square is similar to tracing a triangle. The interior angles are 90 degrees so
the exterior angles are also 90 degrees. Keeping a side length of 30 cm, we can trace a square by 
programming our robot to drive straight for 30 cm four times and turn 90 degrees between each drive straight.

.. tab-set::

    .. tab-item:: Python

        .. code-block:: python

            from RosmoLib.defaults import *

            drivetrain.straight(30, 0.5)
            drivetrain.turn(90, 0.5)
            drivetrain.straight(30, 0.5)
            drivetrain.turn(90, 0.5)
            drivetrain.straight(30, 0.5)
            drivetrain.turn(90, 0.5)
            drivetrain.straight(30, 0.5)

    .. tab-item:: Blockly

        .. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/square-blockly.png
            :width: 300

Polygons
--------

We can generalize the procedure used to make a triangle and square to make any regular polygon; you just have to
determine the exterior angle and choose a side length. However, for polygons with many sides, this process can get very tedious. 
Instead of repeating the same code multiple times, we can use a function to simplify the process. 

First, lets determine what information the function needs. To trace a polygon, you need to determine the number of sides 
and the length of each side. We can create a function that takes these two values as an input. 
The function will drive the distance we give it, turn by the exterior angle, and then repeat that process
as many times as there are sides in the shape. We can use a loop for this. The one problem is:
how do we know the measure of the exterior angles? Fortunately, this can be easily calculated with this equation:

.. math:: 
    360/n

With the variable *n* representing the number of sides of your polygon, this equation 
determines the number of degrees of your polgyon's exterior angles. With this information, you 
can now write a function to trace any regular polygon!

.. tab-set::
    
    .. tab-item:: Python

        .. code-block:: python
        
            from RosmoLib.defaults import *

            def polygon(sideLength, numSides):
                for i in range(int(numSides)):
                    differentialDrive.turn((360 / numSides), 0.5)
                    differentialDrive.straight(sideLength, 0.5)

    .. tab-item:: Blockly

        .. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/polygon-blockly.png
            :width: 450

Pinwheel
--------

Now we know how to easily draw any polygon, but we can take it one step further and draw a polygon pinwheel.
This pattern consists of several polygons extending out from a center point. Your Rosmo can execute this
by tracing several polygons consecutively and turning slightly between each new polygon. A pinwheel of 3 squares should look 
something like this:

.. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/pinwheel-square.jpg
    :width: 240

Programming this may seem like a daunting task, but it is actually quite simple. Every time you want to trace a piece
of the pinwheel, you just need to call your polygon function from before and then turn your robot slightly. We can calculate the measure of this
turn by dividing 360 degrees by the number of polygons we are tracing in order to keep even spacing between each polygon.
Repeat this process as many times as there are polygons in the pinwheel, and your pattern will be finished!

.. tab-set::

    .. tab-item:: Python

        .. code-block:: python

            from RosmoLib.defaults import *

            def pinwheel(sideLength, numSides, numShapes):
                for i in range(numShapes):
                    polygon(sideLength, numSides)
                    drivetrain.turn(360 / numShapes, 0.5)

    .. tab-item:: Blockly

        .. image:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/pinwheel-blockly.png 
            :width: 450

    Parking Challenge
=================

Challenge Description
---------------------
This challenge features a sequence of turns that the robot must perform in order
to get to the “end” of the Labyrinth. The robot must first begin at the starting
point, and get to the goal area by completing turning and forward movement behaviors. 

Materials needed
----------------
* White board or six 8.5”x11” sheets of paper (use scotch tape to tape the six sheets of paper together to form a 25.5”x22” rectangle. Turn it over and tape outside border to floor with blue masking tape.
* Black electrical tape (you can substitute blue masking tape for this exercise)
* Red electrical tape or red marker 
* Scissors (or cutting tool)
* Ruler (or straightedge)

Project specifications
----------------------

.. figure:: ![](https://raw.githubusercontent.com/Open-STEM/IntroToRoboticsV2/main/course/driving/media/labyrinth.png
    :width: 300
    :align: center
    
    Carnegie Mellon Robotics Academy, Labyrinth Challenge 

The robot should do the following:

* Begin fully contained in position 1 and then maneuver to goal area.
* Reach and be fully contained within position 2 without crossing any black lines.
    
