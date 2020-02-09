# cintiq-control
Control your Wacom Cintiq tablet in linux
## wacom-output-switch
Script to toggle Wacom input between different outputs/displays. It stores state in ~/.wacom-ouput-switch.state since xsetwacom does not provide such info. It is best utilised with key-binding (e.g. [WIN]+[SPACE] in desktop-environment of your choice.
## cintiq-screen-control
Script to control Wacom Cintiq screen brightness, contrast and color profile. It can take up to three arguments:
1) Brightness [0-100]
2) Contrast [0-100] and
3) Color profile [1, 2, 4, 5, 6, 8 or 11 for for sRGB, Display Native, 5000K, 6500K, 7500K, 9300K and User 1 respectively.]
cintiq-screen-control requires ddcutil and sudo or user in i2c group
It may eventually become renamed to something more generic as ddcutil can control any screen it detects - not just Cintiqs.
