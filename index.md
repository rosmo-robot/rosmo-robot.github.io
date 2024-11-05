---
layout: page
title: Rosmo
---
 
A micro-robot for ROS2 & Microblocks that can be assembled without soldering, or access to a 3D printer. 
An affordable, adaptable, and open-source robot, for students, makers, universities, R&D.

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/v1/0.8-side.jpeg)

If you'd like one please sign up for [Tindie waitlist](https://www.tindie.com/products/rosmo-robot/rosmo-robot-kit/)


## Parts list

| Part             | Description                               | Quantity |
| ------------------------- | ----------------------------------------- | -------- |
| ~$12  Rosmo Chassis | [Custom PCB Chassis](https://easyeda.com/editor#id=447760e4d8144c399aa1b6c57f085c0b){:target="_blank"} for sale soon  | 1       |
| ~$16-$32 Motors with encoder & wheel     | [6v 150RPM $Bringsmart motors](https://s.click.aliexpress.com/e/_DErxgYv){:target="_blank"}            | 2 or 4   |
| ~$5  80mm motor cables    | [6Pin reverse direction cables](https://s.click.aliexpress.com/e/_Dk6w1x3){:target="_blank"}            | 4   |
| ~$6 - $12 ESP32-S3-C1 N16R8          | [Olimex open hardware -recomended](https://www.olimex.com/Products/IoT/ESP32-S3/ESP32-S3-DevKit-Lipo/open-source-hardware){:target="_blank"}, [UK](https://thepihut.com/products/olimex-esp32-s3-devkit-lipo-development-board){:target="_blank"} [US](https://www.digikey.com/en/products/detail/olimex-ltd/ESP32-S3-DEVKIT-LIPO-EA/22157950){:target="_blank"}, [AUS](https://au.mouser.com/ProductDetail/Olimex-Ltd/ESP32-DevKit-Lipo?qs=Rp5uXu7WBW8uPlSS6e5Gsg%3D%3D){:target="_blank"} [official](https://eu.mouser.com/ProductDetail/Espressif-Systems/ESP32-S3-DevKitC-1-N8R8){:target="_blank"} or [Closed Waveshare ESP32s3](https://www.waveshare.com/product/esp32-s3-dev-kit-n8r8.htm) very cheap alternatives may [require soldering](https://forum.arduino.cc/t/chinese-esp32-s3-5v-pin-warning/1192758){:target="_blank"}        | 1        |
| ~$5 Hex Spacers               | [15mm height M3 standoff](https://s.click.aliexpress.com/e/_DEqXY9d){:target="_blank"} or [200pc M3 pack](https://s.click.aliexpress.com/e/_DEo1RWF){:target="_blank"}          | 1    |
| ~$9 1x 2A powerbank        |[OSHW powerbank](https://oshwlab.com/wagiminator/fp6277-power-bank){:target="_blank"} or [TNTOR Powerbank](https://tntor.com/product/tntor-5000mah-mini-power-bank){:target="_blank"} or  [Aliexpress Powerbank](https://s.click.aliexpress.com/e/_DCvODWh){:target="_blank"}*        | 1        |
| ~$4 USB>Pin adaptor  | [Type 3 DIP-4P](https://www.aliexpress.com/item/1005004696562222.html){:target="_blank"}*        | 1   

 *buy batteries locally if your postage service has restrictions on Lithium. 

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/IU4FcknEoXo/0.jpg)](https://www.youtube.com/watch?v=IU4FcknEoXo){:target="_blank"} 

 ~$50 US for 2wd, ~$80 for 4wd  

Rosmo is built from modular components on the [Open Robotic Platform rules](https://openroboticplatform.com/designrules){:target="_blank"}
 
 Some of the links on this page are affiliate links to help offset the costs of this project, no one is getting rich off of these. [List of the above items on Aliexpress](https://www.aliexpress.com/p/wishlist/shareReflux.html?groupId=H3r6Ix9p3i%2BvbdGhQpxk4NMRKh%2F%2Bgiup4z2X0odX6os%3D){:target="_blank"} cost can be reduced, by using existing powerbank.

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/v1/certification-mark-UK000062-wide.png)

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/signal-2024-04-05-171808.jpeg)

 
## Optional extras


| Add on           | ROS2 Linorobot                               | Microblocks | Micropython|
| ------------------------- | ----------------------------------------- | -------- |---------|
|  [MPU6050 IMU](https://www.adafruit.com/product/3886){:target="_blank"} | [Yes](https://github.com/hippo5329/linorobot2_hardware/wiki#supported-sensors){:target="_blank"}    | Yes   | To do |
|  [BNO055 IMU](https://www.adafruit.com/product/4646){:target="_blank"} | [Yes](https://github.com/linorobot/linorobot2_hardware/issues/21#issuecomment-1567868751){:target="_blank"}   | To do    |To do |
|  [Ultrasonic - ZIO](https://github.com/ZIOCC/Zio-Qwiic-Ultrasonic-Distance-Sensor){:target="_blank"}  | [Yes](https://github.com/hippo5329/linorobot2_hardware/wiki#supported-sensors){:target="_blank"} | Yes    | To do|
|  [LD19/D300 LiDAR module,](https://s.click.aliexpress.com/e/_DchqT0p){:target="_blank"} | [Yes](https://github.com/hippo5329/linorobot2_hardware/wiki#supported-sensors){:target="_blank"}   | Never     |Never |
| [TOF Adafruit](https://www.adafruit.com/product/3317){:target="_blank"} or [Sparkfun](https://www.sparkfun.com/products/19013){:target="_blank"}   | Yes    | Yes   |[To do](https://github.com/kevinmcaleer/vl53l0x){:target="_blank"} |
| [OLED/Eyes - Zio](https://www.smart-prototyping.com/Zio-Qwiic-OLED-Display-1_5inch-128x128?search=oled){:target="_blank"}   | To do    | To do   |To do |
| [Line finder - ZIO](https://github.com/ZIOCC/Zio-Line-Finder-Qwiic-4-Transceivers-){:target="_blank"} | To do  | To do   | To do|
| [Servo - Zio](https://github.com/rosmo-robot/Qwiic_Servo_Driver_PCA9685/){:target="_blank"} for [mini arm](https://www.thingiverse.com/thing:5683010){:target="_blank"}  | To do   | To do   | To do|
| [LED - Zio](https://www.smart-prototyping.com/Zio-Qwiic-RGB-LED-APA102){:target="_blank"}  | To do  | To do   |To do   |
|  [Mecanum wheels (48mm)](https://www.aliexpress.com/item/1005005115563126.html){:target="_blank"} & [Adaptor](https://s.click.aliexpress.com/e/_Dm7R12P){:target="_blank"}| Yes    | To do    |To do   |
| [10mm Cube standoff](https://www.aliexpress.com/item/1005005880192495.html){:target="_blank"} | Yes   | Yes    |Yes   |
|  [Loader attachment (closed hardware)](https://www.dfrobot.com/product-2006.html){:target="_blank"} [Grabber attachment](https://www.dfrobot.com/product-2128.html){:target="_blank"}| To do   | Yes     | To do   |
| [1300 MikroBUS, other sensors (closed hardware)](https://hackaday.io/project/183129-rosmo-robot/log/227959-mikrobus-expansion){:target="_blank"}| partial   | partial    | partial|


<br>

  <video src="https://github.com/rosmo-robot/zio_demo/assets/400875/a9e81594-8d13-4ccd-9438-b3a10081cebc" controls="controls" style="max-width: 730px;"></video>

# Daughter boards

![](https://cdn.hackaday.io/images/9540661709561892794.png)
Mikrobus header can break out into a [add on board](https://easyeda.com/editor#id=532e49d109694babaa0abe71d380afd2){:target="_blank"} concept [here](https://hackaday.io/project/183129-rosmo-robot/log/227959-mikrobus-expansion){:target="_blank"}) students or others may want to design their own breakouts.

![](https://cdn.hackaday.io/images/2248281712336134786.png)


| Add on for breakouts          | ROS2 Linorobot                               | Microblocks | Micropython|
| ------------------------- | ----------------------------------------- | -------- |---------|
| [ESP32-S3 camera (closed hardware)](https://s.click.aliexpress.com/e/_DF0kUdn){:target="_blank"}| [Likely](https://github.com/FrankBu0616/esp32cam_ros)   | Untested  | Untested |
| [USBC power adaptor (closed hardware)](https://s.click.aliexpress.com/e/_DE0W3PJ){:target="_blank"}| Untested   | Untested  | Untested|
| [1.3" OLED](https://s.click.aliexpress.com/e/_DlBWIBB){:target="_blank"}|Untested| Untested|Untested|
| [Pimoroni SPI or I2C sensors](https://shop.pimoroni.com/collections/breakout-garden){:target="_blank"}|Untested| Untested|Untested|



I also did a breakout in a [Wemos D1 format](https://easyeda.com/editor#id=c77407793cf440ed92fb880dfeb9522a){:target="_blank"} as there are a good number of [cheap sensors available](https://s.click.aliexpress.com/e/_DD433Tb){:target="_blank"} in this footprint

![](https://raw.githubusercontent.com/rosmo-robot/rosmo/main/Images/V1/signal-2024-04-12-124516.jpeg)

## Schematic
Can be found [here](https://easyeda.com/editor#id=fe972d3133f048a3be8b1bbdfaf8a93f){:target="_blank"}

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/Schematic_open-robot-platform_2024-04-03.svg)


## Microblocks; Best if you're just starting

1) Download [ESP32-S3 bin](https://github.com/rosmo-robot/rosmo-robot.github.io/raw/master/assets/img/v1/vm_esp32_s3.bin)
   
3) Visit [ESP web tool](https://esp.huhn.me/)
   
5) Connect ESP32-S3 and flash device (you may need to hold the 'boot' button)
   
7) Use the [Pilot version in Chrome](https://microblocks.fun/run-pilot/microblocks.html){:target="_blank"}
   
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
  

##  Openbot (Android) software; Best if you want to explore affordable vision 

Status: Needs tweaking for ESP32S3

- Android app and Arduino for computer vision & AI
- [https://www.openbot.org](https://www.openbot.org/research)


## Micropython software
Status: Doesn't exist yet, 

Interest from author of [Otto Mecanum](https://github.com/UEA-envsoft/Otto-Mecanum) in adapting for Rosmo


## Arduino software
Status: Doesn't exist yet, 
Might be interesting to do something with [Arduino Mecanum](https://github.com/StormingMoose/DroneBot-Workshop-Mecanum-for-L9110S) and maybe [Smartcar Shield](https://github.com/platisd/smartcar_shield?tab=readme-ov-file#software) at some point


## Collaborators

I'd love to work with people on the software, give us a shout on Twitter or Hackaday.io if you're interested some [ideas here](https://hackaday.io/project/183129-rosmo-robot/log/227995-version-10-approaches-stuff-to-do-looking-for-collaborators)

## License

PCB is CERN-OHL-S
This documentation is CC-BY-4.0 unless otherwise noted on the page.

![](https://raw.githubusercontent.com/rosmo-robot/rosmo/main/Images/V1/signal-2024-04-11-210009.jpeg)

![](https://raw.githubusercontent.com/rosmo-robot/rosmo/main/Images/V1/signal-2024-04-11-205952.jpeg)


## Older photos of iteration process

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/claw.jpeg)


![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/zio.jpeg)

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/new.jpeg)

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/front.jpeg)

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/side-zio.jpeg)

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/signal-2023-12-03-173143.mp4)

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/pen.jpeg)


- 2WD

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/2wd-4wd.jpeg)
![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/2wd.jpeg)

 - 4WD/ Mecanum

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/4wd-side.jpeg)
![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/4wd.jpeg)

  
## Alternate IMU
-  [BMI270 6DOF](https://www.sparkfun.com/products/22398) [Micropthon](https://github.com/jposada202020/MicroPython_BMI270) [Arduino](https://registry.platformio.org/libraries/sparkfun/SparkFun%20BMI270%20Arduino%20Library)
- [IMU - LSM6DSOX](https://www.adafruit.com/product/4438) [Micropthon](https://github.com/jposada202020/MicroPython_LSM6DSOX) [Arduino](https://registry.platformio.org/libraries/sparkfun/SparkFun%20Qwiic%206Dof%20-%20LSM6DSO)
- [LSM6DSV16X 6DOF](https://www.sparkfun.com/products/21336) no Micropthon [Arduino](https://registry.platformio.org/libraries/sparkfun/SparkFun%206DoF%20LSM6DSV16X)
- [ISM330DHCX 6DOF A](https://www.sparkfun.com/products/20176) [ISM330DHCX 6DOF B](https://www.adafruit.com/product/4502) Micropthon Arduino


<video src="https://github.com/rosmo-robot/zio_demo/assets/400875/8500637e-e9ad-4a71-80ed-6da3dec69c0c" controls="controls" style="max-width: 730px;">
</video>



<video src="https://github.com/rosmo-robot/zio_demo/assets/400875/2a7d44ed-8b35-4954-bf69-88f5d1b43024" controls="controls" style="max-width: 730px;">
</video>

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/purple.jpeg)


![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/purplebattery.jpeg)
Top plate removed to expose battery layer
![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/purple-motor.jpeg)
Battery layer removed to expose motor controller, microcontroller, exposed motor/encoder connections. [Mikrobus click](https://www.mikroe.com/click?interface=analog,i2c,spi,analog,i2c,spi&categories*=sensors,display-and-led,interface,wireless-connectivity,sensors,display-and-led,interface,wireless-connectivity) footprint Not shown are screw terminals as I haven't soldered them yet.

    



