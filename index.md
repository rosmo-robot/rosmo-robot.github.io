---
layout: page
title: Rosmo
---
A Open-hardware micro-robot for ROS2 that can be assembled without soldering, or access to a 3D printer. 

Built using affordable components available worldwide. For hobbyists, universities, R&D.

![](https://cdn.hackaday.io/images/2988771707607922324.jpeg)


## BOM 
~£60 ~$75 for 4wd can be reduced, by using existing powerbank for example

| Components                | Description                               | Quantity |
| ------------------------- | ----------------------------------------- | -------- |
|  Rosmo Chassis Plates | [Custom PCB Chassis](https://easyeda.com/editor#id=3403ce9a81fe4425908f98d88d95e6c7) get fabricated at JLPCB, or solder your own     | 5       |
| Motor with encoder     | [6v 150RPM $Bringsmart motors](https://s.click.aliexpress.com/e/_DC72ruf) or [$$Pololu](https://www.pololu.com/category/60/micro-metal-gearmotors)              | 2        |
| Motor Driver              | [Zio H-bridge Motor Driver](https://www.smart-prototyping.com/Zio-4-DC-Motor-Controller.html?search=motor)          | 1        |
|  ESP32-S3-C1              | [Olimex open hardware](https://www.olimex.com/Products/IoT/ESP32-S3/ESP32-S3-DevKit-Lipo/open-source-hardware), [UK](https://thepihut.com/products/olimex-esp32-s3-devkit-lipo-development-board) [US](https://www.digikey.com/en/products/detail/olimex-ltd/ESP32-S3-DEVKIT-LIPO-EA/22157950) or [generic version](https://www.aliexpress.com/item/1005006028969168.html)        | 1        |
| N20 Wheel            | [N20 rubber wheels](https://s.click.aliexpress.com/e/_DBjDZqx) or [3mm shaft Mecanum wheels A](https://www.aliexpress.com/item/1005003264388589.html),[B](https://www.aliexpress.com/item/32977691906.html) or [C](https://www.thingiverse.com/thing:1358552)          | 4   |
| Motor mount   | [N20 mounts](https://s.click.aliexpress.com/e/_Dm7LWRD) | 1        |
| USB powerbank           |[ battery case](https://www.aliexpress.com/item/1005005637445437.html) [1x or 2x 18650 battery](https://s.click.aliexpress.com/e/_DnPRBEj) or open hardware [18650 battery](https://oshwlab.com/wagiminator/fp6277-power-bank)        | 1        |
| 3x 18650           |[Batteries](https://s.click.aliexpress.com/e/_DdfBurF)         | 1        |
| USB > Motor driver cable         |[JST cable](https://www.aliexpress.com/item/1005004192966816.html)         | 1        |
| Qwiic cable             | [For connecting ESP32](https://www.aliexpress.com/item/1005005796723171.html)                      | 1        |
| Hex Spacers               | [45mm height M3 standoff](https://www.aliexpress.com/item/32539100523.html)          | 1    |
| M2 Bolts & nuts           | [400pc Bolt pack](https://www.aliexpress.com/item/1005002046118328.html)                                          | 1      |
| M3 Bolts  & nuts          | From Bolt pack                                          | 10        |
| Screw Driver              | 2 in 1 Flat and Philips Head Screw Driver | 1 |
| Optional IMU | [MPU6500](https://www.adafruit.com/product/3886) or [BNO085](https://www.adafruit.com/product/4754)                                     | 2        |
| Optional LiDAR Kit for use with ROS2 |  [LiDAR module, USB Cable and Data Convertor Box](https://www.amazon.co.uk/DTOF-D300-Distance-Obstacle-Education/dp/B0B1V8D36H/ref=sr_1_1?crid=2BSZJ4XVN2S12&keywords=ld19+lidar&qid=1707070916&sprefix=ld19+lidar%2Caps%2C254&sr=8-1) | 1 |

Parts excluding PCB and motor driver are available on this [List](https://www.aliexpress.com/p/wishlist/shareReflux.html?groupId=H3r6Ix9p3i%2BvbdGhQpxk4HzpYMoqXal2lBW1GCdCX4A%3D) ensure you get correct quantities, eg 4x wheels and motors. 

If you don't get JLPCB to fabricate the PCB you'll also need some 2.54mm screw terminals or a breadboard [For connecting encoder](https://www.aliexpress.com/item/1005001677869988.html)

Note a previous iteration of this project used the Pi Pico dimensions, if you wanted that the [PCB is here](https://easyeda.com/editor#id=69415ef7785b4ad29ea97032be2ffa39)

## Optional extras
- [Loader attachment (closed hardware)](https://www.dfrobot.com/product-2006.html) [Grabber attachment](https://www.dfrobot.com/product-2128.html)
- [10mm Cube standoff](https://www.aliexpress.com/item/1005005880192495.html)
- [TOF Adafruit](https://www.adafruit.com/product/3317) or [Sparkfun](https://www.sparkfun.com/products/19013)
- [OLED/Eyes - Zio](https://www.smart-prototyping.com/Zio-Qwiic-OLED-Display-1_5inch-128x128?search=oled)
- [Line finder - ZIO](https://github.com/ZIOCC/Zio-Line-Finder-Qwiic-4-Transceivers-)
- [Ultrasonic - ZIO](https://github.com/ZIOCC/Zio-Qwiic-Ultrasonic-Distance-Sensor) 
- [Servo - Zio](https://github.com/rosmo-robot/Qwiic_Servo_Driver_PCA9685/) for [mini arm](https://www.thingiverse.com/thing:5683010)
- [LED - Zio](https://www.smart-prototyping.com/Zio-Qwiic-RGB-LED-APA102)
- [On-board compute. Beagleboard Play](https://www.beagleboard.org/boards/beagleplay)
- [Camera - Maxlab](https://github.com/maxlab-io/tokay-lite-pcb) or OpenMV

  <video src="https://github.com/rosmo-robot/zio_demo/assets/400875/a9e81594-8d13-4ccd-9438-b3a10081cebc" controls="controls" style="max-width: 730px;"></video>


## Microblocks Software - Best if you're just starting

<video src="https://github.com/rosmo-robot/zio_demo/assets/400875/4d8f3e58-93ae-484d-b4bf-076c96f3a7d6" controls="controls" style="max-width: 730px;"></video>


Current status: Working but you have to build in Platformio to get ESP32-S3 support

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/microblocks.png)

- Provides a block programing interface 

- Provides an [Android app](http://www.microblocks.fun/wifigamepad/gamepadwifiremote.apk)  for remote control & [detailed instructions](http://www.microblocks.fun/en/wifi/gamepad)

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/wsgamepad-start.jpg)

Use the [Pilot version](https://microblocks.fun/download) from the bottom of the downloads page. Then to quickly get started download this raw [UBP file](https://github.com/rosmo-robot/rosmo-robot.github.io/blob/master/assets/img/ziopublicwifiremote.ubp) and open it in the Microblocks app.

## Ros2 - Best if you want to learn ROS2

Current status: I2C comms with Zio driver established and wheel spinning, but not working fully yet 
  
- [Linorobot2](https://github.com/hippo5329/linorobot2_hardware/tree/esp32_zio) Zio driver now supported.
- [Virtual machine for download](https://drive.google.com/file/d/1itU1ZYsxZf3GO9LMmP3NauBo0db6XsqN/view?usp=sharing) Ubuntu 22.04 with ROS2/Linorobot. For use with [Virtualbox](https://www.virtualbox.org/wiki/Downloads) 
- On a Linux host; sudo adduser $YOUR-USER vboxusers then follow [this guide](https://roboticsbackend.com/control-arduino-from-ubuntu-virtualbox/) reboot your computer
- nano /linorobot2_hardware/config/custom put in your wifi credentials near the bottom of the file, set the agent IP to the address of your computer
- cd /linorobot2_hardware/firmware
- pio run -e esp32_zio -t upload
-  ros2 launch linorobot2_bringup bringup.launch.py micro_ros_transport:=udp4 micro_ros_port:=8888

## Micropython
Doesn't exist yet, might be interesting to do something with [ESP32_Car_Platform](https://github.com/jppang/ESP32_Car_Platform/tree/main/software) & [Motor driver code](https://github.com/ZIOCC/Qwiic_4-Ch_DC_Motor_Controller/tree/master/micropython) at some point

## Arduino 
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

<video src="https://github.com/rosmo-robot/zio_demo/assets/400875/2a7d44ed-8b35-4954-bf69-88f5d1b43024" controls="controls" style="max-width: 730px;">
</video>

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/purple.jpeg)


![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/purplebattery.jpeg)
Top plate removed to expose battery layer
![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/purple-motor.jpeg)
Battery layer removed to expose motor controller, microcontroller, exposed motor/encoder connections. [Mikrobus click](https://www.mikroe.com/click?interface=analog,i2c,spi,analog,i2c,spi&categories*=sensors,display-and-led,interface,wireless-connectivity,sensors,display-and-led,interface,wireless-connectivity) footprint Not shown are screw terminals as I haven't soldered them yet.

    



