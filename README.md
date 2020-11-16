# My Linux (Debian) Setup

### Machine/Hardware
Mid 2012 MacBookAir5,2 (A1466)
1.8 GHz Core i5
8Gb Ram / 128 Gb SSD

### Desktop Environment: 
KDE Plasma

### Customize Application Menu Icon
Octopi
System Icons > Status > "Octopi-ok" || "Octopi-Indicator"

### Customize Trackpad 
Install libinput && xdotool && fusuma

~/.config/fusuma/config.yml
```
swipe:
  3:
    left:
      command: 'xdotool key ctrl+alt+Right'
      # move to left workspace
    right:
      command: 'xdotool key ctrl+alt+Left'
      # move to right workspace
    up:
      command: 'xdotool key ctrl+alt+Up'
      # move to above activity
      threshold: 1.5
    down:
      command: 'xdotool key ctrl+alt+Down'
      # move to below activity
      threshold: 1.5
  4:
    up:
      command: 'xdotool key ctrl+F8'
      # show the desktop grid
   
pinch:
  2:
    in:
      command: 'xdotool key ctrl+plus'
      threshold: 0.1
    out:
      command: 'xdotool key ctrl+minus'
      threshold: 0.1
```
Put the following in /usr/share/X11.xorg.conf.d/30-touchpad.conf in order to keep tap click while also disabling tap to drag
```
Section "InputClass"
Identifier "touchpad"
Driver "libinput"
  MatchIsTouchpad "on"
  Option "Tapping" "on"
  Option "NaturalScrolling" "on"
  Option "ClickMethod" "clickfinger"
  Option "TappingDrag" "false"
EndSection
```

### Themes 
Desktop: Arc Dark

Cursor: Breeze
