# DTSU666_CHINT_to_HUAWEI_translator
This project uses ESP32 to translate MODBUS messages of CHINT's DTSU666 Energy Meter into HUAWEI DTSU666H format.
This project translates the DTSU666 CHINT Power Meter registers 1 to Huawei DTSU666H Power Meter addresses

Project base on the eMODBUS library  https://emodbus.github.io/ in this library i made two small changes :
in the ModbusServerRTU.cpp added "delay(60)"  	row 192
in the RTUutils.cpp	added "delay(70)"    // row 223;  

Information on how to prepare environment , compile and flash ESP32 modules can be found at
https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/index.html#

Project uses the Arduino.h library. How to install this library in espressif environment,  you can read at
https://docs.espressif.com/projects/arduino-esp32/en/latest/esp-idf_component.html

Description how to assembling the hardware you will found in the /doc project directory . 

After installation Espressif ESP-IDF environment for ESP32 , you can execute commands to compiling and flash this project.
Go to the directory where you copied project files and execute this commands  

idf.py set-target esp32

idf.py menuconfig     // not necessary if you want to use configuration prepared by me

idf.py -p com8 flash monitor     // change number COM port depending your configuration

After this commands build directory will be created  and the ESP32 module flashed .


Good Luck:-)
