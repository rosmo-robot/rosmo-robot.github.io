For reproducable robots larger than Rosmo a modular system makes sense

A professionalised https://github.com/luisllamasbinaburo/OpenRobot_V2/wiki/Module_I2C_GPIO 

Using a fast STM https://oshwlab.com/ottello/stm32h750 for uROS or other low layer control (Lizard)

We need 
- encoder in x 4
- IMU
- Lidar
- Mikrobus small header
- CANBUS

From this most things, can be I2C via Qwiic, using the 20x20 mount holes, eg servos, motor controller.
 
For more pro stuff this needs to swap to CANBUS, BLDC.

Power distro is also a thing.

Arm controller: https://oshwlab.com/quirin.forster21/open-flight-computer-proton





