---
title: "Download Beta"
draft: true
---

{{< note "0.5.0 is currently unreleased. Please only try it if you have nothing to lose!" >}}

This is the download page for 0.5.0. Precompiled builds are currently still a work in progress, please tell me any issues you have in the [issue tracker](https://todo.sr.ht/~redstrate/astra) or the [mailing list](https://lists.sr.ht/~redstrate/public-inbox).

See the [changelog](/astra/changelog/0.5.0) for this version.

### Fedora Linux

Fedora packages are available from my [COPR](https://copr.fedorainfracloud.org/coprs/redstrate/personal/). In your preferred terminal emulator, enable the repository:

```bash
$ dnf copr enable redstrate/personal
```

Astra 0.5.0 uses KDE Frameworks 6, and it is not packaged yet in a stable Fedora version. There is a [KDE 6 COPR](https://copr.fedorainfracloud.org/coprs/g/kdesig/kde-nightly-qt6/) maintained by the Fedora KDE SIG team, which you must install before Astra.

Then you can install Astra like any other package:

```bash
$ dnf install astra
```

### Arch Linux

An Arch Linux package is available on the [AUR](https://aur.archlinux.org/packages/astra-launcher-git) but requires you to figure out how to get KDE Frameworks 6 packages installed on your system.

### Gentoo Linux

A Gentoo package is available in [my personal overlay](https://git.sr.ht/~redstrate/overlay) and instructions on how to use it are located on it's site. In order to install the package you must source the required KDE Frameworks 6 packages yourself, I suggest using my [KF6 overlay](https://git.sr.ht/~redstrate/kf6-overlay).

### Flatpak

A Flatpak is currently unavailable right now. Sorry!

### Source Code

A complete source tarball is available, which is generated via sourcehut CI on every commit. This includes every vendored dependency as well, which is useful for distribution packaging.

{{< rawhtml >}}
<div class="buttons">
<a class="blurb-button" href="https://xiv.zone/distrib/astra/git/astra-source.tar.gz" download>Download source code tarball</a>
</div>
{{< /rawhtml >}}
