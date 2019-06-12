---
description: You need macOS for this.
---

# From macOS \(Offline Installer\)

1. Format your usb with these settings: `Name: USB Format: MacOS Extended Journaled Scheme: GUID Partition Map`
2. Right click on your macOS installer app \(mentioned [here](../get-started/untitled/#things-need-to-get-if-you-are-making-the-installer-in-macos)\) and click `Show Contents Packages`.
3. Go to `Contents/Resources` and find `createinstallmedia` inside that folder.
4. Open Terminal.
5. Type `sudo [drag and drop createinstallmedia here] --volume /Volumes/USB` and enter.
6. Follow the instructions. Be patient as it will take a lot time.
7. When it finished, you can now [install Clover Bootloader to your USB](from-macos.md#part-2).

