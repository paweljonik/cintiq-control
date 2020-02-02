# cintiq-control
Control your Wacom Cintiq tablet in linux
## cintiq-output-switch
Script to switch Wacom Cintiq input between different outputs/monitors. It stores state in ~/.cintiq-ouput-switch.state since xsetwacom does not provide such info.
## cintiq-screen-control
Script to control Wacom Cintiq screen brightness, contrast and color profile. It can take up to three arguments:
1) Brightness [0-100]
2) Contrast [0-100] and
3) Color profile [1, 2, 4, 5, 6, 8 or 11 for for sRGB, Display Native, 5000K, 6500K, 7500K, 9300K and User 1 respectively.]

