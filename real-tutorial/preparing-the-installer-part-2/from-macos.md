---
description: Installing Clover by using the installer package.
---

# From macOS \(Online Method\)

### You'll need ethernet connection while installing macOS. If you don't have a ethernet connection, go to the next page for offline installation.

## Part - 1

1. Rename the downloaded `RecoveryHDMetaDMG.pkg (or RecoveryHDUpdate.pkg)` to `RecoveryHDMetaDMG.dmg (or RecoveryHDUpdate.dmg)`
2. Double click on it and a new disk call RecoveryHDMeta \(or RecoveryHDUpdate\) should be mounted
3. Go into the RecoveryHDMeta \(or RecoveryHDUpdate\) disk and copy BaseSystem.dmg to desktop.
4. Go to disk utility. Click **View &gt; Show all devices** and find your USB **\(whole disk instead of a partition, check out the gif below to know what I am talking\)** and format it to:  `Name:   [whatever you want] Format: Mac OS Extended (Journaled)  Scheme: GUID Partition Map`
5. Now, choose your **USB partition** click Restore button in Disk Utility and choose Image...
6. Choose BaseSystem.dmg on desktop and press Restore.
7. This should take some time depending on your USB speed.

![Steps 4 - 7 \(Restoring the resources to USB\)](../../.gitbook/assets/restoring-to-usb.gif)

## Part - 2

1. Open the Clover installer.
2. Install it to your USB with these settings. \(Choose Customize in `Installation Type` part, **only choose either UEFI or Legacy**\) **UEFI \(For newer Mobo\):** `Clover for UEFI booting only Install Clover in the ESP UEFI Drivers:  - ApfsDriverLoader  - AptioMemoryFix  - HFSPlus (or VBoxHFS - 64) Install RC Scripts on target volume (or Install RC Scripts on other volumes)` **Legacy \(For older Mobo\):** `Install Clover in ESP Boot0ss Clover EFI Sata Drivers64: - UsbMouseDxe - UsbKbDxe - Ps2MouseDxe - XhciDxe Install Rc Scripts on target volume (or Install RC Scripts on other volumes)` More explanations [here](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/clover-setup).
3. When it is finished, a disk call EFI should be mounted. Replace the original config.plist in EFI/EFI/CLOVER with the downloaded sample config \(**or the pre-patched one for AMD Users** which mentioned [here](../get-started/untitled/amd-clover-config.plist.md)\).
4. After that, put all the kexts you have downloaded \(in [Gathering Kexts page](../get-started/untitled/gathering-kexts.md)\) to `EFI/EFI/CLOVER/kexts/Other` folder.
5. You have finally made the installer! Woo-hoo! 🥳 

![Steps 1 - 2 \(Installing Clover\)](../../.gitbook/assets/installing-clover.gif)

![Step 3](../../.gitbook/assets/copying-config.gif)

