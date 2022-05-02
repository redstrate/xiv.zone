---
title: "Astra - Installation"
---

The current version is [0.4.0](/astra/changelog). These precompiled builds are currently still a work in progress, please tell me any issues you have in the [mailing list](https://lists.sr.ht/~redstrate/astra-dev).

**Note:** Windows and macOS users currently have to check for updates manually. You can tell which version you have by reading it in the `About` menu under `Help`. I hope to remedy this in the next major release.

### Windows

{{< rawhtml >}}
<div class="buttons">
<a class="blurb-button" href="https://xiv.zone/distrib/astra/0.4.0/astra-0.4.0-win-x64.zip" download>Download for Windows (ZIP)</a>
</div>
{{< /rawhtml >}}

SHA256: `e283e6f65abe3546942d17ba240300edc96e2bcb51bf29790b6779be2a5ba7aa`

### macOS

{{< rawhtml >}}
<div class="buttons">
<a class="blurb-button" href="https://xiv.zone/distrib/astra/Astra.app" download>Download for macOS</a>
</div>
{{< /rawhtml >}}

_Note: The app is signed and the developer should read as "Joshua Goins"._

### Linux

I'm only providing a [Flatpak](https://www.flatpak.org/setup/) for now. Unfortunately it's not on Flathub yet, but I've created a repository specifically for xiv.zone applications:

{{< rawhtml >}}
<div class="buttons">
<a class="blurb-button" href="https://xiv.zone/distrib/flatpak/xivzone.flatpakrepo" download>Install Flatpak Repository</a>
</div>
{{< /rawhtml >}}

You can install it through your preferred GUI Flatpak manager, using the link below or by searching:

{{< rawhtml >}}
<div class="buttons">
<a class="blurb-button" href="appstream://zone.xiv.Astra" download>Install Astra for Linux</a>
</div>
{{< /rawhtml >}}

Or by the command-line if you prefer:

`flatpak install xiv.zone.Astra`

A benefit of Flatpak is that it works across most distributions, and I'm able to control the repository so you'll get
any updates without any hassle.

If you're an Arch Linux user, I also maintain the [AUR package](https://aur.archlinux.org/packages/astra-launcher). You can find the PKGBUILD [here](https://git.sr.ht/~redstrate/pkgbuilds/tree/main/item/astra-launcher/PKGBUILD) and the original Flatpak manifests [here](https://git.sr.ht/~redstrate/astra-flatpak).

### Source Code

[Tarball](https://xiv.zone/distrib/astra/0.4.0/astra-source.tar.gz)

SHA256: 97c1f77535d240e56f19a19a8d22c61d57064a20b72ffd524b9206a3fca7860c
