# ESP32 Marauder from Source to CYD.
A simple guide to installing the firmware from source without the hassle of editing multiple files.

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

![Screenshot 2024-07-02 103638](https://github.com/jei3m/cyd-marauder/assets/113350529/2fc5e774-6842-4f34-8c19-9b74ab925448)


---
## Replacing `platform.txt` file
1. Download the `platform.txt` file from this repository, then copy it.
2. Go to `C:\Users\USERNAME\AppData\Local\Arduino15\packages\esp32\hardware\esp32\2.0.11`

![Screenshot 2024-07-02 103738](https://github.com/jei3m/cyd-marauder/assets/113350529/d49d4a84-d82b-435d-bebb-8f908db5bd8b)

4. Paste the `platform.txt` you copied from this repository, replacing the existing one from the abovementioned directory.

---
## TFT_eSPI-master
1. Depending on your type of CYD, edit the value of `USER_SETUP.H` inside the `TFT_eSPI-master` library folder.
2. Go to: `C:\Users\USERNAME\OneDrive\Documents\Arduino\libraries\TFT_eSPI-master`
3. Open the `USER_SETUP.H` file.
4. Edit accordingly, depending on your device. Refer to the images below.
- 1 USB CYD w/o GPS:

![1 usb](https://github.com/jei3m/cyd-marauder/assets/113350529/dd4ebd86-2fb1-4a88-972f-94aae91fe393)

- 2 USB CYD w/o GPS

![2usb](https://github.com/jei3m/cyd-marauder/assets/113350529/99c06e5d-2300-4b3f-89cf-3020e2562d09)

The `USER_SETUP.H` is responsible for the inversion of colors. Especially in some cases where you flashed the firmware and the interface displays with a white background.
- Don't forget to hit save.
---
## The Source Code of ESP32 Marauder
1. Download the `esp32_marauder.zip` from this repository and extract it.
2. After extracting the zip file onto a folder, open `esp32_marauder.ino`.
3. Avoid updating libraries, just to be safe.
4. For boards, choose LOLIN D32.

![board](https://github.com/jei3m/cyd-marauder/assets/113350529/1e37c8b4-fa67-4326-8b70-20684b01806d)

6. Your port depends on the value of COM# on where your CYD is connected.
7. Set the Partition Scheme to `MINIMAL SPIFFS (LARGE APP WITH OTA)`
8. Set the upload speed to `115200`

![boardsall](https://github.com/jei3m/cyd-marauder/assets/113350529/a6ebb6cd-42a5-4fe6-b248-8a0b7aa4b92f)

10. Click on verify and hit upload.

---
## Modding the Splash Screen
1. Open the `esp32_marauder.ino` file that is located inside the `esp32_marauder` folder.
2. Look and edit these lines of code:

![ino](https://github.com/jei3m/cyd-marauder/assets/113350529/dd3bdfa5-e697-4151-975a-fdaaf9263102)

