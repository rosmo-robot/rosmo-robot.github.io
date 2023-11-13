---
layout: page
title: Ziobot
---

Developing ideas from the [XRP-X4](https://rosmo-robot.github.io/learn-robotics/)

Trying to have a less weird footprint than the XRP-X4, but keeping within 100mm x 100mm. 

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/purple.jpeg)
Top plate in place

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/purplebattery.jpeg)
Top plate removed to expose battery layer

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/purple-motor.jpeg)
Battery layer removed to expose motor controller, microcontroller, exposed motor/encoder connections. [Mikrobus click](https://www.mikroe.com/click?interface=analog,i2c,spi,analog,i2c,spi&categories*=sensors,display-and-led,interface,wireless-connectivity,sensors,display-and-led,interface,wireless-connectivity) footprint Not shown are screw terminals as I haven't soldered them yet.

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/weird-board.png)
Next iteration will be narrower and attempts to abstract the microcontroller so it's compatible with many dev boards



## Tentative BOM 

- 5 pieces [PCB plate](https://easyeda.com/editor#id=a7b537fbb9da40e5b189efd041921d19) fabricated, or not depending on user preference/budget
- 1 ESP32-S3 [Pico S3](https://www.nologo.tech/product/esp32/esp32s3Pico/esp32S3Pico.html?spm=a2g0s.imconversation.0.0.33073e5fnnUtHY) or [Olimex S3](https://www.olimex.com/Products/IoT/ESP32-S3/ESP32-S3-DevKit-Lipo/open-source-hardware) & Qwiic cable or any other board with a Qwiic and sufficient pins to handle 8x encoder signal. eg [unexpected maker pro or feather](https://esp32s3.com/)
- [Zio motor driver](https://www.smart-prototyping.com/Zio-4-DC-Motor-Controller.html?search=motor)
- 2x or 4x [6v 150RPM Bringsmart motors](https://s.click.aliexpress.com/e/_DC72ruf)
- 2x or 4x [N20 rubber wheels](https://s.click.aliexpress.com/e/_DBjDZqx) or [3mm shaft Mecanum wheels A](https://www.aliexpress.com/item/1005003264388589.html),[B](https://www.aliexpress.com/item/32977691906.html) or [C](https://www.thingiverse.com/thing:1358552)
- 2x or 4x [N20 mounts](https://s.click.aliexpress.com/e/_Dm7LWRD)
- 1x pack [18mm female standoffs](https://www.aliexpress.com/item/32539100523.html)
- 1x [Qwiic > Male pin cable](https://www.aliexpress.com/item/1005005796723171.html)
- 1x pack [M3 x 6mm screw](https://www.aliexpress.com/item/32539100523.html)
- [1x or 2x 18650 battery](https://s.click.aliexpress.com/e/_DnPRBEj) or open hardware [18650 battery](https://oshwlab.com/wagiminator/fp6277-power-bank)

## Configurations
- 2WD
- 4WD
- Mecanum

## Optional extras
- [Pico breakout](https://kitronik.co.uk/products/5341-kitronik-pin-breakout-for-the-raspberry-pi-pico) (no soldering robot)
- [10mm Cube standoff](https://www.aliexpress.com/item/1005005880192495.html)
- TOF Zio or [Sparkfun](https://www.sparkfun.com/products/19013)
- [2x OLED/Eyes - Zio](https://www.adafruit.com/product/5297#description)
- [Line finder - ZIO](https://github.com/ZIOCC/Zio-Line-Finder-Qwiic-4-Transceivers-)
- [Ultrasonic - ZIO](https://github.com/ZIOCC/Zio-Qwiic-Ultrasonic-Distance-Sensor) 
- [Servo - Zio](https://github.com/rosmo-robot/Qwiic_Servo_Driver_PCA9685/) for [mini arm](https://www.thingiverse.com/thing:5683010)
- [On-board compute. Beagleboard Play](https://www.beagleboard.org/boards/beagleplay)
- [Camera - Maxlab](https://github.com/maxlab-io/tokay-lite-pcb) or OpenMV
- [LED - Zio](https://www.smart-prototyping.com/Zio-Qwiic-RGB-LED-APA102)
- IMU TBC
  - [LSM6DSOX](https://www.adafruit.com/product/4438) [Micropthon](https://github.com/jposada202020/MicroPython_LSM6DSOX) [Arduino](https://registry.platformio.org/libraries/sparkfun/SparkFun%20Qwiic%206Dof%20-%20LSM6DSO)
  -  [BMI270 6DOF](https://www.sparkfun.com/products/22398) [Micropthon](https://github.com/jposada202020/MicroPython_BMI270) [Arduino](https://registry.platformio.org/libraries/sparkfun/SparkFun%20BMI270%20Arduino%20Library)
  - [LSM6DSV16X 6DOF](https://www.sparkfun.com/products/21336) no Micropthon [Arduino](https://registry.platformio.org/libraries/sparkfun/SparkFun%206DoF%20LSM6DSV16X)
  - [ISM330DHCX 6DOF A](https://www.sparkfun.com/products/20176) [ISM330DHCX 6DOF B](https://www.adafruit.com/product/4502) Micropthon Arduino

## Software todo
- Simple [Webui remote control](https://github.com/rosmo-robot/ESP32-robot-car-controller)
- 4WD [Bipes](https://bipes.net.br/ide/)
- 2WD ROS2 [Hadabot](https://www.hadabot.com/build-learn.html)
- 4WD/ Mecanum ROS2 [Linorobot2](https://github.com/rosmo-robot/linorobot2_hardware_hippo_esp32_fix/tree/master)



