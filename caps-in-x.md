# Use Caps Lock for escape in X11

Edit `/etc/X11/xorg.conf.d/00-keyboard`:

```
# Read and parsed by systemd-localed. It's probably wise not to edit this file
# manually too freely.
Section "InputClass"
        Identifier "system-keyboard"
        MatchIsKeyboard "on"
        Option "XkbLayout" "us"
        Option "XkbModel" "pc105"
        Option "XkbVariant" "dvorak-alt-intl"
	Option "XkbOptions" "caps:escape"
EndSection
```

And reboot.
