# AGS v1.8.2 forever

<img width="1919" height="1081" alt="image" src="https://github.com/user-attachments/assets/2a00567e-401c-4ad5-a455-df80bab5f7a0" />

## Why does this fork exist?

Aylur has forsaken us with his newer AGS versions and not everyone is happy with this. Not even the legendary [end-4](https://github.com/end-4) who has switched to quickshell ever since.

But I'm too stubborn to let AGS v1 go. That's why this fork exists: It promises survival. AGS v1 will keep breathing as long as I feel like fighting the build system.

Since the beginning of 2025 I've been occasionally making small changes to the source code of AGS so as to ensure it still compiles and executes without errors. However, every now and then, updates of GTK (or Hyprland) (or anything in-between) might completely break the integrity of this fork and I will have to patch it back again. So... good luck to me, I guess?

## How to install

```sh
sudo pacman -S typescript npm meson gjs gtk3 gtk-layer-shell gnome-bluetooth-3.0 upower networkmanager gobject-introspection libdbusmenu-gtk3 libsoup3
git clone https://github.com/iluvgirlswithglasses/ags-v1
cd ags-v1
npm install
meson setup build --prefix=/usr
meson compile -C build
meson install -C build
```

**Notes:**
- Sometimes `npm install` behaves, sometimes it doesn't. You may download the `node_modules` in [release tag](https://github.com/iluvgirlswithglasses/ags-v1/releases/tag/node_modules) instead of running this command.
- The `--prefix=/usr` on the `meson setup` is not optional. Skip it and AGS won't find its libraries at all.
