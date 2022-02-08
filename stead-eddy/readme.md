## PC

* Download the most recent firmware from the list above (the latest .hex file)
* Download <a href='https://blog.zakkemble.net/download/AVRDUDESS-2.13-setup.exe'>AVRDudess</a>, install, and run
* 


## MACOS

* Download the most recent firmware from the list above (the latest .hex file)
* Download <a href='https://blog.zakkemble.net/download/AVRDUDESS-2.13-portable.zip'>AVRDudess portable</a>, and extract to `/Downloads/AVRDUDESS-2.13-portable`
* Open a command line
* Navigate to your Downloads folder (or whichever folder you extracted AVRDudess) and run AVRDudess using mono
```
cd Downloads
cd AVRDUDESS-2.13-portable
```
* Find the USB port you are connected to
```
ls /dev/tty.wch*
```
* Run the following, substituting {port} with the result of the previous command
```

```
