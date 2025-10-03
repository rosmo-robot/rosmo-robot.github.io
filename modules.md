For reproducable robots larger than Rosmo a modular system makes sense https://arxiv.org/pdf/2402.09833

A professionalised https://github.com/luisllamasbinaburo/OpenRobot_V2/wiki/Module_I2C_GPIO 

Using a fast Olimex P4 for uROS or other low layer control (Lizard) Via UART from SBC or Ethernet.

We need 
- encoder in x 4
- IMU (bunch of Qwiic)
- Lidar header
- Mikrobus small header
- CANBUS to SimpleFOC motors 
- UEXT for relays https://www.olimex.com/Products/Modules/IO/MOD-IO/open-source-hardware
- Headers for pololu https://www.pololu.com/product/1213/specs / clone https://oshwlab.com/mephistopheles.loki/mc33926-dual-driver-ardumower

From this most things, can be I2C via Qwiic, using the 20x20 mount holes, eg servos, motor controller.
 
For more pro stuff this needs to swap to CANBUS, BLDC.

Power distro is also a thing. https://mjbots.com/products/mjpower-ss  + https://oshwlab.com/manoranjan2050/multi-voltage-regulator-pcb-12v-

Arm controller: https://oshwlab.com/quirin.forster21/open-flight-computer-proton





