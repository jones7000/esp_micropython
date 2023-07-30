# Getting started with MicroPython on ESP32 / ESP8266

* see detailed documentation on official micropython docs:
	* [esp8266](https://docs.micropython.org/en/latest/esp8266/tutorial/intro.html)
	* [esp32](https://docs.micropython.org/en/latest/esp32/tutorial/intro.html#esp32-intro)

## 1 Getting firmware
Download firmware from [micropython.org](https://micropython.org/download/)

## 2 Deploy firmware

### 2.1 Install esptool: 
* Command: `pip install esptool`
* Source: [git esptool](https://github.com/espressif/esptool/)
	
### 2.2 Flash Firmware:
* Erase flash:
`esptool.py --port /dev/ttyUSB0 erase_flash`

* Deploy new firmware:
`esptool.py --port /dev/ttyUSB0 --baud 460800 write_flash --flash_size=detect 0 esp8266-1m-20230426-v1.20.0.bin`
