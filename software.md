[Microblocks](#Microblocks).

[MicroPython](#MicroPython).

[ROS2](#ROS2).


Rosmo can be used in a few different applications:

* A **STEM learning platform using microblocks** for people just starting with robotics
  
* A robot for **Students and hobbyists to learn Python & ROS2 programming** with
  the same tools, languages, and libraries used in professional and industrial robots.

<a name="Microblocks"></a> 
# Microblocks 

1) Download [ESP32-S3 bin](https://github.com/rosmo-robot/rosmo-robot.github.io/raw/master/assets/img/v1/vm_esp32_s3.bin)
   
3) Visit [ESP web tool in a Chrome browser](https://espressif.github.io/esptool-js/)
   
5) Connect ESP32-S3 and flash device (you may need to hold the 'boot' button)
   
7) Use the [Pilot version in Chrome](https://microblocks.fun/run-pilot/microblocks.html){:target="_blank"}
   
8) In Microblocks; Cog icon > Install ESP firmware from URL > Paste https://microblocks.fun/downloads/pilot/vm/vm_esp32-s3.bin
   
9) Download this raw [UBP file](https://github.com/rosmo-robot/rosmo-robot.github.io/blob/master/assets/img/v1/rosmo-wifiremote-public.ubp){:target="_blank"} and open it in the Microblocks app.

<video src="https://github.com/rosmo-robot/zio_demo/assets/400875/4d8f3e58-93ae-484d-b4bf-076c96f3a7d6" controls="controls" style="max-width: 730px;"></video>

- Provides a block programing interface 

- Provides an [Android app](http://www.microblocks.fun/wifigamepad/gamepadwifiremote.apk){:target="_blank"}  for remote control & [detailed instructions](http://www.microblocks.fun/en/wifi/gamepad){:target="_blank"}

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/wsgamepad-start.jpg)

Current status: Working but encoders not yet configured.

<a name="ROS2"></a>
# ROS2 

Software; Best if you want to learn ROS2 based on [Linorobot2](https://github.com/hippo5329/linorobot2)

Status: Wheels spinning, encoders working but not fully tested yet. 

Thanks to [John Vial](https://github.com/johnny555) for contributing this code
  
- Install [Docker](https://www.docker.com/products/docker-desktop/){:target="_blank"}
- Start Docker gui
- in a terminal: docker run -p 6080:80 --security-opt seccomp=unconfined --shm-size=512m tiryoh/ros2-desktop-vnc:jazzy
- Open browser to http://127.0.0.1:6080/ fullscreen the Linux desktop tab
- Open firefox in the virtual machine, open this page so you can copy/paste
-  in a second tab download & extract [https://github.com/rosmo-robot/linorobot2_hardware](https://github.com/rosmo-robot/linorobot2_hardware)
- in a third tab download & extract [https://github.com/hippo5329/linorobot2/tree/rolling](https://github.com/hippo5329/linorobot2/tree/rolling)
-   Get your IP address from your router or [AngryIP](https://angryip.org/){:target="_blank"}.)
-  In file browser navigate to /Downloads/linorobot2_hardware-master/config/custom
- right click on rosmo_config.h & open in pluma (put in your wifi credentials at line 116, set the agent IP at line 113 & lidar ip at line 129 to the address of your computer, save the file
- open a terminal paste
  
```curl -fsSL -o get-platformio.py https://raw.githubusercontent.com/platformio/platformio-core-installer/master/get-platformio.py

python3 get-platformio.py 

sudo mkdir -p /usr/local/bin

sudo ln -s ~/.platformio/penv/bin/platformio /usr/local/bin/platformio

sudo ln -s ~/.platformio/penv/bin/pio /usr/local/bin/pio

sudo ln -s ~/.platformio/penv/bin/piodebuggdb /usr/local/bin/piodebuggdb

cd /Downloads/linorobot2_hardware-master/firmware/

pio run -e rosmo
```

- Open a file browser & search for .bin
- Send the .bin file to yourself via email or Google drive
- In your normal Windows/Mac desktop environment visit [ESP web tool](https://esp.huhn.me/)
- Connect ESP32-S3 and flash device with the .bin file
- In the terminal of the virtual machine
- `cd linorobot2-rolling`
- `chmod +X install_linorobot2.bash`
- `./install_linorobot2.bash`
- `ros2 launch linorobot2_bringup bringup.launch.py micro_ros_transport:=udp4 micro_ros_port:=8888`
- In a browser access http://localhost:8888/ to get teleop UI
- Have fun

<a name="MicroPython"></a>
## MicroPython 

Status: Beta released providing Webui to drive the robot with encoders 

Please see [Micropython repository](https://github.com/rosmo-robot/micropython)

Thanks to [Alex](https://github.com/UEA-envsoft) for contributing this code


##  Openbot (Android) software;  

Status: Needs tweaking for ESP32S3

- Android app and Arduino for computer vision & AI
- [https://www.openbot.org](https://www.openbot.org/research)

## C++/ Arduino software

Status: Doesn't exist yet, 
Might be interesting to do something with [Arduino Mecanum](https://github.com/StormingMoose/DroneBot-Workshop-Mecanum-for-L9110S) and maybe [Smartcar Shield](https://github.com/platisd/smartcar_shield?tab=readme-ov-file#software) at some point.  

##  Possible learning journey

-   Assemble 2WD bot
-   Drive 2WD bot with Microblocks remote control from Android 
-   try to make the robot drive in a straight line
-   Configure the encoders in microblocks and try again 
-   Add a pair of mechanical bump sensors, in microblocks do bump & run
-   Add a sharpie - Draw a straight line on a large piece of paper
-   Draw your initials
-   Add a pair of line sensors, follow a line 
-   Add 2x wheels to make a 4wd bot
-   Configure Microblocks to run 4WD
-   Try and make it go in a straight line again
-   Complete the [parking challenge](https://introtoroboticsv2.readthedocs.io/en/latest/course/driving/parking.html) using microblocks
-   Add Mecanum wheels.
-   In Microblocks make the robot go sideways with remote control
-   Complete the parking challenge again without making the robot turn at all
-   Install an IMU & configure in Microblocks
-   Add a ESP32 cam and watch the livestream from a computer
-   Install a grabber & move an object from a to b in the parking challenge
-   Move two objects
-   Add a daughterboard with 2x oled
-   Load the robot eyes in microblocks & make the eyes interact with the controls
-   Install thonny/ micropython and complete steps 1-15 in Micropython code
-   Install ROS and complete steps 1-15 again
-   Install a Lidar and map a room
-   Run the robot. A lot.
-   Add the protoboard add on - Add a novel sensor to the bot and get it working
-   In easyeda create a daughterboard to your own design

##  Further robotics resources

- [Robo Grok](https://www.robogrok.com/)
- [Python Robotics](https://atsushisakai.github.io/PythonRobotics/)
- [CPP Robotics](https://github.com/giacomo-b/CppRobotics)
- [Ros2RoboticsCpp](https://github.com/quangnhat185/Ros2RoboticsCpp)
- [Awesome robotics](https://github.com/ahundt/awesome-robotics)
- [Awesome ROS2](https://github.com/fkromer/awesome-ros2)
- [Awesome-robotics-libraries](https://github.com/jslee02/awesome-robotics-libraries)
- [C reference document](https://github.com/rosmo-robot/modern-robotics-I-course/blob/main/Introductory%20C%20Programming%20Reference.md)
- [Weekly robotics](https://github.com/msadowski/awesome-weekly-robotics)
- [Top 100 universities](https://edurank.org/engineering/robotics/)
- [UK undergraduate](https://www.thecompleteuniversityguide.co.uk/courses/search/undergraduate/all?keyword=robotics#h1)


  
