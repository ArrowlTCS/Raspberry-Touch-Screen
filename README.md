# Raspberry-Touch-Screen
A guide to adding touchscreen support for any Waveshare touchscreen display to various OSes.

This apparently works on any OS with a /boot/firmware/config.txt, or if the OS is _very_ old, /boot/config.txt, but I have yet to check evry single OS, for obvious reasons.

# Options:

* Add ```dtoverlay=ads7846,cs=1,penirq=25,penirq_pull=2,speed=50000,keep_vref_on=0,swapxy=0,pmax=255,xohms=150,xmin=200,xmax=3900,ymin=200,ymax=3900``` to your /boot/firmware/config.txt file.
(credit: https://forums.raspberrypi.com/viewtopic.php?t=375432)

OR

* Use the below repository that will enable touchscreen and gestures on your RPi via terminal:
  - https://github.com/tobykurien/rpi_tablet_os
 

Tested OSes for adding to the /boot/config.txt:

* Ubuntu Touch
  - requires dtoverlay=disableoverscan
  - requires screen calibration
* Raspberry Pi OS
  - requires screen calibration
* Android 10 (Lineage 17.1) by KonstaKANG
  - no need to add, just uncomment line below #Waveshare touchscreen
  - requires screen calibration
* Android 9 (Lineage 16.0) by KonstaKANG
  - no need to add, just uncomment line below #Waveshare touchscreen
  - requires screen calibration


Tested OSes for the repo:
* Ubuntu


Theoretically Supported OSes:
* POP OS
* Ubuntu MATE
* Ultramarine Linux
* LibreELEC
* OpenELEC
* RISC OS Pi
* OSMC
* Recalbox
* RetroPie
* Kali Linux
* many more
