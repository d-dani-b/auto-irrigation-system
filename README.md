 Arduino-based technology to monitor soil moisture levels in real-time then can transmit the readings to my PC (up to 2,000,000 times per second). When the soil is dehydrated, the system automatically activates a water pump to irrigate the plant, then stops when optimal moisture is reached. Input code in Arduino IDE. Components required: Arduino UNO r3, HW 080, 2x aa battery holder with LI-ION 18650 batteries (ofc), L289N Motor controller, 3-5v water pump. Wiring is easy enough, but here you go!:

 | Battery       | L298N                 |
| ------------- | --------------------- |
| **Red (+)**   | **12V / +V / Vmotor** |
| **Black (–)** | **GND**               |


| Arduino | L298N   |
| ------- | ------- |
| **GND** | **GND** |


| Pump wire | L298N    |
| --------- | -------- |
| Wire 1    | **OUT1** |
| Wire 2    | **OUT2** |


| Arduino   | L298N   |
| --------- | ------- |
| **Pin 6** | **IN1** |
| **Pin 7** | **IN2** |
| **Pin 5** | **ENA** |

| HW-080  | Arduino  |
| ------- | -------- |
| **VCC** | **5V**   |
| **GND** | **GND**  |
| **AO**  | **A0**   |
| **DO**  | not used |



⚠️ Critical rules

Sensor NEVER touches the 18650

Pump NEVER touches Arduino 5V

All grounds must connect

Battery → L298N
Arduino → L298N
Sensor → Arduino
