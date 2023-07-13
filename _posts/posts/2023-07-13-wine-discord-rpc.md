---
layout: post
title: Enabling Discord RPC for WINE Games
updated: 2023-07-13
category: posts
---

Since Wine doesn't offer a native "native" interface for games running under it to connect to the Discord Rich Presence listener on Linux, here's a short guide on how to make RPC work.

I used this method on Arch Linux, though it should work the same on all other distros too.

## How-to

- Download [this tarball](https://github.com/Marc3842h/rpc-wine/releases/download/1.0.0/rpc-wine.tar.gz) by [Marc3842h](https://github.com/Marc3842h/)
- Extract its content to `/opt/discord-rpc`
- Make sure you have the bin32 and the bin64 directories in `/opt/discord-rpc`
- Open a terminal and append the locations of `bin32` and `bin64` directories to the `WINEDLLPATH` environment variable using the following command `export WINEDLLPATH=$WINEDLLPATH:/opt/discord-rpc/bin64:/opt/discord-rpc/bin32`
- Run winetricks/protontricks, select your wine prefix (default prefix if using protontricks), and run winecfg
- Head to the libraries tab, and add a new override for library by typing in `discord-rpc` and clicking add. Hit Apply, and then OK
- Run your game the way you usually would, and RPC should be working now

Note: This has to be done for each game individually. There might be a way to set it up for all wineprefixes at once, but I'm not aware of how to do that.
