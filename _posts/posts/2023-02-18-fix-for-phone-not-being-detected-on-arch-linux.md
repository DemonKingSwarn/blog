---
layout: post
title: Fix for phone not being detected on arch linux
updated: 2023-02-18
category: posts
---

I connected a IQOO 9T (with USB debugging and File Transfer enabled) to my Arch Linux computer, however, it was not being detected by `lsblk`, `mtp` (through the `pcmanfm` integration), etc. However, it was being detected by `dmesg` and `lsusb`.

After some fiddling, it turned out that the problem (apparently) was that my computer hadn’t been authorised by the phone.

I ran `adb shell`, causing an authorization popup in the phone. After authorizing the computer, it was able to detect the phone through `lsblk` and mount it through `aft-mtp-mount` etc.

```sh
sudo pacman -S android-file-transfer
aft-mtp-mount /wherever/you/like/to/mount
```
