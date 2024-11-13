## Microblocks; Best if you're just starting

1) Download [ESP32-S3 bin](https://github.com/rosmo-robot/rosmo-robot.github.io/raw/master/assets/img/v1/vm_esp32_s3.bin)
   
3) Visit [ESP web tool in a Chrome browser](https://espressif.github.io/esptool-js/)
   
5) Connect ESP32-S3 and flash device (you may need to hold the 'boot' button)
   
7) Use the [Pilot version in Chrome](https://microblocks.fun/run-pilot/microblocks.html){:target="_blank"}
   
8) In Microblocks; Cog icon > Install ESP firmware from URL > Paste https://microblocks.fun/downloads/pilot/vm/vm_esp32-s3.bin
   
9) Download this raw [UBP file](https://github.com/rosmo-robot/rosmo-robot.github.io/blob/master/assets/img/v1/rosmo-wifiremote-public.ubp){:target="_blank"} and open it in the Microblocks app.

<video src="https://github.com/rosmo-robot/zio_demo/assets/400875/4d8f3e58-93ae-484d-b4bf-076c96f3a7d6" controls="controls" style="max-width: 730px;"></video>

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/microblocks.png)

- Provides a block programing interface 

- Provides an [Android app](http://www.microblocks.fun/wifigamepad/gamepadwifiremote.apk){:target="_blank"}  for remote control & [detailed instructions](http://www.microblocks.fun/en/wifi/gamepad){:target="_blank"}

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/wsgamepad-start.jpg)

Current status: Working but encoders not yet configured.


## Linorobot2 Software; Best if you want to learn ROS2

Status: Wheels spinning, but not fully tested yet. 
  
- [Linorobot2](https://github.com/hippo5329/linorobot2)
- Install [Docker desktop](https://www.docker.com/products/docker-desktop/){:target="_blank"}
- [Download Docker image](https://hub.docker.com/r/samuk/rosmorobot/tags){:target="_blank"} and run in Docker desktop
- Open browser to http://127.0.0.1:6080/ fullscreen the Linux desktop tab
- Open a terminal
- git clone https://github.com/johnny555/rosmo
- cd /rosmo/firmware/include
- nano config.h (put in your wifi credentials at line 195, set the agent IP at line 207 to the address of your computer, get this from your router or [AngryIP](https://angryip.org/){:target="_blank"}.) <ctrl +O> to save <ctrl + X> to exit
- cd ..
- pio run -e esp32s3_wifi 
- Open a file browser & search for .bin
- Send the .bin file to yourself via email or Google drive
- In your normal Windows/Mac desktop environment visit [ESP web tool](https://esp.huhn.me/)
- Connect ESP32-S3 and flash device with the .bin file
- Back in the terminal on your virtual machine; ros2 launch linorobot2_bringup bringup.launch.py micro_ros_transport:=udp4 micro_ros_port:=8888
- In a browser access http://localhost:8888/ to get teleop UI
- Have fun

## Micropython software
Status: Doesn't exist yet, 

Interest from author of [Otto Mecanum](https://github.com/UEA-envsoft/Otto-Mecanum) in adapting for Rosmo. Maybe developing from [explaining computers demo code](https://www.explainingcomputers.com/sample_code/web_control_test.py)


##  Openbot (Android) software;  

Status: Needs tweaking for ESP32S3

- Android app and Arduino for computer vision & AI
- [https://www.openbot.org](https://www.openbot.org/research)


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




## Arduino software
Status: Doesn't exist yet, 
Might be interesting to do something with [Arduino Mecanum](https://github.com/StormingMoose/DroneBot-Workshop-Mecanum-for-L9110S) and maybe [Smartcar Shield](https://github.com/platisd/smartcar_shield?tab=readme-ov-file#software) at some point
