# RAK811_LoRaWAN_Arduino
1. What is Arduino?
If you know little about Arduino, please have a look below:  
[https://www.arduino.cc/](https://www.arduino.cc/)

2. You have known Arduino.  Install the IDE first:  
[https://www.arduino.cc/en/Main/Software](https://www.arduino.cc/en/Main/Software)

3. What lib is used?  
RAK811 is based on STM32L151.Therefore Arduino Core for Arduino_Core_STM32 is suitable for RAK811.

4. How to install Arduino_Core_STM32 in Arduino?  
[https://github.com/stm32duino/Arduino_Core_STM32](https://github.com/stm32duino/Arduino_Core_STM32)  
add "https://github.com/stm32duino/BoardManagerFiles/raw/master/STM32/package_stm_index.json" to **Additional Boards Manager URLs:** option  
![install Arduino_Core_STM32](https://i.imgur.com/YT9RnJZ.png)  
Check the other lib below install or not?
![Check Cores](https://i.imgur.com/faDIbvj.png)
Then install the BSP for STM32.
If install completed as following:

5. Download the LoRaWAN library from:  
[https://github.com/mcci-catena/arduino-lmic#selecting-the-lorawan-region-configuration](https://github.com/mcci-catena/arduino-lmic#selecting-the-lorawan-region-configuration)  
Add it to Arduino IDE:  
![LoRaWAN library](https://i.imgur.com/y0EIxmZ.png)
6. OK, development environment is finished. Open the Arduino_RAK811_LoRaWAN.ino，config 3 parameters for LoRaWAN_OTAA:  
![config 3 parameters](https://i.imgur.com/gJkX8hy.png)  
And set Pins mapping:  
![Pin mapping](https://i.imgur.com/pcTiILc.png)

7. Compile it,ingnore the Waring:  
![compile success](https://i.imgur.com/2eEF9MG.png)  
Download the *.bin, *.hex or *.elf file from the folder in the above path with JFlash,STM32CubeProgrammer,or any tool if it supports STM32 mcu.

8. When download ok, the Gateway and server are working properly.  
The RAK811 will be auto join LoRaWAN:
![Joinning LoRaWAN](https://i.imgur.com/jT9HJbX.png)  
TTN receive data:  
![TTN data](https://i.imgur.com/2uZxblA.png)

