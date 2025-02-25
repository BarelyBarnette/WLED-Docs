---
title: Compiling WLED
hide:
  # - navigation
  # - toc
---


You want to add custom features to WLED, use non-default pins, or add in a usermod? You've found the right place!

WLED has come to rely on so many dependencies in the latest versions that building with the Arduino IDE is no longer recommended.
Instead, installing Visual Studio Code and its PlatformIO (PIO) extension is easier, as it will install the ESP Arduino core, all the required libraries and the correct compilation settings for you automatically.

### Installation guide (PlatformIO, recommended)
0. Make sure Git client is installed on your system. If it isn't, you can get it [here](https://git-scm.com/downloads).
1. Download and install the free [Visual Studio Code](https://code.visualstudio.com/) by Microsoft.
2. Open VS Code and go to the Extensions manager (the icon with the stacked blocks in the left bar)
3. Search for `platformio ide` and install the PlatformIO extension
4. Download the WLED source code by executing `git clone https://github.com/Aircoookie/WLED.git` in some folder. Alternatively fork the WLED project first and download it from your fork
5. Go to `File -> Open Folder` and open that root WLED folder (the one that contains `platformio.ini`, _NOT_ the `wled00` folder)

### Compilation guide (PlatformIO)
1. In VS Code, open the file `platformio.ini`.
2. Add a semicolon in front of the line that says `default_envs = travis_esp8266, travis_esp32` to comment it out.
3. Select your build environment by un-commenting one of the lines starting with `; default_envs =`.  
Please remove _BOTH_ the `;` and the whitespace behind it to correctly uncomment the line.  
For most ESP8266 boards, the `d1_mini` environment is best.  
4. In the blue bottom bar, hit the checkmark to compile WLED or the arrow pointing right to compile and upload!  

     [Picture Guide](https://i.imgur.com/mZYo4KJ.jpg)

Success! 
 
If you get one of these two errors, hit the checkmark icon once again to compile and that time the code should build without problems! 
- `error: wled00\wled00.ino.cpp: No such file or directory`
- `FileNotFoundError: [WinError 2] The system cannot find the file specified: '[...].sconsign37.dblite'`

### Compilation guide (Arduino IDE, not recommended)

- Follow a guide to setup your Arduino IDE (I am using version 1.8.9) with the ESP8266 libraries.
For current compiles I recommend the latest Arduino core version 2.7.4. If you do not wish to install all libraries manually it is recommended to download the PlatformIO extension for VS Code (see above).

- You will need to install a few libraries:

| Library Name | Platform |
| --- | --- |
[NeoPixelBus](https://github.com/Makuna/NeoPixelBus) (2.6.0) | All
[FastLED](https://github.com/FastLED/FastLED) | All
[ESPAsyncWebServer Aircoookie fork](https://github.com/Aircoookie/ESPAsyncWebServer) (2.0.0) | All
[IRRemoteESP8266](https://github.com/crankyoldgit/IRremoteESP8266) | All
[ESPAsyncTCP](https://github.com/me-no-dev/ESPAsyncTCP) | ESP8266 only
[ESPAsyncUDP](https://github.com/me-no-dev/ESPAsyncUDP) | ESP8266 only
[AsyncTCP for ESP32](https://github.com/me-no-dev/AsyncTCP) | ESP32 only
[LITTLEFS_esp32](https://github.com/lorol/LITTLEFS)* | ESP32 only

\* Please see [the installation guide](https://github.com/lorol/LITTLEFS#installation). You might need to enable a define in the library code.

All other dependencies are included with WLED for convenience.

- Now compile and flash the software! Make sure you erase everything when you flash! (If your board config does not provide this option, you can `Sketch -> Export compiled Binary` and upload with [any ESP flashing tool](/basics/install-binary).)

### Compilation settings (Arduino IDE)
ESP8266:
- Arduino Core v2.7.4
- Board: NodeMCU 1.0 (ESP-12E module) (or select your ESP board)
- CPU frequency: 80 MHz
- Flash size : 4MB (1MB SPIFFS)
- LwIP variant: v1.4 Higher Bandwidth (try 2 if you experience issues)
- Upload speed: Any, 921600 recommended

ESP8266-07 (External Antenna):
- Variants have 512kB or 1MB flash
- Be sure to use DOUT mode when flashing
- Flash Size 1MB (128k SPIFFS)
- 512kB variant no longer compatible

ESP-07s (External Antenna):
- Variant have 4MB flash
- Settings as for NodeMCU or Wemos

ESP32:
- Arduino Core v1.0.4