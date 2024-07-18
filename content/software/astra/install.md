---
title: "Install"
aliases:
- /astra/install
---

The stable version currently is **0.6.1**. You can report issues either on [GitHub](https://github.com/redstrate/Astra/issues) or if you prefer then [contact me via e-mail](https://redstrate.com/contact).

See the [changelog](/software/astra/changelog/0.6.1) for this version.

### Flatpak

There is a Flatpak repository available, which is the preferred method to use Astra especially on the Steam Deck. You can open the file below if you use GNOME Software or Plasma Discover:

{{< rawhtml >}}
<div class="buttons">
<a class="blurb-button" href="https://flatpak.xiv.zone/xivzone.flatpakrepo">Download Repository</a>
</div>
{{< /rawhtml >}}

If you prefer using the CLI, use the command below:

```shell
flatpak remote-add --if-not-exists xiv.zone https://flatpak.xiv.zone/xivzone.flatpakrepo
```

### Fedora

I also maintain an RPM which you can find in my [personal COPR](https://copr.fedorainfracloud.org/coprs/redstrate/personal/). After adding my COPR, run `dnf`:

```shell
dnf install astra
```

### Arch Linux

I maintain the [AUR package](https://aur.archlinux.org/packages/astra-launcher). For example, using [aurutils](https://github.com/aurutils/aurutils):

```shell
aur sync astra-launcher
```

### Source Code

If you don't see your preferred distribution listed, it's always possible to build it manually. Please refer to the [build instructions](https://github.com/redstrate/Astra/blob/main/BUILDING.md) for more help.

{{< rawhtml >}}
<div class="buttons">
<a class="blurb-button" href="https://xiv.zone/distrib/astra/0.6.1/astra-source.tar.gz" download>Download source code tarball</a>
</div>
{{< /rawhtml >}}

SHA256: 904f5efab48f87c64fc59c1748354b41bbe5c991d47499332603071bd67f6596

Size: ~256 KiB
