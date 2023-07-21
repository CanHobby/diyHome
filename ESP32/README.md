# diyHome - ESP32
DIY Home Automation using ESPnow inspired by Home Assistant

So far the ESP32 versions of diyHome supports all flavours of the ESP32 family.  Most of my testing has been with an ESP32-S3.  The ES{32 Arduini Boards Package supports all versions of the MCU - The latest stable release can be installed using the IDE Boards Manager by adding the line:

      https://espressif.github.io/arduino-esp32/package_esp32_index.json

into the File -> Preferences box of the IDE.

## Libraries - you will need to install the following lbraries using the IDE Library Manager:
Arduino_JSON  by Arduino

## External Libraries - you will need to download the following lbraries from github: (git clone works reak nice) 
the ESPAsyncWebServer will need to be downloaded from https://github.com/me-no-dev/ESPAsyncWebServer/tree/master<br>
            --  clone or unzip the code into your $HOME/Arduino/libraries folder<br>
the ESPAsyncWebServer depends on [https://github.com/me-no-dev/ESPAsyncWebServer/tree/master](https://github.com/me-no-dev/AsyncTCP)<br>
            --  clone or unzip the code into your $HOME/Arduino/libraries folder
            

diyHone makes extensive use of freeRTOS which makes it very modular.  The "diyHome.h" has defines near the top of the file which allow you to use or not use different modules.   for example:

<code>
#define use_NTP    //    include the NTP internet time routines
#define use_Weath  //    include the openweathermap internet weather routines.
#define use_FCast  //    include the openweathermap internet weather forecast routines.
</code>
