# diyHome - ESP32
DIY Home Automation using ESPnow inspired by Home Assistant

So far the ESP32 versions of diyHome supports all flavours of the ESP32 family.  Most of my testing has been with an ESP32-S3.  The ES{32 Arduini Boards Package supports all versions of the MCU - The latest stable release can be installed using the IDE Boards Manager by adding the line:

      https://espressif.github.io/arduino-esp32/package_esp32_index.json

into the File -> Preferences box of the IDE.

### <u>Libraries</u> - you will need to install the following libraries using the IDE Library Manager:
<ul><li>Arduino_JSON  by Arduino</li></ul>

<h3>External Libraries - you will need to download the following libraries from github:</h3>
use git clone ....  or download the ".zip" into your $HOME/Arduino/libraries folder.<br><br>
<ul><li>ESPAsyncWebServer will need to be downloaded from: <a href="https://github.com/me-no-dev/ESPAsyncWebServer" target="_blank">ESPAsyncWebServer</a></li></ul>
<ul><li>ESPAsyncWebServer depends on: <a href="https://github.com/me-no-dev/AsyncTCP" target="_blank"> AsyncTCP</a></li></ul><br>
<h3>The ESP32FS Spiffs File System Upload Tool needs to be installed in the IDE</h3>
<ul><li>Make a new subdiectory named 'tools' in your "Arduino" folder.</li>
<li>Go to the <a href=https://github.com/me-no-dev/arduino-esp32fs-plugin/releases/>Release Page</a>, click on ESP32FS-1.1.zip and download it.
<li>UnZip it into the 'tools' directory.</li>
<li>Close the IDE and Open it again - You should see an Option for "ESP32 Sketch Data Upload".<br>
just above the Board Selector in the tools menu dropdown.</li>
</ul>
<b>diyHone</b> makes extensive use of freeRTOS which makes it very modular.  The "diyHome.h" has defines near the top of the file which allow you to use or not use different modules.   for example:

<code>
#define use_NTP    //    include the NTP internet time routines
#define use_Weath  //    include the openweathermap internet weather routines.
#define use_FCast  //    include the openweathermap internet weather forecast routines.
</code>
