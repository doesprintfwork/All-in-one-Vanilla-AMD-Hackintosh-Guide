---
description: Installing Clover by using the installer package.
---

# From macOS

## Part - 1

1. Open Terminal and run `pkgutil --expand [drag and drop the RecoveryHDMetaDmg.pkg in gibMacOS/macOS Downloads/publicrelease/xxx-xxxxx xx.xx.x macOS xxxx folder] Desktop/RecoveryFiles`By doing the above command, it will extract files from the recovery package and create a folder call RecoverFiles on desktop to save all extracted resources. 
2. Go inside the RecoverFiles folder, double click on RecoveryHDMetaDmg.dmg and the disk image should be mounted.
3. Go into the RecoveryHDMeta disk and copy BaseSystem.dmg to desktop.
4. Go to disk utility. Find your USB and format it to:  `Name: [whatever you want] Format: Mac OS Extended (Journaled)  Scheme: GUID Partition Map`
5. Now click Restore button in Disk Utility and choose Image...
6. Choose BaseSystem.dmg on desktop and press Restore.
7. This should take some time depending on your USB speed.

## Part - 2

1. Open the Clover installer
2. Install it to your USB with these settings \(choose Customize in the Installation Type\) `Clover for UEFI booting only Install Clover in the ESP UEFI Drivers:  - ApfsDriverLoader  - AptioMemoryFix  - HFSPlus (or VBoxHFS - 64) Install RC Scripts on target volume (or Install RC Scripts on other volumes)` More explanations [here](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/clover-setup).
3. Time to edit the config.plist located in EFI/EFI/CLOVER . You can go to [this page ](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/config.plist-basics)to know what you need to edit. \(Quick Tip: There is a sample config.plist at the bottom of each config explanation. You can download it and use it\) If you have downloaded the config.plist, you can use it to replace the original one. **AMD Users, please continue reading.**
4. Replace the original config.plist in EFI/EFI/CLOVER with the prepatched one \(mentioned [here](../get-started/untitled/amd-clover-config.plist.md)\).
5. You have finally made the installer! Woo-hoo! 🥳 

