---
description: Post installation
---

# Posty!!!

## General

### Clover Installation

We'll need to install Clover to your hard disk. Without that, you won't be able to boot to macOS.

1. Download Clover Install Package.
2. Right-click and press Open.
3. Keep pressing `Continue` until you get to Installation Type.
4. Press `Change Install Location..`.
5. Choose the hard disk you have your macOS installed and press `Continue`.
6. Press `Customize` and Choose these settings:

   `Clover for UEFI booting only  
   Install Clover in the ESP  
   UEFI Drivers:  
    - ApfsDriverLoader  
    - OsxAptioFix3Drv  
    - VBoxHFS (or HFSPlus)  
   Install RC Scripts on target volume (or Install RC Scripts on other volumes)`

7. Press Install.
8. When it finish, a partition call EFI should be mounted.
9. Mount your USB EFI partition.
10. Copy the kexts and config to your EFI partition \(like what you do before\)
11. Done.

## Intel

[This page](https://internet-install.gitbook.io/macos-internet-install/posty-posty...) from Midi's guide contains all post install guide for Intel.

## AMD

Here \(link broken\) is another link for Post-Installation on AMD. \(If audio isn't working, delete AppleALC.kext and put [VoodooHDA.kext](https://sourceforge.net/projects/voodoohda/) in `kexts/Other` folder\)

