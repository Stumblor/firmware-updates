![image](https://user-images.githubusercontent.com/3416626/146519116-27e0c64f-bc0b-44f8-83ff-b28c550571a6.png)

### Updating you Firmware

#### The Easy Way

* Find your mod in the directories above. If there is a version number, check what is written on your board.
* Open the folder, and download the latest firmware (the .bin file at the bottom of the list)
* Power the device
  * If uninstalled, the easiest way is to use a 9V battery and your alligator clips. Red to positive, Black to negative.

    ![image](https://user-images.githubusercontent.com/3416626/133926847-52d98d64-d494-41fb-b7c8-ddf0166606c7.png)

    ![image](https://user-images.githubusercontent.com/3416626/133926854-f6d35e71-669c-4c4b-84df-e83bc10cbb64.png)

  * If installed, power up your game and go into the machine's Test Menu using the coin door controls.
* Connect to your Wifi Access point (example: Stumblor-Lollypops-xxxx)
* Open a browser and type **192.168.4.1** into the address bar
* Click 'Update Firmware'
* Enter your HOME Wifi details, then click 'Test'
* Once connected, browse for the firmware file you downloaded earlier
* Wait for the update to complete

#### The Hard Way

If you find yourself unable to access the web UI, you can also update using a FTDI programmer. Different flavours if FTDI programmers have different layouts, so make sure you take a look at your documenation to ensure you are connecting to the right pins.

![image](https://user-images.githubusercontent.com/3416626/138160041-0c45ab58-f65d-4d75-89f1-a1b4c3f383f7.png)

* Download the latest firmware from this folder (the .bin file at the bottom of the above list)
* run **pip install esptool**
* run **esptool.py --chip esp8266 erase_flash**
* run **esptool.py --chip esp8266 write_flash 0x0000 {name of the file you downloaded}**
