---
description: Installing Clover by using the installer package.
---

# From macOS \(Network Installer\)

#### You'll need an ethernet connection while installing macOS with this method. For people who don't have an ethernet connection, go to [this page](from-macos-offline-installer.md).

## Part - 1

1. Rename the downloaded `RecoveryHDMetaDMG.pkg (or RecoveryHDUpdate.pkg)` to `RecoveryHDMetaDMG.dmg (or RecoveryHDUpdate.dmg)`
2. Double click on it and a new disk call RecoveryHDMeta \(or RecoveryHDUpdate\) should be mounted
3. Go into the RecoveryHDMeta \(or RecoveryHDUpdate\) disk and copy BaseSystem.dmg to desktop.
4. Go to disk utility. Click **View &gt; Show all devices** and find your USB **\(the whole disk instead of a partition, check out the gif below to know what I am talking\)** and format it to:  `Name:   [whatever you want] Format: Mac OS Extended (Journaled)  Scheme: GUID Partition Map`
5. Now, choose your **USB partition** click Restore button in Disk Utility and choose Image...
6. Choose BaseSystem.dmg on desktop and press Restore.
7. This should take some time depending on your USB speed.

![Steps 1 - 3 \(Extracting BaseSystem.dmg to Desktop\)](../../.gitbook/assets/ezgif-4-c4f2b894d040.gif)

![Steps 4 - 7 \(Restoring the resources to USB\)](../../.gitbook/assets/restoring-to-usb.gif)

## Part - 2

1. Open the Clover installer.
2. Install it to your USB with these settings. \(Choose Customize in `Installation Type` part, select settings depends on your Mobo.\) **UEFI \(For newer Mobo\):** `Clover for UEFI booting only Install Clover in the ESP UEFI Drivers:  - ApfsDriverLoader  - AptioMemoryFix  - HFSPlus (or VBoxHFS - 64) Install RC Scripts on target volume (or Install RC Scripts on other volumes)` **Legacy \(For older Mobo\):** `Install Clover in ESP Boot0ss Clover EFI Sata Drivers64: - UsbMouseDxe - UsbKbDxe - Ps2MouseDxe - XhciDxe Install Rc Scripts on target volume (or Install RC Scripts on other volumes)` More explanations [here](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/clover-setup).
3. When it is finished, a disk call EFI should be mounted. Replace the original config.plist in EFI/EFI/CLOVER with the config.plist you've made.
4. After that, put all the kexts you have downloaded \(in [Gathering Kexts page](../get-started/gathering-kexts.md)\) to `EFI/EFI/CLOVER/kexts/Other` folder.
5. You have finally made the installer! You can proceed to the [next part](../actual-installation-part-1.md)! Woo-hoo! 🥳 

![Steps 1 - 2 \(Installing Clover\)](../../.gitbook/assets/installing-clover.gif)

![Steps 3 - 4 \(Copy files to Clover\)](../../.gitbook/assets/ezgif-4-7eed77270d16.gif)

