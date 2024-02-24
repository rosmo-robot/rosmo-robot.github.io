## Rosmo Medium

If you find you want a larger robot than the standard 10x8cm platform this is a larger option. You'll note that the electronics components are shared between this verson and the smaller bot. You can also re-use the 10x8 mounting plate from the smaller robot to save soldering/fabrication

## BOM 
~£? ~$? for 4wd can be reduced, by using existing powerbank for example

| Components                | Description                               | Quantity |
| ------------------------- | ----------------------------------------- | -------- |
|  Rosmo-M Chassis Plates | [Custom PCB Chassis](https://easyeda.com/editor#id=144a1a06572f48fca974494ad7a75ebc) get [fabricated at JLPCB](https://passport.jlcpcb.com/#/login?response_type=code&client_id=34495309ae47483ebf71827b5bcb591c&redirect_url=https%3A%2F%2Fjlcpcb.com%2Fquote%2Feda%3FeadLink%3D2%2526uuid%3D14228fde15ff42158045d32f5a947a14&state=RDPqofFaHWeXoV4oRNQJkmP28Dy7Dc1pSmrNnbR2%2BoK0iuZDs8YBVdB29kKNa7AN6AUwv9Yt%2FNXdQpHICFCsDw%3D%3D&from=jlcpcb), or solder your own     | 5       |
| Motors with encoder, mount & 65mm wheels     | (JGA25](https://www.aliexpress.com/item/1005006213247803.html) [JGB-37](https://www.aliexpress.com/item/1005004242997257.html)         |      |
| Motor Driver              | [Zio H-bridge Motor Driver](https://www.smart-prototyping.com/Zio-4-DC-Motor-Controller.html?search=motor)          | 1        |
|  ESP32-S3-C1              | [Olimex open hardware](https://www.olimex.com/Products/IoT/ESP32-S3/ESP32-S3-DevKit-Lipo/open-source-hardware), [UK](https://thepihut.com/products/olimex-esp32-s3-devkit-lipo-development-board) [US](https://www.digikey.com/en/products/detail/olimex-ltd/ESP32-S3-DEVKIT-LIPO-EA/22157950) or [generic version](https://www.aliexpress.com/item/1005006028969168.html)        | 1        |
| USB powerbank           |[ battery case](https://www.aliexpress.com/item/1005005637445437.html) [1x or 2x 18650 battery](https://s.click.aliexpress.com/e/_DnPRBEj) or open hardware [18650 battery](https://oshwlab.com/wagiminator/fp6277-power-bank)        | 1        |
| 3x 18650           |[Batteries](https://s.click.aliexpress.com/e/_DdfBurF)         | 1        |
| 33S Lipo battery 135mm*42mm*25mm 304g [~$21 2200Mah](https://www.aliexpress.com/item/1005001419560964.html) > [~$38 4000Mah](https://www.aliexpress.com/item/1005004335619259.html) 135x42x21      | 1        |
| 3S charger         |[USB charger](https://www.aliexpress.com/item/1005003240894835.html)         | 1        |
| XT60 > Barrel cable       |[power cable]](https://s.click.aliexpress.com/e/_DDVjyhr)         | 1        |
|  Barrel> Screw terminal      |[barrel adaptor]](https://s.click.aliexpress.com/e/_DDVjyhr)         | 1        |
| USB > Motor driver cable         |[JST cable](https://www.aliexpress.com/item/1005004192966816.html)         | 2       |
| Qwiic cable             | [For connecting ESP32](https://www.aliexpress.com/item/1005005796723171.html)                      | 1        |
| Hex Spacers               | [45mm height M3 standoff](https://www.aliexpress.com/item/32539100523.html)          | 1    |
| M2 Bolts & nuts           | [400pc Bolt pack](https://www.aliexpress.com/item/1005002046118328.html)                                          | 1      |
| M3 Bolts  & nuts          | From Bolt pack                                          | 10        |
| Screw Driver              | 2 in 1 Flat and Philips Head Screw Driver | 1 |
| Optional (recommended) IMU | [MPU6500](https://www.adafruit.com/product/3886) or [BNO085](https://www.adafruit.com/product/4754)                                     | 2        |
| Optional LiDAR Kit for use with ROS2 |  [LiDAR module, USB Cable and Data Convertor Box](https://www.amazon.co.uk/DTOF-D300-Distance-Obstacle-Education/dp/B0B1V8D36H/ref=sr_1_1?crid=2BSZJ4XVN2S12&keywords=ld19+lidar&qid=1707070916&sprefix=ld19+lidar%2Caps%2C254&sr=8-1) | 1 |


