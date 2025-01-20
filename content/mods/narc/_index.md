---
title: "Neo Armor Refit Collection"
layout: "single"
---

Are you annoyed that some armor somehow changes your female character's chest? Try NARC!

![Comparison shot](comparison.jpg)

It works around weight painting issues in certain chest pieces by over-scaling the chest bones. Yes it's a giant hack but it works without modifying the gear models themselves. This is accomplished via my plugin [Refitter]({{< ref "refitter" >}}).

## Instructions

1. Download and install the [Refitter plugin]({{< ref "refitter" >}}).
2. Open the Refitter configuration window by typing "/refitter" in chat, or by using the Dalamud Plugin Installer window.
3. Click the "Download" button below. Once the file is downloaded, copy the _text data_ to your clipboard - not the file itself.
4. Back in the Refitter config window: Under the "Data" tab, click the "Import to Clipboard" button.
5. You're all done! 

## Downloads

{{< begin-grid >}}
{{< blurb title="Download Configuration" description="Download the NARC configuration." url="https://xiv.zone/distrib/narc/config.json" >}}
{{< blurb title="Download Penumbra Mod" description="Download the Penumbra mod (optional) to fix clipping with some armor." url="https://xiv.zone/distrib/narc/narc-penumbra.zip" >}}
{{< end-grid >}}

## Caveats

This mod is still a work-in-progress. Here's some things to note:

* There's no way to tell which version of NARC you have installed yet. If you notice some armor is missing refits, try re-importing.

## Frequently Asked Questions

### How is this different than VARC?

[VARC](/mods/varc) does the same thing, but through manually fixing the weight painting on the gear model themselves. While this works (assuming I fixed it, and not making it worse) it's very time consuming.

A secondary and less important reason is to prevent breakages during game updates. Previously, VARC depended on Penumbra to update first. And now with the graphical update ongoing, gear models could be changed from underneath us!

Refitter is much simpler to update in comparison, and NARC needs no updates itself unless any gear's weight painting changes.

### Can I selectively apply this to certain characters?

I have no plans to build that feature into Refitter at the moment.

### What is the difference between Refitter and NARC?

Refitter is the Dalamud plugin I created to modify the chest bones, it technically has nothing to do with NARC. NARC is just a configuration file for it I've been tweaking.

### Can I create my own refits or modify yours?

Yes! Refitter includes a live, in-game system to do this. You also have the option of exporting your configuration which can easily be shared online.

### Why did you make another stupid, useless mod??

I don't care what you think :)
