---
layout: post
title: My New Desktop Hyprland
updated: 2024-02-02
category: posts
---

[Hyprland](https://github.com/hyprwm/hyprland) is an amazing wayland compositor. Here is my current setup that is being made.

# The Desktop

![Hyprland](https://raw.githubusercontent.com/DemonKingSwarn/blog/master/assets/images/swappy-20240202_193536.png)

GitHub Project: https://github.com/demonkingswarn/dotfiles

# Install

## Paru
Run as user NOT ROOT!

```sh
git clone https://aur.archlinux.org/paru-bin
cd paru-bin
makepkg -si
```

## Packages

```sh
paru -S hyprland polkit-gnome ffmpeg neovim rofi-lbonn-wayland rofi-file-browser-extended-git hyprpaper hyprpicker-git waybar-hyprland xdg-desktop-portal xdg-desktop-portal-hyprland nemo obs-studio floorp-bin grim slurp swappy pamixer brightnessctl dunst wl-clipboard xclip
```

# Work In Progress

- Help popup with hotkey
