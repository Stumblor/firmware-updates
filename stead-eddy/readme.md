## PC

* Download the most recent firmware from the list above (the latest .hex file)
* Download <a href='https://blog.zakkemble.net/download/AVRDUDESS-2.13-setup.exe'>AVRDudess</a>, install, and run
* 


## MACOS

* Download the most recent firmware from the list above (the latest .hex file)
* Download avrdude.conf from the list above
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
avrdude -Cavrdude.conf -v -V -patmega328p -carduino -P/dev/cu.wchusbserial1430 -b115200 -D -Uflash:w:/var/folders/6r/j_h8gfzd1xs55kvgr9l1hr440000gn/T/arduino_build_95019/afterglow_gi_arduino.ino.hex:i 
```
