## PC

* Download the most recent firmware from the list above (the latest .hex file)
* Download <a href='https://blog.zakkemble.net/download/AVRDUDESS-2.13-setup.exe'>AVRDudess</a>, install, and run
* 


## MACOS

* Download the most recent firmware from the list above (the latest .hex file)
* Press `Command+Space` and type `Terminal` and press enter.
* Install avrdude
```
brew install avrdude
```
* Navigate to your Downloads folder
```
cd Downloads
```
* Find the USB port you are connected to
```
ls /dev/tty.wch*
```
(or if none found)
```
ls /dev/cu.usbserial*
```
* Run the following, substituting {port} with the result of the previous command
```
avrdude -v -V -patmega328p -carduino -P{port} -b115200 -D -Uflash:w:firmware.hex:i
```
