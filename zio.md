---
layout: page
title: Ziobot
---
Open hardware ROS2 robot.

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/claw.jpeg)


<video src="https://github.com/rosmo-robot/zio_demo/assets/400875/2a7d44ed-8b35-4954-bf69-88f5d1b43024" controls="controls" style="max-width: 730px;">
</video>

## BOM 


| Components                | Description                               | Quantity |
| ------------------------- | ----------------------------------------- | -------- |
| Ziobot ORP Chassis Plates | [Custom PCB Chassis](https://easyeda.com/editor#id=144a1a06572f48fca974494ad7a75ebc) get [fabricated at JLPCB](https://passport.jlcpcb.com/#/login?response_type=code&client_id=34495309ae47483ebf71827b5bcb591c&redirect_url=https%3A%2F%2Fjlcpcb.com%2Fquote%2Feda%3FeadLink%3D2%2526uuid%3D14228fde15ff42158045d32f5a947a14&state=RDPqofFaHWeXoV4oRNQJkmP28Dy7Dc1pSmrNnbR2%2BoK0iuZDs8YBVdB29kKNa7AN6AUwv9Yt%2FNXdQpHICFCsDw%3D%3D&from=jlcpcb), or solder your own     | 5       |
| BO Motor with encoder     | [6v 150RPM $Bringsmart motors](https://s.click.aliexpress.com/e/_DC72ruf) or [$$Pololu](https://www.pololu.com/category/60/micro-metal-gearmotors)              | 2        |
| Motor Driver              | [Zio H-bridge Motor Driver](https://www.smart-prototyping.com/Zio-4-DC-Motor-Controller.html?search=motor)          | 1        |
|  ESP32-S3-C1              | [Olimex open hardware](https://www.olimex.com/Products/IoT/ESP32-S3/ESP32-S3-DevKit-Lipo/open-source-hardware) or [generic version](https://www.aliexpress.com/item/1005006028969168.html)        | 1        |
| N20 Wheel            | [N20 rubber wheels](https://s.click.aliexpress.com/e/_DBjDZqx) or [3mm shaft Mecanum wheels A](https://www.aliexpress.com/item/1005003264388589.html),[B](https://www.aliexpress.com/item/32977691906.html) or [C](https://www.thingiverse.com/thing:1358552)          | 4   |
| Motor mount         | [N20 mounts](https://s.click.aliexpress.com/e/_Dm7LWRD)
| USB powerbank           |[ battery case](https://www.aliexpress.com/item/1005005637445437.html) [1x or 2x 18650 battery](https://s.click.aliexpress.com/e/_DnPRBEj) or open hardware [18650 battery](https://oshwlab.com/wagiminator/fp6277-power-bank)        | 1        |
| 3x 18650           |[Batteries](https://s.click.aliexpress.com/e/_DdfBurF)         | 1        |
| USB > Motor driver cable         |[JST cable](https://www.aliexpress.com/item/1005004192966816.html)         | 1        |
| Qwiic cable             | [For connecting ESP32](https://www.aliexpress.com/item/1005005796723171.html)                      | 1        |
| 2.54mm screw terminals      | [For connecting encoder](https://www.aliexpress.com/item/1005001677869988.html)                      | 4       |
| Hex Spacers               | [45mm height M3 standoff](https://www.aliexpress.com/item/32539100523.html)          | 18       |
| M3 10 mm Bolts            | [Bolt pack](https://www.aliexpress.com/item/1005002046118328.html)                                          | 40       |
| M3 25 mm Bolts            | From Bolt pack                                          | 4        |
| M3 Nuts                   | From Bolt pack                                          | 44       |
| M3 Washers                | From Bolt pack                                          | 4        |
| M2 10 mm Bolts            | From Bolt pack                                         | 2        |
| M2 Nuts                   | From Bolt pack                                        | 2        |
| Screw Driver              | 2 in 1 Flat and Philips Head Screw Driver with Tester | 1 |
| Optional IMU                   | [MPU6500](https://www.adafruit.com/product/3886) or [BNO085](https://www.adafruit.com/product/4754)                                     | 2        |
| Optional LiDAR Kit                 |  [LiDAR module, USB Cable and Data Convertor Box](https://www.amazon.co.uk/DTOF-D300-Distance-Obstacle-Education/dp/B0B1V8D36H/ref=sr_1_1?crid=2BSZJ4XVN2S12&keywords=ld19+lidar&qid=1707070916&sprefix=ld19+lidar%2Caps%2C254&sr=8-1) | 1 |


Note a previous iteration of this project used the Pi Pico dimensions, if you wanted that the [PCB is here](https://easyeda.com/editor#id=69415ef7785b4ad29ea97032be2ffa39)

## Optional extras
- [10mm Cube standoff](https://www.aliexpress.com/item/1005005880192495.html)
- [TOF Adafruit](https://www.adafruit.com/product/3317) [Zio](https://www.smart-prototyping.com/Zio/Zio-TOF-Distance-Sensor-RFD77402.html) or [Sparkfun](https://www.sparkfun.com/products/19013)
- [OLED/Eyes - Zio](https://www.smart-prototyping.com/Zio-Qwiic-OLED-Display-1_5inch-128x128?search=oled)
- [Line finder - ZIO](https://github.com/ZIOCC/Zio-Line-Finder-Qwiic-4-Transceivers-)
- [Ultrasonic - ZIO](https://github.com/ZIOCC/Zio-Qwiic-Ultrasonic-Distance-Sensor) 
- [Servo - Zio](https://github.com/rosmo-robot/Qwiic_Servo_Driver_PCA9685/) for [mini arm](https://www.thingiverse.com/thing:5683010)
- [LED - Zio](https://www.smart-prototyping.com/Zio-Qwiic-RGB-LED-APA102)
- [On-board compute. Beagleboard Play](https://www.beagleboard.org/boards/beagleplay)
- [Camera - Maxlab](https://github.com/maxlab-io/tokay-lite-pcb) or OpenMV
- [Loader attachment (closed hardware)](https://www.dfrobot.com/product-2006.html) [Grabber attachment](https://www.dfrobot.com/product-2128.html)


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

  

## Software WIP
- [Platformio C++ demo](https://github.com/rosmo-robot/zio_demo)
- [Webui remote control](https://github.com/donskytech/platformio-projects/tree/main/esp32-projects/esp32-robot-car-websockets)
- 4WD [Microblocks](https://discord.gg/TCpHYbcvkS )
- 4WD/ Mecanum ROS2 [Linorobot2](https://github.com/hippo5329/linorobot2_hardware/blob/master/config/custom/pico_zio_config.h)

## Alternate MCU
 - [Olimex S3](https://www.olimex.com/Products/IoT/ESP32-S3/ESP32-S3-DevKit-Lipo/open-source-hardware) & Qwiic cable or any other board with a Qwiic and sufficient pins to handle 8x encoder signal. eg 
 - [unexpected maker pro or feather](https://esp32s3.com/)

## Alternate IMU
-  [BMI270 6DOF](https://www.sparkfun.com/products/22398) [Micropthon](https://github.com/jposada202020/MicroPython_BMI270) [Arduino](https://registry.platformio.org/libraries/sparkfun/SparkFun%20BMI270%20Arduino%20Library)
   - [IMU - LSM6DSOX](https://www.adafruit.com/product/4438) [Micropthon](https://github.com/jposada202020/MicroPython_LSM6DSOX) [Arduino](https://registry.platformio.org/libraries/sparkfun/SparkFun%20Qwiic%206Dof%20-%20LSM6DSO)
  - [LSM6DSV16X 6DOF](https://www.sparkfun.com/products/21336) no Micropthon [Arduino](https://registry.platformio.org/libraries/sparkfun/SparkFun%206DoF%20LSM6DSV16X)
  - [ISM330DHCX 6DOF A](https://www.sparkfun.com/products/20176) [ISM330DHCX 6DOF B](https://www.adafruit.com/product/4502) Micropthon Arduino


<video src="https://github.com/rosmo-robot/zio_demo/assets/400875/8500637e-e9ad-4a71-80ed-6da3dec69c0c" controls="controls" style="max-width: 730px;">
</video>



## Older iterations

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/purple.jpeg)


![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/purplebattery.jpeg)
Top plate removed to expose battery layer
![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/purple-motor.jpeg)
Battery layer removed to expose motor controller, microcontroller, exposed motor/encoder connections. [Mikrobus click](https://www.mikroe.com/click?interface=analog,i2c,spi,analog,i2c,spi&categories*=sensors,display-and-led,interface,wireless-connectivity,sensors,display-and-led,interface,wireless-connectivity) footprint Not shown are screw terminals as I haven't soldered them yet.

    



