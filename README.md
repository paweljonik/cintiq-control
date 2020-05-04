# cintiq-control
Control your Wacom Cintiq tablet in linux
## wacom-display-toggle
Script to toggle Wacom input between different outputs/displays. It stores state in ~/.wacom-ouput-switch.state since xsetwacom does not provide such info. It is best utilised with key-binding (e.g. [WIN]+[SPACE] in desktop-environment of your choice.
## cintiq-screen-control
Requires:
- ddcutil
- i2c
- user in i2c group
- for nvidia: echo "options nvidia NVreg_RegistryDwords=RMUseSwI2c=0x01;RMI2cSpeed=100" >> /etc/modprobe.d/nvidia.conf
```
Brightness: |■■■■■■----------------------------------------------| 10/100
  Contrast: |■■■■■■■■■■■■■■■■------------------------------------| 30/100
 Sharpness: |■■■■■■■■■■■■■■■■■■■■■■■■■■--------------------------|  2/4
     Color: [ User 1 (0x0b) ]
       Red: |■■■■■■■■■■■■■■■■■■■■■■■■■■--------------------------|128/255
     Green: |■■■■■■■■■■■■■■■■■■■---------------------------------| 96/255
      Blue: |■■■■■■■■■■■■■---------------------------------------| 64/255
```
Usage: cintiq-screen-control [brightness: 0-100] [contrast: 0-100] [color-profile] [sharpness]
```
--help			- print this message
--usage			- print usage
--factory-defaults	- reset to factory defaults
--bc-defaults		- reset brightness and contrast to defaults
--color-defaults	- reset color profile to defaults
--brightness [0-100]    - get/set brightness
--contrast [0-100]	- get/set contrast
--color [profile]	- get/set color-profile:
			  1 for sRGB
			  2 for Display Native
			  4 for 5000 K
			  5 for 6500 K
			  6 for 7500 K
			  8 for 9300 K
			  11 for User 1
--rgb	[r/g/b 0-255]   - get / set R/G/B values (if set - implies User color profile)
--sharpness [0-4]       - get / set sharpness
```
