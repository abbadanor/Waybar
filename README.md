# Waybar
Waybar optimized for Hyprland without systemd

Build:
```
sed -i 's/zext_workspace_handle_v1_activate(workspace_handle_);/const std::string command = "hyprctl dispatch workspace " + name_;\n\tsystem(command.c_str());/g' src/modules/wlr/workspace_manager.cpp
meson --prefix=/usr --buildtype=plain --auto-features=enabled --wrap-mode=nodownload build
meson configure -Dexperimental=true build
sudo ninja -C build install

```
