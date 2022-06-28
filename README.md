# 191148-RemakeWeatherStation

This is the software for use with the Elektor weatherstation remake of 2020
The core of the station is a ESP32 Pico Kit V4.x arround the WH-SP-WS02 ( https://www.elektor.de/professional-outdoor-weather-station-wh-sp-ws02 )
The software and also some parts of the webpage got an overhaul or are completely rewritten. 

The new modular design should allow for the later addition of new sensors or features with less hassle than before.

## Getting Started

Use your current Arduino IDE to compile the Code and also the ESP32 Arduino Core installed.
Have a look at : https://www.elektormagazine.com/labs/esp32-getting-started for a getting started guide.
You will need to have the following libraries available:

* LiquidCrystal_I2C ( https://github.com/johnrickman/LiquidCrystal_I2C )
* eHaJo Absolut Pressure AddOn by Hannes Jochriem ( https://github.com/ehajo/WSEN-PADS )
* Adafruit Unified Sensors
* Adafruit BME280 Library
* Adafruit VEML6070 Library
* Adafruit VEML6075 Library/
* Adafruit TSL2561 Library
* Adafruit TSL2591 Library
* Adafruit BusIO
* Time by Michael Margolis
* ArduinoJson 6.x 
* PubSubclient by Nick o'Leary
* NTP Client Lib by German Martin

### Prerequisites

If you try to programm the ESP32 Pico Kit be aware that the use of more modern USB3.x ports may cause the board
NOT to enter programming mode. Use a USB2.0 Port or at least a USB2.0 Hub to get around this. 

## Pin mapping

Currently the following Pin mapping is used for the software:

* IO02 : RES  ( RFM95 )
* IO14 : SCKL ( RFM95 )
* IO12 : MISO ( RFM95 )
* IO13 : MOSI ( RFM95 )
* IO15 : NSS  ( RFM95 )
* IO32 : DIO2 ( RFM95 )
* IO33 : DIO1 ( RFM95 )
* IO34 : DIO0 ( RFM95 )
* IO25 : SCL
* IO26 : SDA
* IO34 : WIND SPEED
* IO38 : RAIN
* IO37 : WIND DIR
* IO19 : MISO ( SD-CARD )
* IO23 ; MOSI ( SD-CARD )
* IO18 : SCKL ( SD-CARD )
* IO05 : CS0  ( SD-CARD )
* IO09 : TX1 ( Particle Sensor )
* IO10 : RX1 ( Particle Sensor )

