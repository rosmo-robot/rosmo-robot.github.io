---
layout: home
title: Rosmo
subtitle: Tortoisebot
---
## Attribution
This document is based on the work of [rigbetellabs](https://github.com/rigbetellabs/tortoisebot_docs) it is adapted to use ROS2 on ESP32 and to have [Open Robotic Platform](https://openroboticplatform.com/library) mount holes.

## 1.1 Checklist
Let's get started by laying out everything. 

Note there are some changes to this version so the photos may not match exactly.

![](https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4382.JPG)

Make sure you have everything with you according to this table:

| Components                | Description                               | Quantity |
| ------------------------- | ----------------------------------------- | -------- |
| TortoiseBot ORP Chassis Plates | [Custom PCB Chassis](https://github.com/rosmo-robot/open-robotics-platform/tree/main/2wd-TT-motor)      | 5       |
| BO Motor with encoder                  | [60 RPM motor & bracket](https://www.aliexpress.com/item/1005005737025799.html)                | 2        |
| Motor Driver              | [Zio H-bridge Motor Driver](https://www.smart-prototyping.com/Zio-4-DC-Motor-Controller.html?search=motor)          | 1        |
| Olimex ESP32-S3              | [For running MicroROS](https://www.olimex.com/Products/IoT/ESP32-S3/ESP32-S3-DevKit-Lipo/open-source-hardware)                | 1        |
| BO Motor Wheel            | [65 mm diameter, 25 mm thickness](https://www.aliexpress.com/item/1005005910261919.html)           | 2        |
| Caster Wheel              | [bearing](https://www.aliexpress.com/item/1005005883966772.html)
| USB powerbank           |[ battery case](https://www.aliexpress.com/item/1005005637445437.html)         | 1        |
| 3x 18650           |[Batteries](https://s.click.aliexpress.com/e/_DdfBurF)         | 1        |
| USB > Motor driver cable         |[JST cable](https://www.aliexpress.com/item/1005004192966816.html)         | 1        |
| PCB or Breadboard              | [Breadboad (if you don't have a PCB to break out ESP32)](https://www.aliexpress.com/item/1005001704653648.html)                      | 1      |
| 2.54mm screw terminals for breadboard/ PCB         | [For connecting encoder](https://www.aliexpress.com/item/1005001677869988.html)                      | 4       |
| Qwiic cable             | [For connecting ESP32](https://www.aliexpress.com/item/1005005796723171.html)                      | 1        |
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


## 2.2 Assembly

Note this is a work in progress, some of the photos and instructions need updating for the new BOM & ESP32 based control

### 2.2.1 Assemble Motors & Base

Take the following components:
* M3 10 mm Bolts x 2
* M3 25 mm Bolts x 2
* M3 Nuts x 2
* BO Motor Bracket x 1
* BO Motor x 1 
> Please note to take the BO Motor, whose shaft points in the left direction when the 2-way-tape is facing downward and the wires are pointing you. Refer to the picture below. This is your Left Motor.

![](https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4385.JPG) 

Now attach the Motor Bracket on the flat side of the motor in a way that the screw holes are facing outwards and at the bottom side and also the holes of the motor align with the farther most holes of the motor brackets. After that put the 10 mm M3 bolts in the bottom holes. Do not tighten these bolts with nuts yet.

<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4386.JPG" width="400"/>. <img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4387.JPG" width="400"/>

Now thread both the 25 mm M3 bolts from the outer end (from the side where there is a shaft) of the motor and attach them with nuts on the other end. Repeat the procedure for the other motor as well. So now you have two motors with the shaft facing outwards and screw holes facing inwards and the 2-way-sticking tape facing downwards.

<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4390.JPG" width="250"/>  <img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4391.JPG" width="250"/>  <img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4392.JPG" width="250"/>
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4394.JPG" width="250"/>  <img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4395.JPG" width="250"/>  <img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4396.JPG" width="250"/>

Now take one of the Chassis plates and place it in the following orientation. The Top is the Front of the Robot and your right and left are the right and left of the robot respectively. 

<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4397.JPG" width="450"/>

Now use the red highlighted holes and put the 10mm M3 bolts through them and tighten them with nuts from below. You can also remove the double-sided tape cover and use it to secure your motors in place for additional strength. If you are facing any problem in building your robot, you could [Join our Discord Community](https://discord.gg/5tBAUJjC) and ask your doubts or questions over there. Our community will be there to help and guide you through the complete process.

<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4398.JPG" width="250"/> 
<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4399.JPG" width="250"/>

Take the caster wheel, remove the plastic covering, and using a pair of nut and bolt, fix it in the highlighted hole from the bottom side. You can use more than one nut and bolt to secure it in place, but one is more than enough

<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/chassis/images/holes002.png" width="250"/>  
<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4400.JPG" width="200"/> 
<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4401.JPG" width="200"/>
<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4402.JPG" width="200"/>

Now you can attach wheels to the motors after which take 6 Hex spacers along with 18 nuts and fix them in these highlighted holes. Also, you can attach the battery in the centre using double-sided tape.

<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4403.JPG" width="350"/>
<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/chassis/images/holes003.png" width="450"/>  
<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4404.JPG" width="400"/>
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4405.JPG" width="400"/>

With this you have the base of your TortoiseBot ready!

### 2.2.2 Electronics Layer

Now let's make the Heart of our Robot. The place where the blood (electrons) are pumped all over our TortoiseBot's body.
the USB powerbank will give power to the motor driver and ESP32.

Here we have the Motor Driver and the powerbank. Take another Chassis plate and keep the orientation the same as the previous one. Also have the Zio Motor Driver,  If your using one also the Data Convertor from LiDAR. You can disconnect the wire from LiDAR as we will attach it later. 

<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/chassis/images/plate.png" width="350"/> 
<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4406.JPG" width="450"/>

Once you have it all, you can attach Motor Driver and LiDAR Data Converter Module each with 4 pairs of nuts and bolts through the blue and green highlighted holes respectively. Make sure the heatsink of the motor driver is facing the front link in the picture while attaching. Similarly, while attaching the LiDAR data convertor, the wires should be on the top side and the USB ports should be facing you on the backside of the robot. Also, you can fix the USB Power Module Simply with Double-sided tape on the given position.

<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/chassis/images/holes004.png" width="250"/> 
<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4407.JPG" width="200"/> 
<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4408.JPG" width="200"/>
<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4409.JPG" width="200"/>

``

Make sure your connections are proper. If you are facing any problem in building your robot, you could [Join our Discord Community](https://discord.gg/5tBAUJjC) and ask your doubts or questions over there. Our community will be there to help and guide you through the complete process.

<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/schematics/ttbotprint.png" width="250"/>  <img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4411.JPG" width="300"/> <img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4412.JPG" width="300"/>

Now take the base of the robot and the plate you made just now and place them second above the first one. While placing it, make sure you pass the motor wires from the highlighted holes. Left hole for left motor wires and right hole for right motor wire. Don't bolt the plate down yet. 

<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4413.JPG" width="300"/> 
<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/chassis/images/holes005.png" width="200"/>  <img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4414.JPG" width="300"/> 

<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4415.JPG" width="250"/> 
<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/chassis/images/holes006.png" width="300"/>  
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4416.JPG" width="250"/> 

Now, look at the wires of your Left Side. Make a note of which coloured wire is at the top and which one is at the bottom. You should also be able to see this written on the info that came with the motor. In this case, for the left motor, our bottom wire is RED and the top wire is GREEN. So keeping that in mind, we will connect our top wire (GREEN) in the front of the motor driver (towards the heatsink) and the bottom wire (RED) towards the backside (near other connection points). Refer to the images below and the connection sheet provided with your kit. Please make sure these connections are made properly or else your Robot will not move in the expected directions. Similarly, if we have a look at our motor on the right side, the top wire is RED in this case and the bottom wire is GREEN. So again we will connect the top wire (RED) towards the side of the heatsink and the bottom wire (GREEN) towards the connection side. Note to cross-check the connections. This is the most important step of building the robot.

<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/schematics/ttbotprint.png" width="250"/>  <img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4418.JPG" width="300"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4419.JPG" width="300"/>  
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4420.JPG" width="310"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4421.JPG" width="550"/> 

After that use, the RED highlighted holes to bolt down the spacers and use the BLUE highlighted holes to add more spacers on top of the existing spacers through the TortoiseBot Chassis Plate like in the picture. Also, use the GREEN highlighted holes to add more spacers which you can tighten with nuts from the bottom.

<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/chassis/images/holes007.png" width="350"/>  <img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4423.JPG" width="500"/>

Finally, for stage number 2, connect Qwiic cable to the motor driver's pins,  
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4424.JPG" width="400"/>  
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4425.JPG" width="400"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4426.JPG" width="800"/>

### 2.2.3 The Brain Layer - Where ESP32 lives

This is the easiest layer to assemble. 



Attach the ESP32 to the breadboad. Now place this breadboard on top of your assembled robot and pass the LiDAR Data Wire from the GREEN highlighted hole and all other Jumper Wires ( 7 in total ) from the BLUE highlighted hole. And finally, bolt it all down using the RED highlighted holes.


Use the USB A to USB C cable to connect the powerbank to the ESP32. You can pass the wire through the inside of the spacers in order to keep everything clean and no wires hanging around. 


Lidar detail to go here

<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4438.JPG" width="550"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4439.JPG" width="310"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4441.JPG" width="310"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4442.JPG" width="550"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4443.JPG" width="430"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4444.JPG" width="430"/> 

Now take 6 Pairs of Nuts and Spacers and attach them through the RED highlighted holes.

<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/chassis/images/holes010.png" width="350"/>  
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4445.JPG" width="450"/>

### 2.2.4 The Final Layer

Grab the final plate. This is where we will be attaching all our sensors i.e. LiDAR and Camera. So to attach that, also grab the 3D Printed Camera Mounts. Both of these parts are different. So don't get confused between them. The one with the flat base will be referred as Camera Mount Top and the one with a step-like structure will be referred as Camera Mount Bottom. The Camera Mount Top is attached to the Plate and the Bottom will be connected to the Camera.

<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4447.JPG" width="310"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4448.JPG" width="550"/>

Now use the RED highlighted holes to assemble the Camera Mount Top to the Chassis Plate at its underside using 2 pairs of nuts and bolts. Refer to the picture for more clarity.

<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/chassis/images/holes011.png" width="450"/>
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4449.JPG" width="350"/>

Now take the Bottom Camera mount and Raspberry Pi Camera and fix them together using M2 Nut and Bolts. The Small ones. I am using a self-tapping screw here, but along with your kit, you might have got nuts and bolts. So use that to secure the camera in place. The step-like design is to accommodate the ribbon cable connector of the camera. So make sure it is flushed while attaching.

<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4451.JPG" width="425"/>
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4452.JPG" width="425"/>

Now attach both the Camera Pieces together with a pair of M3 nut-bolt. You can also use pair of washers on both ends to make the joint firm and adjustable at the same time.

<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4454.JPG" width="425"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4455.JPG" width="425"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4453.JPG" width="185"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4456.JPG" width="330"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4457.JPG" width="330"/> 

Take the rest of the assembled Robot, and attach the Raspberry Pi Camera to Raspberry Pi using the ribbon cable. Make sure the connections on the cable are facing away from the USB ports. Once that is done, you can place the plate on the robot and take the LiDAR wire out of the big circular hole as shown in the picture. And then bolt the spacers down with M3 10mm bolts through the RED highligted holes.

<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4458.JPG" width="550"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4460.JPG" width="310"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4464.JPG" width="275"/> 
<img src="https://raw.githubusercontent.com/rigbetellabs/tortoisebot_docs/master/chassis/images/holes010.png" width="325"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4465.JPG" width="275"/> 

Now take the LiDAR and attach the LiDAR cable to its bottom as shown in the image. Then pass the wire through the small notch around the circle and then pass the LiDAR motor through the big hole and making sure the wire is passed through the notch properly. Take 2 more pairs of nut bolts and use them to secure the LiDAR in place.

<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4466.JPG" width="275"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4467.JPG" width="275"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4468.JPG" width="275"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4469.JPG" width="225"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4470.JPG" width="225"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4471.JPG" width="400"/> 

<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4472.JPG" width="400"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4473.JPG" width="400"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4474.JPG" width="400"/> 
<img src="https://raw.githubusercontent.com//rigbetellabs/tortoisebot_docs/master/imgs/assembly/IMG_4475.JPG" width="400"/> 

# 3. Linorobot Setup

Once you are done with assembling the robot, you could start [Setting up linorobot](https://robofoundry.medium.com/building-cheapest-ros2-robot-using-esp32-part-1-hardware-build-af0044de68ce)
 so that it could connect to your Local Wi-Fi and you could start coding it using ROS
