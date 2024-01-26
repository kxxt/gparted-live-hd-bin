# gparted-live-hd-bin

GParted Live on Hard Disk, packaged for Arch Linux.

https://gparted.org/livehd.php

This package enables booting GParted live without a usb drive.

## Requirements

- Arch Linux or derivation
- Grub2
- x86_64 (Actually i686 is also supported by upstream but I don't have hardware to test it so I don't support it in this PKGBUILD)
- Enough space in `/boot` partition (600MB should be enough).

I only tested in UEFI mode. BIOS mode is not tested.

## Warn

Use it at your own risk. I am not responsible for this package or your actions.

## How to use

- Install the package from github releases or build and install it on your own :)
- After installation, regenerate your grub configuration
- Then you can see a gparted live menuentry in grub.

## How it works

- GParted live ISO is stored as `/boot/gparted-live.iso`
- We can boot that iso from grub. That's it!

## Why not publish this PKGBUILD to AUR?

Because it assumes too many things.
I don't want to hear complaints from users who blindly install this package without going through the requirements.
