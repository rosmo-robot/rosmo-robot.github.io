---
layout: page
title: Learn Robotics
---

#  Introduction to Robotics with ROSMO Robots

This class is designed for instructors to learn the basics of robotics and programming using **ROSMO Robots**. You will be using **MicroBlocks**, a simple and powerful visual programming language, as an introduction to coding. For those who wish to advance, you can transition from MicroBlocks to Python as you become more comfortable programming the robots.

The course consists of several hands-on modules, beginning with an **Introduction to Robotics**. These modules cover topics like:  
- **Driving** the robot  
- Using **sensors**  
- Operating the **manipulator (robot arm)**  

## Final Project: Delivery Robot Challenge  
The course concludes with an exciting **final project** that brings together everything you have learned in the previous modules. This **Delivery Robot Challenge** allows students to program their robot to complete a series of tasks. To add a competitive element, an optional scoring rubric is provided to evaluate the runs completed by students.  

![Final Project Delivery Robot Challenge](../../_images/deliveryRobotImage.png)  

## Support and Contact  
We hope this course is engaging and enjoyable for both you and your students. Since this is a new course with new robots and software, there may be occasional bugs or unexpected issues. If you encounter any challenges or have questions, don’t hesitate to contact us.  

For more details about the program and resources, please visit the [ROSMO website](https://rosmo-robot.github.io/).  

Dive in and start exploring the world of robotics with ROSMO and MicroBlocks!

## In this Module You Will:

- Learn about the field of robotics  
- Assemble your robot  
- Install the software required for programming the robot  
- Write a short program to familiarize yourself with programming the ROSMO robot  

## At the End of this Module, You Will Be Able To:

- Recognize the characteristics of robots  
- Discuss the core disciplines that make up the field of robotics  
- Understand the components of the robot and how it is assembled  
- Be familiar with the tools for programming  

## Completing the Module  
To finish this module, review and complete all tasks outlined in each section. Then, successfully pass the module quiz at the end.

## Getting the Robot to Drive

### In This Module, Students Will:

- Learn how to set power to the robot’s drivetrain  
- Understand the relationship between motor efforts and the robot’s motion  
- Be introduced to motor encoders and how to use them to correct the robot’s motion  
- Use the pre-made drive, turn, and button functions  

### At the End of This Module, Students Will Be Able To:

- Control the robot’s basic motions  
- Understand the basics of while loops and exit conditions  
- Be familiar with making and running functions  
- Break down a larger path into components and convert it into code  















# Objectives
 -  Get at strong foundation in open-source electronics and prototyping
 -  Gain intuition on mechanical prototyping and design with dc brush motors, servo motors 
 -  Apply basic machine learning and computer vision to a small project



![Bot](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/bat.jpeg)

![Bot](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/stripped.jpeg)



# Other PicoW or ESP32 cars

- [Edurob](https://github.com/IDiAL-IMSL/Edurob/tree/main) not yet available for sale

- [Wukong 2040](https://www.elecfreaks.com/elecfreaks-wukong2040-breakout-board-for-raspberry-pi-pico.html) no encoders, closed hardware

- [ESP cam car](https://www.aliexpress.com/item/1005005439195049.html), no encoders, closed hardware

# Notes on software installed on the Ubuntu Docker image

docker run -p 6080:80 --security-opt seccomp=unconfined --shm-size=512m --device=/dev/ttyUSB0 --device=/dev/ttyACM0 tiryoh/ros2-desktop-vnc:jazzy

apt-get update

sudo apt remove unattended-upgrades

In the browser at 127.0.0.1:6080
Open a terminal and
git clone -b rosmo git@github.com:hippo5329/linorobot2_hardware.git
sudo apt-get install -y --install-recommends linux-lowlatency
sudo apt remove -y brltty
sudo apt install -y python3-venv build-essential cmake git curl
curl -fsSL -o get-platformio.py https://raw.githubusercontent.com/platformio/platformio-core-installer/master/get-platformio.py
python3 get-platformio.py
rm get-platformio.py
echo "PATH=\"\$PATH:\$HOME/.platformio/penv/bin\"" >> $HOME/.bashrc
source ~/.bashrc
curl -fsSL https://raw.githubusercontent.com/platformio/platformio-core/develop/platformio/assets/system/99-platformio-udev.rules | sudo tee /etc/udev/rules.d/99-platformio-udev.rules
sudo service udev restart
sudo usermod -a -G dialout $USER
sudo usermod -a -G plugdev $USER
export ROS_DISTRO=jazzy
export ROS_DISTRO=jazzy
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
sudo apt update
sudo apt install -y ros-$ROS_DISTRO-desktop ros-dev-tools python3-colcon-common-extensions python3-pip
sudo rosdep init
rosdep update
echo "source /opt/ros/$ROS_DISTRO/setup.bash" >> ~/.bashrc
source ~/.bashrc
mkdir ~/uros_ws/src -p
cd ~/uros_ws/src
git clone -b $ROS_DISTRO https://github.com/micro-ROS/micro-ROS-Agent.git
git clone -b $ROS_DISTRO https://github.com/micro-ROS/micro_ros_msgs.git
cd ..
rosdep install --from-paths src --ignore-src -r -y
colcon build --symlink-install
cd ~
echo "source \$HOME/uros_ws/install/setup.bash" >> ~/.bashrc
source ~/.bashrc




git clone -b rosmo git@github.com:hippo5329/linorobot2.git
cd linorobor2 
chmod 777 install_linorobot2.bash
./install_linorobot2.bash 4wd ld19






----------------------


chmod 777 install

./install

source /opt/ros/humble/setup.bash

cd /tmp

wget https://github.com/hippo5329/linorobot2/raw/humble/install_linorobot2.bash

bash install_linorobot2.bash 2wd ld19

source ~/.bashrc

https://github.com/hippo5329/linorobot2_hardware/wiki#installation


ZIO
git clone -b esp32_zio https://github.com/hippo5329/linorobot2_hardware.git








