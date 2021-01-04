# ESP32-BTC
Simple Demo for an ESP32 module with a TFT LCD or an OLED display.

Forked from https://github.com/joysfera/esp32-btc

![clock](esp32btcclock.gif)
1. Modify current time to real current time.
2. Set time zone on JST(+9h).

![checkbtc](esp32btcgetbtc.gif)
3. When renew the BTC, blink the blue LED on esp32s GPIO 02.

Displays current real time and BTC price in USD.


## install (The result I tried)
1. Prepare the parts.

   ESP32-S(Node-MCU/Hiletgo) 
   
   0.96" I2C serial 128×64 OLED LCD
   
   Wire & Pret board
   
2. Wiring following below

![wire](ESP32stoOLED.png)

3. Insert Wi-fi SSID & Password in .ino file

4. Compile arduino IDE & write down ESP-32.

   You may need to press and hold the Boot button when writing to the ESP32.

5. Just run!


The original text below
-------------------------------------------------------------------------------------------------------------------------------------

Supports two different modules directly:

- ESP32 with I2C connected SSD1306 driven OLED display (resolution 128x64) made by Lolin as [WEMOS LOLIN32]( https://github.com/FablabTorino/AUG-Torino/wiki/Wemos-Lolin-board-(ESP32-with-128x64-SSD1306-I2C-OLED-display))
- ESP32 with SPI connected ST7789V driven TFT LCD display (resolution 240x135) made by TTGO as [T-Display](https://github.com/Xinyuan-LilyGO/TTGO-T-Display)

It's very easy to modify the source code for any I2C or SPI connected display.

The demo application shows several useful techniques, such as:
- using a single source code with very different displays and graphics libraries
- obtaining current time using SNTP
- obtaining current bitcoin price using a web API
- avoiding JSON library when decoding simple JSON message
- using the Tasker library to call a task periodically or on a button press

To install ESP32 core on Arduino follow the instructions on this page:
https://github.com/espressif/arduino-esp32#installation-instructions

Then you'll need to install either SSD1306 or TFT_eSPI libraries and also NTPClient and Tasker libraries. They are available via the Arduino Library Manager.

Please note that the TTGO T-Display requires version **1.4.16** (or higher) of the TFT_eSPI library, otherwise the screen content is shifted by 52 pixels.

Enjoy!

Petr Stehlik
https://github.com/joysfera

#### LOLIN32 photo
![LOLIN photo](lolin.jpg)

#### LOLIN32 pinout
![LOLIN pinout](lolin2.jpg)

#### TTGO T-Display
![TTGO T-display photo+pinout](T-display.jpg)
