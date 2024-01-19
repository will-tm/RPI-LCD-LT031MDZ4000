# RPI-LCD-LT031MDZ4000
Raspberry Pi panel driver for JDI LT031MDZ4000 720x720 display

# LCD Adapter board for Raspberry Pi
![Adapter](https://raw.githubusercontent.com/will-tm/RPI-LCD-LT031MDZ4000/main/images/result.jpg)


# Get kernel source
Refer to [rpi-source](https://github.com/RPi-Distro/rpi-source)


# Build & Install
```
git clone https://github.com/will-tm/RPI-LCD-LT031MDZ4000.git
cd RPI-LCD-LT031MDZ4000
make
make install
```
Then edit /boot/config.txt to add:
```
lcd_ignore=1
dtoverlay=vc4-kms-dsi-lt031mdz4000
```
and reboot

LCD pins defaults to:
- Reset - GPIO26
- BL_Enable - GPIO19
- PWM - GND

Default pins can be changed, for example:
```
#change Reset to GPIO5,BL_Enable to GPIO6
dtoverlay=vc4-kms-dsi-lt031mdz4000,bl_en=5,reset=6

```

# Hardware

Datasheet - [LT031MDZ4000-Datasheet](https://www.panoxdisplay.com/uploadfile/datasheet/LT031MDZ4000.pdf)

Proof-of-concept schematics - cf. repository KiCad project.

Important notes:
- This schematics comes with no warranties, use at your own risk

