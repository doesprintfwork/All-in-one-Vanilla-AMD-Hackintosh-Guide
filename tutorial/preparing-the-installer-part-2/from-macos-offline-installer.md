---
description: You need macOS for this.
---

# From macOS \(Offline Installer\)

1. Format your USB with these settings: `Name: USB Format: MacOS Extended Journaled Scheme: GUID Partition Map`
2. Right click on your macOS installer app \(mentioned [here](../get-started/prerequisites.md#things-need-to-get-if-you-are-making-the-installer-in-macos)\) and click `Show Contents Packages`.
3. Go to `Contents/Resources` and find `createinstallmedia` inside that folder.
4. Open Terminal.
5. Type `sudo [drag and drop createinstallmedia here] --volume /Volumes/USB` and enter.
6. Follow the instructions. Be patient as it will take a lot of time.
7. Go to this [page](../preparing-the-installer-part-3/install-and-configuring-clover-in-macos.md) after finishing this part.

![Step 1 \(Format your USB\)](../../.gitbook/assets/ezgif-4-8c9decf9eb06.gif)

![Steps 2 - 6 \(Restoring files to USB\)](../../.gitbook/assets/ezgif-4-cde07ffbd394.gif)

