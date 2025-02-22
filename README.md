# IMPORTANT 
> *This documentation provides an overview of the School Schedule Project created for School. The project uses the ESP8266 microcontroller to display a schedule on an LCD 16x2 screen and plays associated sounds or messages using the DFPlayer Mini MP3 module, and RTC module for tracking the times. Additionally, I add web interface to control the schedule remotely using local Address. The system allows users to view the schedule and modify it using a website.*

Hello this is my first project that requested directly by School and still used till now in my School, The system may not be perfect, and there’s a lot room for improvements, but it’s working as intended for now.

If u wan't to try please use **PlatformIO** instead of **Arduino IDE**

## Component Used
- ESP8266
- DFMusicPlayer
- LCD 16x2 + I2C
- RTC DS321

## Circuit Diagram
**ESP8266**

    - GPIO4 (D2) → SDA (I2C for LCD) & RTC DS321 (I2C)
    - GPIO5 (D1) → SCL (I2C for LCD) & RTC DS321 (I2C)
    - GPIO13 (D7) → RX (DFPlayer Mini)
    - GPIO15 (D8) → TX (DFPlayer Mini)
    - VIN → Power Jack (OPTIONAL DEPENDING ON YOUR ESP8266 YOU CAN USE USB MICRO / TYPE-C INSTEAD)

**LCD 16x2**

    - VCC → VIN of ESP8266 / Power Jack
    - GND → GND of ESP8266
    - SDA → GPIO4 (D2)
    - SCL → GPIO5 (D1)

**DFPlayer Mini**

    - VCC → VIN of ESP8266 / Power Jack
    - GND → GND of ESP8266
    - RX → GPIO13 (D7)
    - TX → GPIO15 (D8)
    - DACL + DACR → Speaker

**RTC DS3231**

    - VCC → VIN of ESP8266 / Power Jack
    - GND → GND of ESP8266
    - SDA → GPIO4 (D2)
    - SCL → GPIO5 (D1)

The Schematic Should be like this
![Schematic](https://i.imgur.com/I0TyYPp.png)

## Website

To Access the Website u need to be connected to ESP8266 WiFi first, then you need to input ESP8266 Local IP Address by default it's 192.168.1.1 on your browser, then it should show the Web Interface

