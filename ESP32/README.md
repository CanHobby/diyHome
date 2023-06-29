# diyHome - ESP32
DIY Home Automation using ESPnow inspired by Home Assistant

So far the ESP32 versions of diyHome support all flavours of the ESP32 family.  Most of my testing has been with an ESP32-S3.
It makes extensive use of freeRTOS which makes it very modular.  The "diyHome.h" has defines near the top of the file which allow you to use or not use different modules.   fo example:

<code>
#define use_NTP    //    include the NTP internet time routines
#define use_Weath  //    include the openweathermap internet weather routines.
#define use_FCast  //    include the openweathermap internet weather forecast routines.
</code>
