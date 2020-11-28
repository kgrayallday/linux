# My Linux (Debian) Setup

### Machine/Hardware
Mid 2012 MacBookAir5,2 (A1466)
1.8 GHz Core i5
8Gb Ram / 128 Gb SSD

### Desktop Environment: 
KDE Plasma

### Fix "$USER not in sudoers file" after Debian install
```
$ su
$ echo "yourusername ALL=(ALL) ALL" >> /etc/sudoers
```

### Customize Application Menu Icon
Octopi
System Icons > Status > "Octopi-ok" || "Octopi-Indicator"

### Customize Trackpad 
Install libinput && xdotool && fusuma

~/.config/fusuma/config.yml
<iframe
  src="https://carbon.now.sh/embed?bg=rgba%2898%2C99%2C101%2C1%29&t=one-dark&wt=none&l=auto&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=14px&lh=133%25&si=false&es=2x&wm=false&code=swipe%253A%250A%2520%25203%253A%250A%2520%2520%2520%2520left%253A%250A%2520%2520%2520%2520%2520%2520command%253A%2520%27xdotool%2520key%2520ctrl%252Balt%252BRight%27%250A%2520%2520%2520%2520%2520%2520%2523%2520move%2520to%2520left%2520workspace%250A%2520%2520%2520%2520right%253A%250A%2520%2520%2520%2520%2520%2520command%253A%2520%27xdotool%2520key%2520ctrl%252Balt%252BLeft%27%250A%2520%2520%2520%2520%2520%2520%2523%2520move%2520to%2520right%2520workspace%250A%2520%2520%2520%2520up%253A%250A%2520%2520%2520%2520%2520%2520command%253A%2520%27xdotool%2520key%2520ctrl%252Balt%252BUp%27%250A%2520%2520%2520%2520%2520%2520%2523%2520move%2520to%2520above%2520activity%250A%2520%2520%2520%2520%2520%2520threshold%253A%25201.5%250A%2520%2520%2520%2520down%253A%250A%2520%2520%2520%2520%2520%2520command%253A%2520%27xdotool%2520key%2520ctrl%252Balt%252BDown%27%250A%2520%2520%2520%2520%2520%2520%2523%2520move%2520to%2520below%2520activity%250A%2520%2520%2520%2520%2520%2520threshold%253A%25201.5%250A%2520%25204%253A%250A%2520%2520%2520%2520up%253A%250A%2520%2520%2520%2520%2520%2520command%253A%2520%27xdotool%2520key%2520ctrl%252BF8%27%250A%2520%2520%2520%2520%2520%2520%2523%2520show%2520the%2520desktop%2520grid%250A%2520%2520%2520%250Apinch%253A%250A%2520%25202%253A%250A%2520%2520%2520%2520in%253A%250A%2520%2520%2520%2520%2520%2520command%253A%2520%27xdotool%2520key%2520ctrl%252Bplus%27%250A%2520%2520%2520%2520%2520%2520threshold%253A%25200.1%250A%2520%2520%2520%2520out%253A%250A%2520%2520%2520%2520%2520%2520command%253A%2520%27xdotool%2520key%2520ctrl%252Bminus%27%250A%2520%2520%2520%2520%2520%2520threshold%253A%25200.1"
  style="width: 513px; height: 708px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Put the following in /usr/share/X11/xorg.conf.d/30-touchpad.conf in order to keep tap click while also disabling tap to drag
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
