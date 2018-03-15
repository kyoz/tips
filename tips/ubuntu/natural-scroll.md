Terminal:

```bash
sudo gedit /usr/share/X11/xorg.conf.d/10-evdev.conf
```

Then add `Option "ButtonMapping" "1 2 3 5 4 6 7 8"` to `InputClass` like below

```
Section "InputClass"
         Identifier "evdev pointer catchall"
         MatchIsPointer "on"
         MatchDevicePath "/dev/input/event*"
-------> Option "ButtonMapping" "1 2 3 5 4 6 7 8"
         Driver "evdev"
EndSection
```

Save and restart to take effect.