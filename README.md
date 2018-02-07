# esp8266_firmware_update
How to update ESP8266 wifi module firmware

What you will need:
- Arduino board
- External 3.3v power supply
- ESP8266 module
- Some wires

1) Circuit: 

	* 3.3v+   <--> ESP VCC
	* 3.3v+   <--> ESP CH_PP
	* 3.3v-   <--> ESP GND
	* 3.3v-   <--> ESP GPIO0 (Means FLASH MODE ON)
	* 3.3v-   <--> Arduino GND
	* ESP TX  <--> Arduino TX
	* ESP RX  <--> Arduino RX

2) Build an empty sketch and download to the Arduino.
3) Run esp8266_flasher.exe
4) Load the file V0.9.2.2_AT_Firmware.bin
5) Click "Download" and wait until its done. Its posible that the program alerts you that was unable to disable the flash mode, thats why we configured it manually by wiring the GPIO0.
6) Unplug the wire to GPIO0 to disable flash mode and restart the ESP.
7) Open the Serial Monitor (CTRL + M) and search for the baudrate which you receive any readable response. The default baudrate depends on the actual ESP8266 model and installed firmware.
