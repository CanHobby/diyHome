# diyHome
DIY Home Automation using ESPnow inspired by Home Assistant

This is my attempt at making a Home Assistant type home automation system geared to the Arduinno DIY user.  It is less bulky and easier to configure than HA.  It is (or will be) a fairly complex project involving mostly Arduino ".ino" files, but does include HTML and ".css" etc.

My goal is to make it as modular as possible, AND to include lots of comments - BOTH in the code and where applicable in the README files in each major subdirectory.

I make the assumption that you know how to use the Arduino IDE to compile and upload code.  OTA upload is supported.

### Nomeclature:

The diyHome system consists of various submodules - notably
 -- Server - the Server is basically a WebPage to espNOW/MQTT gateway.
 -- Station - Stations are the controllers for individual entities such as lamps, relays, LEDs etc.  espNOW stations are part of this github repository.  For MQTT we highly recommend [Tasmota](https://tasmota.github.io/docs/).

 I welcome suggestions and/or collaborations.
