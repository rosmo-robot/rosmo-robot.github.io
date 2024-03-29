---
layout: page
title: Rosmo
---
A Open-hardware micro-robot for ROS2 that can be assembled without soldering, or access to a 3D printer. Built from modular components on the [Open Robotic Platform rules](https://openroboticplatform.com/designrules)

Using affordable components available worldwide. For hobbyists, universities, R&D.

![](https://cdn.hackaday.io/images/2988771707607922324.jpeg)


## BOM 
~$62 for base 4wd can be reduced, by using existing powerbank for example. 

| Components latest v0.7 version              | Description                               | Quantity |
| ------------------------- | ----------------------------------------- | -------- |
| ~$12  Rosmo Chassis v0.7 with on-board motor driver | [Custom PCB Chassis](https://easyeda.com/editor#id=d1613b232be34ba19d8c2b5ff3585e13) for sale soon     | 1       |
| ~$32 Motor with encoder & wheel     | [6v 150RPM $Bringsmart motors](https://s.click.aliexpress.com/e/_DErxgYv)            | 4   |
| ~$6 motor cables    | [6Pin same direction cables](https://s.click.aliexpress.com/e/_DkjeS8V)            | 4   |
| ~$6 - $12 ESP32-S3-C1              | [Olimex open hardware](https://www.olimex.com/Products/IoT/ESP32-S3/ESP32-S3-DevKit-Lipo/open-source-hardware), [UK](https://thepihut.com/products/olimex-esp32-s3-devkit-lipo-development-board) [US](https://www.digikey.com/en/products/detail/olimex-ltd/ESP32-S3-DEVKIT-LIPO-EA/22157950) or [generic version](https://s.click.aliexpress.com/e/_DBbQjGl)        | 1        |
| ~$7 1x 2A powerbank        |[Powerbank](https://www.aliexpress.com/item/1005006593619440.html)        | 1        |
| ~$5 Hex Spacers               | [45mm height M3 standoff](https://www.aliexpress.com/item/32539100523.html)          | 1    |

List of these items on [Aliexpress](https://www.aliexpress.com/p/wishlist/shareReflux.html?groupId=H3r6Ix9p3i%2BvbdGhQpxk4NMRKh%2F%2Bgiup4z2X0odX6os%3D)


## Optional extras



| Add on           | ROS2 Linorobot                               | Microblocks | Micropython|
| ------------------------- | ----------------------------------------- | -------- |---------|
|  [MPU6050 IMU](https://www.adafruit.com/product/3886) | Yes    | Yes   | To do |
|  [BNO085 IMU](https://www.adafruit.com/product/4754) | Yes   | To do    |To do |
|  [Ultrasonic - ZIO](https://github.com/ZIOCC/Zio-Qwiic-Ultrasonic-Distance-Sensor)  | Yes | Yes    | To do|
|  [LiDAR module, USB Cable and Data Convertor Box (ROS2)](https://s.click.aliexpress.com/e/_DchqT0p) | Yes    | Never     |To do |
| [TOF Adafruit](https://www.adafruit.com/product/3317) or [Sparkfun](https://www.sparkfun.com/products/19013)   | Yes    | Yes   |To do |
| [MikroBUS, UEXT or Breakout Garden sensors](https://hackaday.io/project/183129-rosmo-robot/log/227959-mikrobus-expansion)| Some    | Some    | To do|
| [OLED/Eyes - Zio](https://www.smart-prototyping.com/Zio-Qwiic-OLED-Display-1_5inch-128x128?search=oled)   | To do    | To do   |To do |
| [Line finder - ZIO](https://github.com/ZIOCC/Zio-Line-Finder-Qwiic-4-Transceivers-) | To do  | To do   | To do|
| [Servo - Zio](https://github.com/rosmo-robot/Qwiic_Servo_Driver_PCA9685/) for [mini arm](https://www.thingiverse.com/thing:5683010)  | To do   | To do   | To do|
| [LED - Zio](https://www.smart-prototyping.com/Zio-Qwiic-RGB-LED-APA102)  | To do  | To do   |To do   |
|  [Mecanum wheels (48mm)](https://www.aliexpress.com/item/1005005115563126.html)| Yes    | To do    |To do   |
| [10mm Cube standoff](https://www.aliexpress.com/item/1005005880192495.html) | Yes   | Yes    |To do   |
|  [Loader attachment (closed hardware)](https://www.dfrobot.com/product-2006.html) [Grabber attachment](https://www.dfrobot.com/product-2128.html)| To do   | Yes     | To do   |






  <video src="https://github.com/rosmo-robot/zio_demo/assets/400875/a9e81594-8d13-4ccd-9438-b3a10081cebc" controls="controls" style="max-width: 730px;"></video>


## Microblocks Software - Best if you're just starting

<video src="https://github.com/rosmo-robot/zio_demo/assets/400875/4d8f3e58-93ae-484d-b4bf-076c96f3a7d6" controls="controls" style="max-width: 730px;"></video>


Current status: Working but you have to build in Platformio to get ESP32-S3 support

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/microblocks.png)

- Provides a block programing interface 

- Provides an [Android app](http://www.microblocks.fun/wifigamepad/gamepadwifiremote.apk)  for remote control & [detailed instructions](http://www.microblocks.fun/en/wifi/gamepad)

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/wsgamepad-start.jpg)

Use the [Pilot version](https://microblocks.fun/download) from the bottom of the downloads page. Then to quickly get started download this raw [UBP file](https://github.com/rosmo-robot/rosmo-robot.github.io/blob/master/assets/img/ziopublicwifiremote.ubp) and open it in the Microblocks app.

## ROS 2 software - Best if you want to learn ROS2

Current status: I2C comms with Zio driver established and wheel spinning, but not working fully yet 
  
- [Linorobot2](https://github.com/hippo5329/linorobot2_hardware/tree/esp32s3-lipo-zio) Zio driver now supported.
- [Virtual machine for download](https://drive.google.com/file/d/1itU1ZYsxZf3GO9LMmP3NauBo0db6XsqN/view?usp=sharing) Ubuntu 22.04 with ROS2/Linorobot. For use with [Virtualbox](https://www.virtualbox.org/wiki/Downloads) 
- On a Linux host; sudo adduser $YOUR-USER vboxusers then follow [this guide](https://roboticsbackend.com/control-arduino-from-ubuntu-virtualbox/) reboot your computer
- cd /linorobot2_hardware/config/custom
- nano esp32s3_wifi_config.h put in your wifi credentials near the bottom of the file, set the agent IP to the address of your computer
- cd /linorobot2_hardware/firmware
- pio run -e esp32s3_wifi -t upload
-  ros2 launch linorobot2_bringup bringup.launch.py micro_ros_transport:=udp4 micro_ros_port:=8888

Notes on Virtualbox 
- git clone --branch esp32s3-lipo-zio https://github.com/hippo5329/linorobot2_hardware.git

## Openbot software (Android) - Best if you want to explore affordable vision 

- Android app and Arduino for computer vision & AI
- [https://www.openbot.org](https://www.openbot.org/research)

## Micropython software
Doesn't exist yet, might be interesting to do something with [Otto Mecanum](https://github.com/UEA-envsoft/Otto-Mecanum)

## Arduino software
Doesn't exist yet, might be interesting to do something with [Smartcar Shield](https://github.com/platisd/smartcar_shield?tab=readme-ov-file#software) at some point


![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/claw.jpeg)


![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/zio.jpeg)

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/new.jpeg)

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/front.jpeg)

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/side-zio.jpeg)

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/signal-2023-12-03-173143.mp4)

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/pen.jpeg)




  ## Configurations
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


## Older iterations

| Components for older v0.6 version               | Description                               | Quantity |
| ------------------------- | ----------------------------------------- | -------- |
| ~$8 Rosmo Chassis  | [Custom PCB Chassis](https://easyeda.com/editor#id=72fd738aaf6c4f808593c5e1d56507f3) get fabricated at JLPCB, or solder your own     | 5       |
| Motor Driver   | [Zio H-bridge Motor Driver](https://www.smart-prototyping.com/Zio-4-DC-Motor-Controller.html?search=motor)          | 1        |
| Optional IMU | [MPU6500](https://www.adafruit.com/product/3886) or [BNO085](https://www.adafruit.com/product/4754)                                     | 2        |
| USB powerbank           |[ battery case](https://www.aliexpress.com/item/1005005637445437.html) [1x or 2x 18650 battery](https://s.click.aliexpress.com/e/_DnPRBEj) or open hardware [18650 battery](https://oshwlab.com/wagiminator/fp6277-power-bank)        | 1        |
| USB > Motor driver cable         |[JST cable](https://s.click.aliexpress.com/e/_DnMT6K5)         | 1        |
| M2 Bolts & nuts           | [400pc Bolt pack](https://www.aliexpress.com/item/1005002046118328.html)                                          | 1      |
| Screw Driver              | 2 in 1 Flat and Philips Head Screw Driver | 1 |
| JST zh 1.5mm, 80mm        |[) Double headed 6pin cable](https://s.click.aliexpress.com/e/_DBkMOpT)        | 1 pack        |
| Qwiic> Qwiic cable             | [For connecting ESP32](https://www.aliexpress.com/item/1005005796723171.html)                      | 1        |

If you don't get JLPCB to fabricate the PCB you'll also need some 2.54mm screw terminals or a breadboard [For connecting encoder](https://www.aliexpress.com/item/1005001677869988.html)

Note a previous iteration of this project used the Pi Pico dimensions, if you wanted that the [PCB is here](https://easyeda.com/editor#id=69415ef7785b4ad29ea97032be2ffa39)


Parts for v0.6 excluding PCB and motor driver are available on this [List](https://www.aliexpress.com/p/wishlist/shareReflux.html?groupId=H3r6Ix9p3i%2BvbdGhQpxk4HzpYMoqXal2lBW1GCdCX4A%3D) ensure you get correct quantities, eg 4x wheels and motors. 


<video src="https://github.com/rosmo-robot/zio_demo/assets/400875/2a7d44ed-8b35-4954-bf69-88f5d1b43024" controls="controls" style="max-width: 730px;">
</video>

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/purple.jpeg)


![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/purplebattery.jpeg)
Top plate removed to expose battery layer
![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/purple-motor.jpeg)
Battery layer removed to expose motor controller, microcontroller, exposed motor/encoder connections. [Mikrobus click](https://www.mikroe.com/click?interface=analog,i2c,spi,analog,i2c,spi&categories*=sensors,display-and-led,interface,wireless-connectivity,sensors,display-and-led,interface,wireless-connectivity) footprint Not shown are screw terminals as I haven't soldered them yet.

    



