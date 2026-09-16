# scoreboard-firmware

Update channel for a hobby ESP32 sports scoreboard: a 4-inch screen that reads
public ESPN scoreboards directly and shows live scores, with no server of its
own.

This repository holds **compiled images only** - no source code, no
credentials, nothing about any particular home network. A screen checks
`latest.json` a few times a day and installs the image named there when its
version differs from the one it is running. It is public for one reason: a
private download would need a password stored inside every screen, and anyone
holding a screen could read it out.

- `latest.json` - the version currently offered, and where to fetch it
- `releases/` - the images themselves, one per version

A screen writes an update into its spare slot, so an interrupted download
leaves the working version in place. Recovery of last resort is a USB cable.
