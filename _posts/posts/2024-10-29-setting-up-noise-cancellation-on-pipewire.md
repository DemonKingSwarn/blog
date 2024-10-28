---
layout: post
title: Setting Up Noise Cancellation on Pipewire
updated: 2024-10-29
excerpt: "So like me, most of you guys definitely stumbled on some services which have noise cancellation sometimes not working on linux, Microsoft Teams being one of those. So recently I have started using a PipeWire plugin to setup noise cancellation and honestly it works much better than any other noise cancellation solution provided by these services"
keywords: [pipewire, rnnoise, noise suppression, linux]
category: posts
---

So like me, most of you guys definitely stumbled on some services which have noise cancellation sometimes not working on linux, Microsoft Teams being one of those. So recently I have started using a PipeWire plugin to setup noise cancellation and honestly it works much better than any other noise cancellation solution provided by these services.

So without wasting any time let us begin.

**NOTE:** I will be using [Arch Linux](https://archlinux.org) for this guide as thats what I personally use, but you can do this on any Linux distribution.

**Prerequisites:**

- [PipeWire](https://www.pipewire.org)

## 1. Plugin Installation

```sh
$ sudo pacman -S noise-suppression-for-voice rnnoise
```

## 2. Configuration

```sh
mkdir -p ~/.config/pipewire/pipewire.conf.d
```

In `~/.config/pipewire/pipewire.conf.d`, create a file called `99-input-denoising.conf` and then put the following in it

```conf
context.modules = [
{   name = libpipewire-module-filter-chain
    args = {
        node.description =  "Noise Canceling source"
        media.name =  "Noise Canceling source"
        filter.graph = {
            nodes = [
                {
                    type = ladspa
                    name = rnnoise
                    plugin = /usr/lib/ladspa/librnnoise_ladspa.so
                    label = noise_suppressor_mono
                    control = {
                        "VAD Threshold (%)" 80.0
                        "VAD Grace Period (ms)" 200
                        "Retroactive VAD Grace (ms)" 0
                    }
                }
            ]
        }
        capture.props = {
            node.name =  "capture.rnnoise_source"
            node.passive = true
            audio.rate = 48000
        }
        playback.props = {
            node.name =  "rnnoise_source"
            media.class = Audio/Source
            audio.rate = 48000
        }
    }
}
]
```

After this just restart your computer and your Noise Cancellation will start working.

Now you can make your meetings more effective and enjoy your podcasts and game streams without worrying about the background noise.
