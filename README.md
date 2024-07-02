# ESP32 Marauder from Source.
A simple guide to install the firmware from source without the hassle of editing multiple files.

---
# Learn More:
### If you want a Webflash Installer go to: [Fr4nkFletcher](https://github.com/Fr4nkFletcher/ESP32-Marauder-Cheap-Yellow-Display)
### For more information about the whole ESP32 Marauder thingy, go to: [justcallmekoko](https://github.com/justcallmekoko/ESP32Marauder)
### For an in-depth process of installation, check out: [smoochiee](https://github.com/smoochiee/MARAUDER-FOR-CYD---CHEAP-YELLOW-DISPLAY/tree/main) 
---
## Preparing Arduino IDE `2.2.1`
1. Install Arduino IDE version 2.2.1 from: [SOURCEFORGE](https://sourceforge.net/projects/arduino-ide.mirror/files/2.2.1/)
2. Open the Arduino IDE and go to File>Preferences
3. Add the following URLs to Additional Boards Manager UR
- https://dl.espressif.com/dl/package_esp32_index.json
- https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_dev_index.json
4. Now, go to Tools>Board>Boards Manager, search for esp32 and install esp32 by Espressif Systems
  - Make sure it is version `2.0.11`
5. Install the [ CH340X Drivers](https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers/all)

---
## Installation of Arduino IDE Libraries:
1. From this repository, download the `libraries` folder.
2. Copy and paste the `libraries` folder to:
3. `C:\Users\USERNAME\OneDrive\Documents\Arduino`

---
