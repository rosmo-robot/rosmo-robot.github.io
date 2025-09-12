---
layout: page
title: Rosmo
---
 
A micro-robot for ROS2 & Microblocks that can be assembled without soldering, or access to a 3D printer. 
An affordable, adaptable, and open-source robot, for students, makers, universities, R&D.

![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/v1/0.8-side.jpeg)

If you'd like one please sign up for [Tindie waitlist](https://www.tindie.com/products/rosmo-robot/rosmo-robot-kit/)

Status: Works will be selling them early in 2025

## Parts list

| Part             | Description                               | Quantity |
| ------------------------- | ----------------------------------------- | -------- |
| ~$12  Rosmo Chassis | [Custom PCB Chassis](https://easyeda.com/editor#id=d247ef6dfe8843e298bc970c2c421022){:target="_blank"} for sale soon  | 1       |
| ~$16-$32 Motors with encoder & wheel     | [6v 150RPM $Bringsmart motors](https://s.click.aliexpress.com/e/_oo2BJ5Z){:target="_blank"} also sold by [Adafruit/mouser](https://www.mouser.co.uk/ProductDetail/Adafruit/4639?qs=DPoM0jnrROWCfj%252BnzBxvKw%3D%3D)  [wheel](https://www.aliexpress.com/item/1005006390888492.html)          | 2 or 4   |
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
|  [vl53l5cx](https://www.sparkfun.com/products/18642) | To do | Yes | [To do](https://github.com/kevinmcaleer/smars_inventor/blob/main/vl53l1x.py)
|  [BNO055 IMU](https://www.adafruit.com/product/4646){:target="_blank"} | [Yes](https://github.com/linorobot/linorobot2_hardware/issues/21#issuecomment-1567868751){:target="_blank"}   | To do    |To do |
|  [Ultrasonic - ZIO](https://github.com/ZIOCC/Zio-Qwiic-Ultrasonic-Distance-Sensor){:target="_blank"}  | [Yes](https://github.com/hippo5329/linorobot2_hardware/wiki#supported-sensors){:target="_blank"} | Yes    | Yes|
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

    



