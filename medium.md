
![](https://raw.githubusercontent.com/rosmo-robot/rosmo-robot.github.io/master/assets/img/larger.png)

If you find you want a larger robot than the standard [100x80mm Rosmo platform](https://rosmo-robot.github.io/) this is a larger 170x110mm option that also uses the [Open Robotic Platform](https://openroboticplatform.com/designrules) mount holes. You'll note that most the electronics components are shared between this verson and the smaller bot, making an upgrade easy and affordable. You can also re-use the 100x80mm ESP32 mounting plate from the smaller robot to save soldering/fabrication cost.

## BOM 

Status: untested work in progeress

~£? ~$? for 4wd can be reduced, by using existing powerbank for example

| Components                | Description                               | Quantity |
| ------------------------- | ----------------------------------------- | -------- |
|  Rosmo-M Chassis Plates | [Custom PCB Chassis](https://easyeda.com/editor#id=2abad8a02be54c91a6b3277fe66bd864)     | 5       |
| Motors with encoder, mount & 65mm wheels     | [JGA25](https://www.aliexpress.com/item/1005006213247803.html) or [JGB-37](https://www.aliexpress.com/item/1005006410464479.html)         |      |
| Motor Driver              | [Zio H-bridge Motor Driver](https://www.smart-prototyping.com/Zio-4-DC-Motor-Controller.html?search=motor)          | 1        |
| Heatsinks for motor Driver              | [12x13x7mm](https://www.aliexpress.com/item/1005005311716183.html)          | 2       |
|  ESP32-S3-C1              | [Olimex open hardware](https://www.olimex.com/Products/IoT/ESP32-S3/ESP32-S3-DevKit-Lipo/open-source-hardware), [UK](https://thepihut.com/products/olimex-esp32-s3-devkit-lipo-development-board) [US](https://www.digikey.com/en/products/detail/olimex-ltd/ESP32-S3-DEVKIT-LIPO-EA/22157950) or [generic version](https://www.aliexpress.com/item/1005006028969168.html)        | 1        |
| USB powerbank           |[ battery case](https://www.aliexpress.com/item/1005005637445437.html) [1x or 2x 18650 battery](https://s.click.aliexpress.com/e/_DnPRBEj) or open hardware [18650 battery](https://oshwlab.com/wagiminator/fp6277-power-bank)        | 1        |
| 3x 18650           |[Batteries](https://s.click.aliexpress.com/e/_DdfBurF)         | 1        |
| 3S Lipo battery  | [~$21 2200Mah](https://www.aliexpress.com/item/1005001419560964.html) or [~$38 4000Mah](https://www.aliexpress.com/item/1005004335619259.html)  | 1        |
| 3S charger         |[USB charger](https://www.aliexpress.com/item/1005003240894835.html)         | 1        |
| XT60 > Barrel cable       |[power cable](https://s.click.aliexpress.com/e/_DDVjyhr)         | 1        |
|  Barrel> Screw terminal      |[barrel adaptor](https://s.click.aliexpress.com/e/_DDVjyhr)         | 1        |
| Battery> Motor driver cable         |[JST cable](https://s.click.aliexpress.com/e/_DDYfp6H)         | 2       |
| Qwiic cable             | [For connecting ESP32](https://www.aliexpress.com/item/1005005796723171.html)                      | 1        |
| Hex Spacers               | [45mm height M3 standoff](https://www.aliexpress.com/item/32539100523.html)          | 1    |
| M2 Bolts & nuts           | [400pc Bolt pack](https://www.aliexpress.com/item/1005002046118328.html)                                          | 1      |
| M3 Bolts  & nuts          | From Bolt pack                                          | 10        |
| Screw Driver              | 2 in 1 Flat and Philips Head Screw Driver | 1 |
| Optional (recommended) IMU | [MPU6500](https://www.adafruit.com/product/3886) or [BNO085](https://www.adafruit.com/product/4754)                                     | 2        |
| Optional LiDAR Kit for use with ROS2 |  [LiDAR module, USB Cable and Data Convertor Box](https://www.amazon.co.uk/DTOF-D300-Distance-Obstacle-Education/dp/B0B1V8D36H/ref=sr_1_1?crid=2BSZJ4XVN2S12&keywords=ld19+lidar&qid=1707070916&sprefix=ld19+lidar%2Caps%2C254&sr=8-1) | 1 |

Please refer to the [100x80mm Rosmo platform](https://rosmo-robot.github.io/) page for software information.
