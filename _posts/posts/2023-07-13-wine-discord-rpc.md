---
layout: post
title: Enabling Discord RPC for WINE Games
updated: 2023-11-16
category: posts
---

Since Wine doesn't offer a native "native" interface for games running under it to connect to the Discord Rich Presence listener on Linux, here's a short guide on how to make RPC work.

I used this method on Arch Linux, though it should work the same on all other distros too.

## How-to

- Download [this tarball](https://web.archive.org/web/20250602095446/https://objects.githubusercontent.com/github-production-release-asset-2e65be/137587190/3d937d22-82b4-11e8-9c00-b8059d9df9dd?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=releaseassetproduction%2F20250602%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250602T095446Z&X-Amz-Expires=300&X-Amz-Signature=312f3572371c3996aa6534c7af834373bd39a2e4186d56b9d2dc7df6f807e7c8&X-Amz-SignedHeaders=host&response-content-disposition=attachment%3B%20filename%3Drpc-wine.tar.gz&response-content-type=application%2Foctet-stream) by [Marc3842h](https://github.com/Marc3842h/)
- Extract its content to `/opt/discord-rpc`
- Make sure you have the bin32 and the bin64 directories in `/opt/discord-rpc`
- Open a terminal and append the locations of `bin32` and `bin64` directories to the `WINEDLLPATH` environment variable using the following command `export WINEDLLPATH=$WINEDLLPATH:/opt/discord-rpc/bin64:/opt/discord-rpc/bin32`
- Run winetricks/protontricks, select your wine prefix (default prefix if using protontricks), and run winecfg
- Head to the libraries tab, and add a new override for library by typing in `discord-rpc` and clicking add. Hit Apply, and then OK
- Run your game the way you usually would, and RPC should be working now
