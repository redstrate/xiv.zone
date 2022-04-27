---
title: "Astra - Installation"
---

The current version is [0.4.0](/astra/changelog).

**Note:** Windows and macOS users currently have to check for updates manually. You can tell which version you have by reading it in the `About` menu under `Help`. I hope to remedy this in the next major release.

### Windows

[Portable ZIP](https://xiv.zone/distrib/astra/0.4.0/astra-0.4.0-win-x64.zip)

SHA256: `e283e6f65abe3546942d17ba240300edc96e2bcb51bf29790b6779be2a5ba7aa`

### macOS

[App](https://xiv.zone/distrib/astra/Astra.app)

_Note: The app is signed and the developer should read as "Joshua Goins"._

### Linux

I'm only providing a Flatpak for now. To install Astra on your Linux system, follow these instructions:

1. [Install Flatpak](https://www.flatpak.org/setup/) if it's not already on your system.
2. [Download the flatpakrepo file](https://www.flatpak.org/setup/) and install it using your preferred GUI Flatpak manager or through the command line:

`flatpak remote-add xiv.zone https://xiv.zone/distrib/flatpak`

3. You can install it directly through your GUI Flatpak manager, or directly from the command line:

`flatpak install xiv.zone.Astra`

A benefit of Flatpak is that it works across most distributions, and I'm able to control the repository so you'll get
any updates without any hassle.

If you're an Arch Linux user, I also maintain the [AUR package](https://aur.archlinux.org/packages/astra-launcher). You can find the PKGBUILD [here](https://git.sr.ht/~redstrate/pkgbuilds/tree/main/item/astra-launcher/PKGBUILD) and the original Flatpak manifests [here](https://git.sr.ht/~redstrate/astra-flatpak).

### Source Code

[Tarball](https://xiv.zone/distrib/astra/0.4.0/astra-source.tar.gz)

SHA256: 97c1f77535d240e56f19a19a8d22c61d57064a20b72ffd524b9206a3fca7860c
