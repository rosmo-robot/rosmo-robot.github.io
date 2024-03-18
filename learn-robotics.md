---
layout: page
title: Learn Robotics
---
The robot PCB has now moved to [ziobot](https://rosmo-robot.github.io/) the PCB and components found there can be used with the XRP robotics kit.


# Objectives
 -  Get at strong foundation in open-source electronics and prototyping
 -  Gain intuition on mechanical prototyping and design with dc brush motors, servo motors and stepper motors
 -  Apply basic machine learning and computer vision to a small project


# 1) Microblocks

- [Microblocks](https://microblocks.fun/)

# 2) Micropython

- [Explaining computers](https://www.explainingcomputers.com/pi_pico_w_robot.html)

# 3) Arduino
- [Smartcar](https://github.com/platisd/smartcar_shield/tree/master/examples/Car) Projects from [2019](https://github.com/DIT112-V19), [2020](https://github.com/DIT112-V20/) [2021](https://github.com/DIT112-V21/)

# 2) ROS2

- [Linorobot2](https://github.com/linorobot/linorobot2#linorobot2)
- [Visual circuit](https://github.com/JdeRobot/VisualCircuit#visual-circuit)

 # Further robotics resources

- [Python Robotics](https://atsushisakai.github.io/PythonRobotics/)
- [CPP Robotics](https://github.com/giacomo-b/CppRobotics)
- [Ros2RoboticsCpp](https://github.com/quangnhat185/Ros2RoboticsCpp)
- [Awesome robotics](https://github.com/ahundt/awesome-robotics)
- [Awesome ROS2](https://github.com/fkromer/awesome-ros2)
- [Awesome-robotics-libraries](https://github.com/jslee02/awesome-robotics-libraries)
- [Weekly robotics](https://github.com/msadowski/awesome-weekly-robotics)
- [Top 100 universities](https://edurank.org/engineering/robotics/)
- [UK undergraduate](https://www.thecompleteuniversityguide.co.uk/courses/search/undergraduate/all?keyword=robotics#h1)




# Similar projects 
https://github.com/Roboost-Robotics/Roboost-Primary-Motor-Cortex




 ![Bot](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/lid.jpeg)




![Bot](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/bat.jpeg)

![Bot](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/stripped.jpeg)



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


# Other PicoW or ESP32 cars

- [Edurob](https://github.com/IDiAL-IMSL/Edurob/tree/main) not yet available for sale

- [Wukong 2040](https://www.elecfreaks.com/elecfreaks-wukong2040-breakout-board-for-raspberry-pi-pico.html) no encoders, closed hardware

- [ESP cam car](https://www.aliexpress.com/item/1005005439195049.html), no encoders, closed hardware

# Notes on software installed on the Ubuntu 22.04 Virtualbox image, or compute module

apt-get update

sudo apt remove unattended-upgrades

[ssh](https://dev.to/developertharun/easy-way-to-ssh-into-virtualbox-machine-any-os-just-x-steps-5d9i) -p 3022 ros2@127.0.0.1

wget https://raw.githubusercontent.com/linorobot/ros2me/master/install

nano install

chmod 777 install

./install

source /opt/ros/humble/setup.bash

cd /tmp

wget https://github.com/hippo5329/linorobot2/raw/humble/install_linorobot2.bash


bash install_linorobot2.bash 2wd ld19

source ~/.bashrc

https://github.com/hippo5329/linorobot2_hardware/wiki#installation

git clone -b esp32_zio https://github.com/hippo5329/linorobot2_hardware.git

dmesg | grep tty






