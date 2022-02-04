# GPD Pocket 2 Screen Rotate

GPD Pocket 2 has a touch screen, its pointer device of touch screen cannot be automatically rotated with xrandr, so this script was born.

## 1. Usage

```shell
gpdp2_screen_rotate [orientation]
```

will rotate the screen and pointer of touch screen clockwise at the same time, or you can specify orientation.

## 2. About The Device

This is the output of `xinput` of my GPD Pocket 2, and this script will only change the calibration matrix for device `pointer:Goodix Capacitive TouchScreen`.

```plain
⎡ Virtual core pointer                    	id=2	[master pointer  (3)]
⎜   ↳ Virtual core XTEST pointer              	id=4	[slave  pointer  (2)]
⎜   ↳ HAILUCK CO.,LTD USB KEYBOARD Mouse      	id=12	[slave  pointer  (2)]
⎜   ↳ Goodix Capacitive TouchScreen           	id=15	[slave  pointer  (2)]
⎣ Virtual core keyboard                   	id=3	[master keyboard (2)]
    ↳ Virtual core XTEST keyboard             	id=5	[slave  keyboard (3)]
    ↳ Power Button                            	id=6	[slave  keyboard (3)]
    ↳ Video Bus                               	id=7	[slave  keyboard (3)]
    ↳ Power Button                            	id=8	[slave  keyboard (3)]
    ↳ Sleep Button                            	id=9	[slave  keyboard (3)]
    ↳ HAILUCK CO.,LTD USB KEYBOARD            	id=10	[slave  keyboard (3)]
    ↳ HAILUCK CO.,LTD USB KEYBOARD Wireless Radio Control	id=11	[slave  keyboard (3)]
    ↳ HAILUCK CO.,LTD USB KEYBOARD System Control	id=13	[slave  keyboard (3)]
    ↳ HAILUCK CO.,LTD USB KEYBOARD Consumer Control	id=14	[slave  keyboard (3)]
    ↳ Intel HID events                        	id=16	[slave  keyboard (3)]
    ↳ Intel HID 5 button array                	id=17	[slave  keyboard (3)]
    ↳ Goodix Capacitive TouchScreen           	id=18	[slave  keyboard (3)]
```

This is the output of `xrandr` of my GPD Pocket 2, and this script will only change the orientation of xrandr output `eDP1`.

```plain
Screen 0: minimum 8 x 8, current 1920 x 1200, maximum 32767 x 32767
eDP1 connected primary 1920x1200+0+0 right (normal left inverted right x axis y axis) 95mm x 151mm
   1200x1920     60.02*+
   1024x768      60.00  
   1024x576      59.90    59.82  
   600x960       60.00  
   960x540       59.63    59.82  
   800x600       60.32    56.25  
   864x486       59.92    59.57  
   640x480       59.94  
   720x405       59.51    58.99  
   640x360       59.84    59.32  
DP1 disconnected (normal left inverted right x axis y axis)
HDMI1 disconnected (normal left inverted right x axis y axis)
VIRTUAL1 disconnected (normal left inverted right x axis y axis)
```
