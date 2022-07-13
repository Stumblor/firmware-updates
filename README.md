![image](https://user-images.githubusercontent.com/3416626/146519116-27e0c64f-bc0b-44f8-83ff-b28c550571a6.png)

### Updating your Mod Firmware

#### The Easiest Way

*This method is only available to mods that have firmware download capability, such as the GZ "Tokyo Neon" sign mod.*

1. Turn on your machine, and then **enter the service menu**. Ensure the device is powered (you may need to re-close your coin door).
2. Connect to your Wifi Access point (example: Stumblor-{device name}-xxxx)
3. Open a browser and type **192.168.4.1** into the address bar.
4. Click 'Settings', then 'Update Firmware'.
5. Enter your HOME Wifi details and then click the Test/Connect button. If the Wifi connect fails, try to put the device closer to your router, or if that is not possible, setup a wifi hotspot on your phone and connect to that.
6. Wait to see if any update is required.
7. If a new version was found, click 'Download Latest & Install'. 
8. Wait for the download & installation to complete. The device will then reset. You may need to reconnect to your Access point (step 2) and possibly do another power cycle of the device to complete the process.

#### The Slightly Less Easy Way

1. Find your mod in the directories above. If there is a version number, check what is written on your board.
2. Open the folder, and download the latest firmware (click .bin file > Download)
3. Power the device
  * If installed, power up your game and go into the machine's Test Menu using the coin door controls (it is important to have steady power, not attract mode!).
  * If uninstalled, the easiest way to power Lollypops is to use a 9V battery and your alligator clips. Red to positive, Black to negative. For other devices, check the pinout.

    ![image](https://user-images.githubusercontent.com/3416626/133926847-52d98d64-d494-41fb-b7c8-ddf0166606c7.png)

    ![image](https://user-images.githubusercontent.com/3416626/133926854-f6d35e71-669c-4c4b-84df-e83bc10cbb64.png)


4. Connect to your Wifi Access point (example: Stumblor-{device name}-xxxx)
5. Open a browser and type **192.168.4.1** into the address bar
6. Click 'Settings', then 'Update Firmware'
7. Enter your HOME Wifi details and then click the Test/Connect button. If the Wifi connect fails, try to put the device closer to your router, or if that is not possible, setup a wifi hotspot on your phone and connect to that.
8. Once connected, browse for the firmware file you downloaded earlier to begin firmware update.
9. Wait for the update to reach 100%. The board will then take 10 seconds or so to install, re-check settings, and then reboot. Once you see the board is active again, you can navigate back to **192.168.4.1** to check settings. Occaisionally the update will stop before reaching 100%. If that happens, refresh the browser and retry from step 7.

#### The Hard Way

If you find yourself unable to access the web UI, you can also update using a FTDI programmer. Different flavours if FTDI programmers have different layouts, so make sure you take a look at your documenation to ensure you are connecting to the right pins.

![image](https://user-images.githubusercontent.com/3416626/138160041-0c45ab58-f65d-4d75-89f1-a1b4c3f383f7.png)

* Download the latest firmware from this folder (click .bin file > Download)
* run **pip install esptool**
* run **esptool.py --chip esp8266 erase_flash**
* run **esptool.py --chip esp8266 write_flash 0x0000 {name of the file you downloaded}**
