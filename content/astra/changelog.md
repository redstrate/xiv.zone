# Astra
## Changelog

### 0.4.0

**Note: this is not released yet.**

It's time for another big release of Astra! There's a lot of exciting features this time around, including:

#### Game boot updating support

This is a small but important change, as this is a sort of "baby step" towards game patch support. To clairfy, your "game boot" is the files in the `boot` folder in your
game directory. This includes stuff like the official launcher, ffxivboot.exe, among other things. This happens transparently when you log in, just like the official launcher does.

#### Game installation support

Astra can now install the game for you if you don't have it installed already! Unfortunately due to unshield (the library it uses to extract game data from the installer) is not yet available for Windows, so this feature is limited to macOS and Linux users at the moment. I hope to have this fixed soon.

#### Prebuilt binaries and AUR packages are now available!

Now at long last there are now prebuilt binaries available! I'm very sorry this took so long, but I wanted to make sure the launcher was in a good place before I started distributing these to users that aren't developers. However there are some notes for each platform:

##### Windows

Unfortunately I do not have an installer prepared, so this is a "portable binary". Just put this anywhere (it doesn't matter where) and run it. The application data is stored in your `AppData` folder, so it doesn't matter where you place the executable. This should work on any recent Windows version, but I only have tested Windows 10 personally.
Unfortunately, **this application does not auto-update at the moment**.

##### macOS

I do have an Apple Developer license, so the app is notarized to work outside of the App Store. Please confirm the developer reads as "Joshua Goins" so you know the app is coming directly from me. Unfortunately, **this app does not auto-update at the moment**.

##### Linux

If you're on Arch Linux, I also maintain the AUR package so that's an option for you as well. I hope to expand my Linux package offerings later on. Unfortunately there is no other precompiled binaries, but I am working on publishing a Flatpak soon.

### News & Topics

Now you can view the news in Astra, so you aren't missing out! Right now the news selection is incredibly basic, and you only get the main banner nor does it properly "slideshow". I hope to address this soon in a follow up release.

### More asset updates

The asset updater got an overhaul, and now will display in a pretty little dialog window that is now cancellable! Fortunately, this dialog should never show up as the gooatscorp CDN and my webserver is plenty fast to download from, so don't freak out if you don't see anything.

### Additional stuff
* The login error message is now pulled directly from Square Enix's response, such as "timeout" and "locked accout" errors that might occur.
* Astra now uses libxiv. This is included as a submodule so no seperate install is required.
* Astra and nativelauncher's communication is now much more stable, and you will get less bootups with Dalamud not injecting properly.
* Unencrypted game arguments now work again, and custom wine executables are fixed. Thank you @mariakeating for your contribution!

---

### 0.3.1

This is a incremental release, meant for the eventual release on the AUR.

However, it does include some important changes:
* Dalamud assets and runtime are now downloaded automatically and also kept up to date for you.
* System libraries are now used for qt5-keychain and quazip if found on your system.

---

### 0.3.0

Hello again! It's time for another big update :-)

#### Name Change
If you haven't noticed already, I changed the name from `xivlauncher` to Astra! Now that this is finally out of the way, I can start distributing packages (I've started on a PKGBUILD already for Arch users) and it's another step towards being fully stable. Unfortunately this means your **config is lost unless you rename it manually**. Dalamud and nativelauncher will automatically redownload to the new data directory as well, but you can rename that as well.

#### Dalamud support
This is a big feature that I've been working on, and now it's finally ready to enter beta testing! For now, it is required to have **XIVLauncher
installed through Wine already**. The asset updater built into Astra doesn't have the capabilities to bootstrap a fresh Dalamud environment on it's own yet, so XIVQuickLauncher is still required for that purpose, although I recommend having it installed anyway :-)

Simply **tick the "Enable Dalamud Injection" setting** in your profile, and Dalamud/nativelauncher will download automatically and Astra will take care of the injection for you. Major thanks to the XIVQuickLauncher devs for writing the original ACL bypass relocated [here](https://github.com/redstrate/nativelauncher).

Dalamud is also automatically updated to the latest stable version automatically, in the future I hope to expand the updating options.

#### CLI Interface
There is now a basic CLI interface, and see you check all of it's options by running `astra --help`. This is pretty basic, but there's enough to have a nice auto-login script going. This isn't a true GUI-less experience though, as Astra still depends on Qt5 heavily, but I hope this is a good enough :-)

#### Maintenance Checks
The login button is now automatically disabled when Astra detects that the game server is under maintenance. In the future, I hope to make this feature more robust.

#### Arch Linux CI builds
Thank you @pepper-jelly for contributing the Github action, which runs and **automatically generates an Arch Linux binary to download**. This still is not ideal though, as this requires a Github account to download, but in the future I will provide real releases.

#### Settings are reorganized
The settings are reorganized a bit, i'm still not completely happy with the layout but it's much, much better than it was before.

![image](https://user-images.githubusercontent.com/54911369/155547834-08f46a7d-4201-4edb-abc9-c0b2a833eb84.png)

**Gamescope settings** were also added, which includes stuff like width, height, refresh rate and so on. I hope to keep expanding these in the future with more of the wine tweaks. Also, gamescope and gamemode are automatically disabled if they are not installed on your system.

There is now a dedicated Dalamud options box, I hope to expand this in the future with being able to enable/disable mods before launching the game, etc. This is part of my effort to better support dedicated/external tools (#14).

The boot/dalamud versions are now displayed in the profile settings as well!

#### Automatically closing
There is now an option to **automatically "close" Astra when the game is launched**, similar to how the official launcher and XIVQuickLauncher works. Due to how our processes are handled, the actual Astra process does not close, but is hidden until the game itself is closed - and that's when the actual application process quits. This option is **enabled by default**.

#### Tags are now signed
I now have a [public GPG key](https://redstrate.com/gpg-0x1DF57CA30D92A21B-2022-02-02.asc), and I will be **signing tags from now on**. This is to test the waters and make sure my GPG key is stable and works before I start having to sign more stuff - like commits, binary packages, and the like. This is also going to be essential for any packages that have be verified using my key.

#### Experimental stuff
There is also some experimental/untested stuff included in this release. When Endwalker launched, I quickly added [Watchdog](https://github.com/redstrate/astra/wiki/Watchdog) to help me through the long login queues. Also, I managed to forget about Steam support, so I skimmed and implemented a Steam option, but I don't have the game on Steam to test yet.

---

### 0.2.0

This is a major beta release which adds a bunch new features!

- Multiple profile support
  - All of the settings you already use are now configurable, per profile. This includes server type, directx mode, and a whole bunch of neat configurable things. For people testing Sapphire servers or different types of wine this should be extremely useful!
- Encrypted game argument support
  - On Windows, FFXIV "encrypts" (not really, just obfuscates) the game arguments otherwise your game login token (SID) is in plain-text. This now matches the behavior of the official xivboot.exe and also XIVQuickLauncher. This will become the new default option in the next release.
  - Big thanks to XIVQuickLauncher where the code is based off of, as well as the information on xivdev.
- Custom wine prefix/executable options on Linux and macOS

These bugs are also fixed:

- Windows dependencies are now copied when building
- Windows "open game directory" button now works
- The built-in game wine is now the default (for real this time) on macOS

---


### 0.1.0

First public release!
