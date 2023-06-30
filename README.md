# diyHome
DIY Home Automation using ESPnow inspired by Home Assistant

This is my attempt at making a Home Assistant type home automation system geared to the Arduinno DIY user.  It is less bulky and easier to configure than HA.  It is (or will be) a fairly complex project involving mostly Arduino ".ino" files, but does include HTML and ".css" etc.

My goal is to make it as modular as possible, AND to include lots of comments - BOTH in the code and where applicable in the README files in each major subdirectory.

I make the assumption that you know how to use the Arduino IDE to compile and upload code.  OTA upload is supported.

**Nomeclature:**

The diyHome system consists of various submodules, notably:

Server: the Server is basically a WebPage to espNOW/MQTT gateway.

Station: Stations are the controllers for individual entities such as lamps, relays, LEDs etc.  espNOW stations are
    part of this github repository.  For MQTT Stations I highly recommend <a href="https://tasmota.github.io/docs/ target=_blank">Tasmota</a>.

 I welcome suggestions and/or collaborations.

 # Getting Started

 ## Phase 0

 You will need to install the <a href="https://www.arduino.cc/en/software" target=_blank>Arduino IDE</a> - I strongly recommend NOT using the new 2.X version.  It does not play nice with the ESP32-S3.  Personally I use rev. 1.8.10 (mosty because it is the only versio I can control the theme).  There are a million tutorials on installing the IDE on the web - just do a DuckDuckGo on the subject.

 For hardware you will need a MCU at a minimum.  I have code (perhaps not yet uploaded) for both <a href="https://canhobby.ca/esp8266cat" target=_blank>ESP8266</a> and <a href="https://canhobby.ca/esp32cat">ESP32</a>.  If you are planning to implement any of the advanced features I suggest using an <a href="https://canhobby.ca/esp32s3/esp32-s3pro" target=_blank>ESP32-S3 pro</a> for experienced Arduinites or an <a href="https://canhobby.ca/esp32s3/esp32-s3-32m" target=_blank>original Espressif</a>.  The ESP32-S3 is availaible with up to 32Meg Flash and 8 Meg pSRAM - the more the merrier.  Minimum flash size for the server is about 1.1M, plus you will need some room for SPIFFS.  If you have a regular ESP32 laying around you can get started with that.  More advanced features like the stock Market Ticker or Internet Radio will require more memory.  The ESP8266 server is somewhat limited but also a good place to start.

 Once you have your server MCU in place go to the <a href="https://github.com/CanHobby/nowSrvr32" target-_blank>Server Code Repo</a> and clone or UnZip the Repo into you Arduino Sketches directory.  Further details are in the Repo README.

 have fun...

 
