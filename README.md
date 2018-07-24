
Ultimaker 2 - AndroidThings 3D Print Server based on Pico Pro Maker Kit
------------------------
<p align="center">
<img src="https://d15z4ngi7vchau.cloudfront.net/media/catalog/product/cache/1/image/9df78eab33525d08d6e5fb8d27136e95/p/i/pico-pi-imx7-startkit-overview.jpg" height="400" width=auto>
</p>

### OVERVIEW ###
3D printer server based on Pico Pro Maker Kit & wonderful app by MDCode - GCodePrintr

### Hardware ###
* Pico Pro Maker Kit
* PC with adb tools

### Installation ###
First we need to install some software buttons back/home, will do it by installing:<br>
https://play.google.com/store/apps/details?id=com.appspot.app58us.backkey&hl=iw

AndroidThings doesn't not nativly show accessability options, will need to enable it by - 
```
adb install com.appspot.app58us.backkey.apk
adb shell settings put secure enabled_accessibility_services %accessibility:com.appspot.app58us.backkey/com.appspot.app58us.backkey.BackkeyService
```

Configure by running - 
```
adb shell am start -n com.appspot.app58us.backkey/com.appspot.app58us.backkey.MainActivity
```

Install the great app GCodePrintr (PAY 4.5$!!)<br>
https://play.google.com/store/apps/details?id=de.dietzm.gcodesimulatorprinter
```
adb install de.dietzm.gcodesimulatorprinter.apk
```

In order to run the app on boot will use:<br>
https://play.google.com/store/apps/details?id=com.autostart

Run on adb -
```
adb shell am start -n com.autostart/com.autostart.AutoStartActivity
```
Configure it to run GCodePrintr at startup.


Download PC version of GCodePrintr from -<br>
https://www.thingiverse.com/thing:44286

Now you can send the Gcode(from slic3r, Simplify3D, Cura etc.) directly to your printer server through WIFI.

### Examples ###
<p align="center">
<img src="https://github.com/Itamare4/dji_ronin/blob/master/MD_Images/Selection_003.png?raw=true" height="300"><br>Image processing using OpenCV<br></p>

<p align="center"><img src="https://github.com/Itamare4/dji_ronin/blob/master/MD_Images/Gimbal.gif?raw=true" width="200"><br>
DJI Ronin controlled by dji_ronin node<br></p>

<p align="center"><img src="https://github.com/Itamare4/dji_ronin/blob/master/MD_Images/Selection_004.png?raw=true" height="200"><br>Arduino RC Circuit</p>




