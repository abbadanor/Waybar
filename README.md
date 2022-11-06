# Waybar
Waybar optimized for Hyprland without systemd

Build:
```
meson --prefix=/usr --buildtype=plain --auto-features=enabled --wrap-mode=nodownload build
meson configure -Dexperimental=true build
sudo ninja -C build install

```
