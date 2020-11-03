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
      command: 'xdotool key ctrl+alt+Left'
    right:
      command: 'xdotool key ctrl+alt+Right'
    up:
      command: 'xdotool key ctrl+alt+Up'
      threshold: 1.5
    down:
      command: 'xdotool key ctrl+alt+Down'
      threshold: 1.5
  4:
    up:
      command: 'xdotool key ctrl+F8'

      
pinch:
  2:
    in:
      command: 'xdotool key ctrl+plus'
      threshold: 0.1
    out:
      command: 'xdotool key ctrl+minus'
      threshold: 0.1
```

### Themes 
Desktop: Arc Dark

Cursor: Breeze
