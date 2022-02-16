For both PC and Mac, you will first need to connect the Blue Arduino Nano board on the steady eddy to your machine using a USB to Mini USB cable.

![image](https://user-images.githubusercontent.com/3416626/152965003-2f0deaf7-17a4-44ff-8d35-319711aeaac9.png)

![image](https://user-images.githubusercontent.com/3416626/152965080-9db6f37e-4e00-4f84-a4f4-3fe298a80c72.png)


## PC

* Download the most recent firmware from the list above (click the latest .hex file > Raw > File > Save Page As)
* Download <a href='https://blog.zakkemble.net/download/AVRDUDESS-2.13-setup.exe'>AVRDudess</a>, install, and run

![image](https://user-images.githubusercontent.com/3416626/152965770-be110290-8501-4cf1-9f3d-a3a4907ce92a.png)

1. Select the correct USB COM port that the device is plugged into
2. Select the .hex file you downloaded earlier
3. Select the Atmega328P
4. Click 'Program!'


## MACOS

1. Download the most recent firmware from the list above (click the latest .hex file > Raw > File > Save Page As)
2. Press `Command+Space` and type `Terminal` and press enter.
3. Install <a href='https://brew.sh/'>homebrew</a> by entering the following command (if not done so already)
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
4. Install avrdude
```
brew install avrdude
```
5. Navigate to your Downloads folder
```
cd Downloads
```
6. Find the USB port you are connected to
```
ls /dev/cu.usbserial*
```
(or if none found)
```
ls /dev/tty.wch*
```
7. Run the following, substituting {port} with the result of step 5
```
avrdude -v -V -patmega328p -carduino -P{port} -b115200 -D -Uflash:w:firmware.hex:i
```
