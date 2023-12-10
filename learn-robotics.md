---
layout: page
title: XRP-X4
---

 ![Bot](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/lid.jpeg)



# XRP-4 BOM (WIP) 100% open hardware

- 1x [XRP Open hardware XRP PCB](http://docs.sparkfun.com/SparkFun_XRP_Controller/hardware_overview/)
- 1x [Motor & components holder PCB](https://easyeda.com/editor#id=949370ce6c864b5090fffa824b774df2) (Untested WIP just register and one click order from JLPCB if you're feeling brave)
- 1x [1mm > 1.5mm Pack of cables](https://www.aliexpress.com/item/32800824381.html)
- 1x [Pack of 1mm 6p JST SH connectors](https://s.click.aliexpress.com/e/_DDIr1m7)
- 1x [Pack of 1.5mm 6P JST ZH connectors](https://www.aliexpress.com/item/32911443586.html)
- 4x [6v 150RPM Bringsmart motors](https://s.click.aliexpress.com/e/_DC72ruf)
- 4x [N20 rubber wheels](https://s.click.aliexpress.com/e/_DBjDZqx) or [3mm shaft Mecanum wheels A](https://www.aliexpress.com/item/1005003264388589.html),[B](https://www.aliexpress.com/item/32977691906.html) or [C](https://www.thingiverse.com/thing:1358552)
- 4x [N20 mounts](https://s.click.aliexpress.com/e/_Dm7LWRD)
- 1x pack [18mm female standoffs](https://www.aliexpress.com/item/32539100523.html)
- 1x pack [M3 x 6mm screw](https://www.aliexpress.com/item/32539100523.html)
- 1x [Battery cable](https://www.aliexpress.com/item/1005003207076823.html)
- 1X [9v Battery](https://s.click.aliexpress.com/e/_DdPChq3)

Or alternately a upgraded  or [18650 battery](https://s.click.aliexpress.com/e/_DClgys7) or open hardware [18650 battery](https://oshwlab.com/wagiminator/fp6277-power-bank)



![Bot](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/bat.jpeg)

![Bot](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/stripped.jpeg)

# Additional components


- [On-board compute. Beagleboard Play](https://www.beagleboard.org/boards/beagleplay)
- [Camera - Maxlab](https://github.com/maxlab-io/tokay-lite-pcb)
- [TOF - Sparkfun](https://www.sparkfun.com/products/19013)
- [OLED/Eyes - Adafruit](https://www.adafruit.com/product/5297#description)
- [Line finder - ZIO](https://github.com/ZIOCC/Zio-Line-Finder-Qwiic-4-Transceivers-)
- [Ultrasonic - ZIO](https://github.com/ZIOCC/Zio-Qwiic-Ultrasonic-Distance-Sensor) 
- [Servo - Zio](https://github.com/rosmo-robot/Qwiic_Servo_Driver_PCA9685/) for [mini arm](https://www.thingiverse.com/thing:5683010)
- [Cube standoff](https://www.aliexpress.com/item/1005005880192495.html)



# Older iterations


 ![Bot](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/signal-2023-11-24-230734.jpeg)

 ![Bot](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/profile-xrp.jpeg)

 ![Bot](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/bottom-xrp.jpeg)

![Bot](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/top-xrp.jpeg)
 ![Bot](https://raw.githubusercontent.com/samuk/IntroToRoboticsV2/main/course/ros2/xrp4.jpeg)

 
 ![Bot](https://raw.githubusercontent.com/samuk/IntroToRoboticsV2/main/course/ros2/compute-xrp4.jpeg
)


 ![Bot](https://raw.githubusercontent.com/samuk/IntroToRoboticsV2/main/course/ros2/ultrasonic-xrp4.jpeg
)

# How to run this bot with ROS2 (WIP)

- Install [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
- Download the [OVA file](https://archive.org/details/ros-2_OVA_0_1) (work in progress) and load it in Virtualbox. ~6Gb ~5hr download.
- Start the virtual machine (password is ros2)
- In the linux desktop Open VScode
- If using a ESP3 configure [platformio.ini](https://github.com/rosmo-robot/linorobot2_hardware_ESP32_Pico/blob/master/firmware/platformio.ini) to match, defaults to PicoW.
- Build the firmware and flash to your device.
- Put the device in your robot car & start it
- Search the network for your-robot-ip using AngryIP
- Launch ROS2
- Open [http://your-robot-ip:8888/](https://github.com/dheera/rosboard/pull/100) in a browser and control the car
- Have fun

# Other PicoW or ESP32 cars

- [Edurob](https://github.com/IDiAL-IMSL/Edurob/tree/main) not yet available for sale

- [Wukong 2040](https://www.elecfreaks.com/elecfreaks-wukong2040-breakout-board-for-raspberry-pi-pico.html) no encoders, closed hardware

- [ESP cam car](https://www.aliexpress.com/item/1005005439195049.html), no encoders, closed hardware

# Notes on software installed on the Ubuntu 22.04 Virtualbox image, or compute module

apt-get update

sudo apt remove unattended-upgrades

sudo apt install lubuntu-desktop thonny nemo chromium

mkdir install

cd install

wget https://raw.githubusercontent.com/linorobot/ros2me/master/install

./install

wget https://raw.githubusercontent.com/linorobot/linorobot2/humble/install_linorobot2.bash

bash install_linorobot2.bash

install https://code.visualstudio.com/

Install platformio

Install vscode extensions c/c++ & platformio manually "code --install-extension myextension.vsix

git config --system core.longpaths true

git clone https://github.com/rosmo-robot/linorobot2_hardware_ESP32_Pico -b $ROS_DISTRO

boot config.txt
- camera_auto_detect=0 (will be 1 by default)
- start_x=1

Angryip?

[Rosboard fork](https://github.com/dheera/rosboard/pull/100)


# Objectives
 -  Get at strong foundation in open-source electronics and prototyping
 -  Gain intuition on mechanical prototyping and design with dc brush motors, servo motors and stepper motors
 -  Apply basic machine learning and computer vision to a small project

# Older notes on robotics education   

Derived from work by Mithi [🐳](https://mithi.github.io/deep-blueberry) [☕️](https://ko-fi.com/minimithi) 

# 1) Microblocks

- [Microblocks](https://microblocks.fun/)

# 2) Micropython

- [Explaining computers](https://www.explainingcomputers.com/pi_pico_w_robot.html)

# 3) Arduino
- [Smartcar](https://github.com/platisd/smartcar_shield/tree/master/examples/Car) Projects from [2019](https://github.com/DIT112-V19), [2020](https://github.com/DIT112-V20/) [2021](https://github.com/DIT112-V21/)

# 4) Python

- [Pyrobots](https://www.csc.liv.ac.uk/~lad/pyrobots/exercises.html) eg [Test document](https://rosmo-robot.github.io/part-1-initio/)
- [Example project](https://github.com/DIT112-V19/group-03) connected to Smartcar Microcontroller
- [Autonomous Robotics - ENPM 809T](https://github.com/govindak-umd/Autonomous_Robotics)
- [Python Robotics](https://atsushisakai.github.io/PythonRobotics/getting_started.html)

# 5) ROS2

- [Linorobot2](https://github.com/linorobot/linorobot2#linorobot2)
- [Visual circuit](https://github.com/JdeRobot/VisualCircuit#visual-circuit)

# Stem robots

[Xiaogui](https://twitter.com/wgy421)
[Fluffbug](https://github.com/deshipu/fluffbug/tree/main/fluffbug-v8.2)


# Further Courses

- [♥️ Robot Academy][series1], Peter Corke, Queensland University of Technology
- [MIT Open Courseware: Robotics][series9] 
- Coursera: [Robotics Specialization][series3], University of Pennsylvania
- Coursera: [Modern Robotics Specialization][series4]  [book][series11a] + [📺 channel][series11b], Northwestern University
- Coursera: [Self-Driving Cars][series10], University of Toronto
- :dollar: Udacity: [Robotics Nanodegree][series5]
- :dollar: Udacity: [Intro to Self-Driving Cars Nanodegree][series6b]
- :dollar: Udacity: [Self-Driving Car Nanodegree][series6]
- :dollar: Udacity: [Flying Car Nanodegree][series7]
- :dollar: Udacity: [Sensor Fusion Nanodegree][series12]
- :dollar: [The Construct: Robotics Developers Course Library][series8], Robot Ignite Academy
- :dollar: [Master's Certification Program in Autonomous Vehicles][series13], Skill Lync

[series1]: http://robotacademy.net.au
[series3]: https://www.coursera.org/specializations/robotics
[series4]: https://www.coursera.org/specializations/modernrobotics
[series5]: https://www.udacity.com/robotics
[series6]: https://www.udacity.com/drive
[series6b]: https://www.udacity.com/course/intro-to-self-driving-cars--nd113
[series7]: https://www.udacity.com/course/flying-car-nanodegree--nd787
[series8]: https://www.theconstructsim.com/robotigniteacademy_learnros/ros-courses-library/
[series9]: https://ocw.mit.edu/search/ocwsearch.htm?q=robotics
[series10]: https://www.coursera.org/specializations/self-driving-cars
[series11a]: http://modernrobotics.org 
[series11b]: https://www.youtube.com/playlist?list=PLggLP4f-rq02vX0OQQ5vrCxbJrzamYDfx
[series12]: https://www.udacity.com/course/sensor-fusion-engineer-nanodegree--nd313
[series13]: https://skill-lync.com/courses/masters-certification-program-autonomous-driving

# Single Courses
- Udacity: [Artificial Intelligence for Robotics][course21], Sebastian Thrun
- EdX: [Self-Driving Cars with Duckietown][course40], ETHzurich
- EdX: [Autonomous Mobile Robots][course1], ETHZurich
- EdX: [Autonomous Navigation for Flying Robots][course2], Technische Universitat Munchen
- EdX: [Underactuated Robotics][course3], Massachusetts Institute of Technology
- EdX: [Robotics][course4], Columbia University in the city of New York
- EdX: Robot Mechanics and Control [Part I][course5] and [Part II][course6], Seoul National University
- EdX: [Robotics Foundations I - Robot Modeling][course7], Università degli Studi di Napoli Federico II
- EdX: [Robotics Foundation II - Robot Control][course41], Bruno Siciliano, Università degli Studi di Napoli Federico II
- EdX: [Robot Development][course42], Angelo Cangelosi, Università degli Studi di Napoli Federico II
- EdX: [Hello (Real) World with ROS – Robot Operating System][course8], Delft University of Technology
- Udemy: [ROS for Beginners: Basics, Motion and OpenCV][course30], Anish Koubaa
- Udemy: [ROS for Beginners II: Localization, Navigation and SLAM][course31], Anish Koubaa
- [Self-Driving Cars with ROS and Autoware][course27], Apex.AI
- [Autonomous Intelligent Systems][course10], Wolfram Burgard et al, University of Freiburg
- [Introduction to Robotics][course11], Oussama Khatib, Stanford Engineering Everywhere
- [Introduction to Aerial Robotics][course13], Kostas Alexis, University of Nevada
- [Deep-learning for Self-Driving Cars][course14], Lex Fridman, Massachusetts Institute of Technology
- [Advanced Robotics (CS 287)][course19], Pieter Abbeel, University of California at Berkeley
- [♥️ Underactuated Robotics][course20c] | [book][course20a] + [📺 channel][course20b], Russ Tedrake, Massachusetts Institute of Technology
- [Robotics Manipulation: Perception, Planning, and Control][course29] + [📺 channel][course29b], Russ Tedrake, Massachusetts Institute of Technology
- [Visual Navigation for Flying Robot][course22], Jürgen Sturm, Technical University of Munich
- [📺 SLAM playlist][course15], Cyrill Stachniss, University of Freiburg
- [📺 Robotics I][course16], De Luca, Universita di Roma
- [📺 SLAM Lectures][course18], Clause Brenne, Leibniz University Hannover
- [📺 Applied Robot Design (CS235)][course23], Reuben Brewer, Standford University
- [Robogrok: Robotics][course17a] + [📺 channel][course17b], Angela Sodemann
- [Autonomous Robots Lab: Autonomous Mobile Robot Design (and more)][course24], University of Nevada
- [MEAM 620: Robotics][course25], University of Pennsylvania
- [Robotics: Advanced Concepts and Analysis][course26], Ashitava Ghosal, Indian Institute of Science
- [Introduction to Robotics][course28], Burton Ma, York University 
- [NPTEL: Introduction to Robotics][course32], IIT Madras
- [CMSC828T Vision, Planning And Control In Aerial Robotics][course33], Yiannis Aloimonos, University of Maryland
- [HKUST ELEC5660 Introduction to Aerial Robots][course34], Shaojie SHEN, Hong Kong University of Science and Technology
- [ENAE 788M: Hands On Autonomous Aerial Robotics][course35], Nitin Sanket, University of Maryland
- [📺 Evolutionary robotics][course43], Josh Bongard, University of Vermont
- [Programming for Robotics - ROS][course44], Edo Jelavić, Tom Lankhorst, Marco Hutter, ETHZurich

[course1]: https://www.edx.org/course/autonomous-mobile-robots-ethx-amrx-2
[course2]: https://www.edx.org/course/autonomous-navigation-flying-robots-tumx-autonavx-0
[course3]: https://www.edx.org/course/underactuated-robotics-mitx-6-832x-0
[course4]: https://www.edx.org/course/robotics-columbiax-csmm-103x#!
[course5]: https://www.edx.org/course/robot-mechanics-control-part-i-snux-snu446-345-1x
[course6]: https://www.edx.org/course/robot-mechanics-control-part-ii-snux-snu446-345-2x
[course7]: https://www.edx.org/course/robotics-foundations-i-robot-modeling
[course8]: https://www.edx.org/course/hello-real-world-with-ros-robot-operating-system
[course9]: https://www.coursera.org/learn/mobile-robot
[course10]: http://ais.informatik.uni-freiburg.de/teaching/ss16/robotics/index_en.php
[course11]: https://see.stanford.edu/Course/CS223A
[course13]: http://www.kostasalexis.com/introduction-to-aerial-robotics.html
[course14]: http://selfdrivingcars.mit.edu/
[course15]: https://www.youtube.com/watch?v=V9qQc5X7O0k&list=PLgnQpQtFTOGQECnBvZSV61oxTrkPut-nc
[course16]: https://www.youtube.com/watch?v=pitZv3PuVMw&list=PLAQopGWlIcyaqDBW1zSKx7lHfVcOmWSWt
[course17a]: http://robogrok.com/index.html
[course17b]: https://www.youtube.com/user/asodemann3/videos
[course18]: https://www.youtube.com/watch?v=B2qzYCeT9oQ&list=PLpUPoM7Rgzi_7YWn14Va2FODh7LzADBSm
[course19]: https://people.eecs.berkeley.edu/~pabbeel/cs287-fa19/
[course20a]: http://underactuated.csail.mit.edu/underactuated.html
[course20b]: https://www.youtube.com/channel/UChfUOAhz7ynELF-s_1LPpWg/playlists
[course20c]: http://underactuated.csail.mit.edu/Spring2020/
[course21]: https://www.udacity.com/course/artificial-intelligence-for-robotics--cs373
[course22]: https://vision.in.tum.de/teaching/ss2013/visnav2013
[course23]: https://www.youtube.com/user/StanfordCS235/videos
[course24]: https://www.autonomousrobotslab.com/education.html
[course25]: https://alliance.seas.upenn.edu/~meam620/wiki/index.php?n=Main.Projects
[course26]: https://nptel.ac.in/courses/112/108/112108093/#
[course27]: https://www.apex.ai/autoware-course
[course28]: https://www.eecs.yorku.ca/course_archive/2017-18/W/4421/
[course29]: http://manipulation.mit.edu/
[course29b]: https://www.youtube.com/watch?v=PGY-4LOPs7U
[course30]: https://www.udemy.com/course/ros-essentials/learn/
[course31]: https://www.udemy.com/course/ros-navigation/
[course32]: https://nptel.ac.in/courses/107/106/107106090/
[course33]: https://cmsc828t.github.io/
[course34]: https://gaowenliang.github.io/HKUST-ELEC5660-Introduction-to-Aerial-Robots/index.html
[course35]: http://prg.cs.umd.edu/enae788m
[course40]: https://www.edx.org/course/self-driving-cars-with-duckietown
[course41]: https://www.edx.org/course/robotics-foundation-ii-robot-control
[course42]: https://www.edx.org/course/developmental-robotics
[course43]: https://www.youtube.com/watch?v=CmiJIKxtEOE&list=PLAuiGdPEdw0inlKisMbjDypCbvcb_GBN9
[course44]: https://rsl.ethz.ch/education-students/lectures/ros.html


# Useful Concepts and Tools
- CAD Tools: [Autodesk Fusion 360][tools10]  [OnShape][tools12]
- [♥️ 🐳 Deep Learning][tools1]
- [Hackertools: The Missing Semester of Your CS Education][tools15], MIT Open Learning
- Kalman Filters: [Roger R. Labbe][tools2]  [Balzer82][tools11]
- Control Systems: [📺 Steve Brunton][tools3]  [📺 Brian Douglas][tools4] | [Tyler Veness][tool5]
- Algorithms and Data Structures, C++, Python, Octave
- [♥️ More courses](https://github.com/mithi/robotics-coursework/issues/6#issuecomment-629713457)

[tools1]: https://mithi.github.io/deep-blueberry/
[tools2]: https://github.com/rlabbe/Kalman-and-Bayesian-Filters-in-Python/
[tools3]: https://youtu.be/Pi7l8mMjYVE?list=PLMrJAkhIeNNR20Mz-VpzgfQs5zrYi085m
[tools4]: https://www.youtube.com/user/ControlLectures/featured
[tools10]: https://www.autodesk.com/products/fusion-360/students-teachers-educators
[tools11]: https://github.com/balzer82/Kalman
[tools12]: https://www.onshape.com/
[tool5]: https://github.com/calcmogul/controls-engineering-in-frc
[tools15]: https://missing.csail.mit.edu/

[Top 100 universities](https://edurank.org/engineering/robotics/)

# Archived Courses
- EdX: [Robotics: Locomotion Engineering][course36], Dan Koditschek, University of Pennsylvania
- EdX: [Robotics: Dynamics and Control][course37], Vijay Kumar, University of Pennsylvania
- EdX: [Robotics: Vision Intelligence and Machine Learning][course38], Jianbo Shi, University of Pennsylvania
- EdX: [Robotics: Kinematics and Mathematical Foundations][course39], Camillo Taylor, University of Pennsylvania
- Coursera: Control of Mobile Robots, Magnus Egerstedt, Georgia Institute of technology


[course36]: https://www.edx.org/course/robotics-locomotion-engineering
[course37]: https://www.edx.org/course/robotics-dynamics-and-control
[course38]: https://www.edx.org/course/robotics-vision-intelligence-and-machine-learning
[course39]: https://www.edx.org/course/robotics-kinematics-and-mathematical-foundations


# Related Lists
| [Ahundt](https://github.com/ahundt/awesome-robotics)
| [Jslee02](https://github.com/jslee02/awesome-robotics-libraries)
| [Kiloreux](https://github.com/Kiloreux/awesome-robotics)
| [Msadowki](https://github.com/msadowski/awesome-weekly-robotics)
| [Protontypes](https://github.com/protontypes/awesome-robotic-tooling)
| [Fkromer](https://github.com/fkromer/awesome-ros2)
| [HarshMaithani](https://medium.com/@harshmaithani09/a-fast-introduction-to-robotics-v-2-0-6d07516e053f)
| [Kanster](https://github.com/kanster/awesome-slam)
| [Papers Related to Quadrotors](https://github.com/prgumd/prg_QuadrotorPapers)

# Misc
| [Adafruit](https://adafruit.com/)
| [Instructables][related1]
| [Hackster][related2]
| [Thingiverse][related3] 
| [Hackaday](https://hackaday.com/)
| [Sparkfun](https://www.sparkfun.com/)
| [Robotshop][related4]
| [Robotics Today][related5]
| [Reddit](https://www.reddit.com/r/robotics/)
| [Youtube](https://github.com/mithi/robotics-coursework/issues/6#issue-608400679)
| [Planet GBC](http://www.planet-gbc.com/)
| [Euro Bricks](https://www.eurobricks.com/forum/index.php?/forums/topic/117305-gbc-the-akiyuki-project/)

[related1]: https://www.instructables.com/howto/robot/
[related2]: https://www.hackster.io/search?i=projects&q=robot
[related3]: https://www.thingiverse.com/search?q=robot
[related4]: https://www.robotshop.com/community/robot
[related5]: https://roboticstoday.github.io/watch.html

[UK undergraduate](https://www.thecompleteuniversityguide.co.uk/courses/search/undergraduate/all?keyword=robotics#h1)


# [🐳](https://mithi.github.io/deep-blueberry) [☕️](https://ko-fi.com/minimithi)
