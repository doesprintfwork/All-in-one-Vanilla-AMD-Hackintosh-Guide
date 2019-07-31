# Install and Configuring Clover in macOS

1. Open the Clover installer.
2. Install it to your USB with these settings. \(Choose Customize in `Installation Type` part\) **UEFI:** `Clover for UEFI booting only Install Clover in the ESP UEFI Drivers:  - ApfsDriverLoader  - AptioMemoryFix (If you have)  - VBoxHFS (or HFSPlus) Install RC Scripts on target volume (or Install RC Scripts on other volumes)` More explanations [here](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/clover-setup).
3. **If you do not have AptioMemoryFix, download the latest release from** [**this repo**](https://github.com/acidanthera/AptioFixPkg/releases)**.  If you do not have ApfsDriverLoader, download the latest release from** [**this repo**](https://github.com/acidanthera/AppleSupportPkg/releases)**.**  You will find them \(they are files that end with .efi\) in the Release folder from the downloaded zip. You need to put them inside `EFI/EFI/CLOVER/drivers/UEFI` folder.
4. When it is finished, a disk call EFI should be mounted. Replace the original config.plist in EFI/EFI/CLOVER with the config.plist you've made.
5. After that, put all the kexts you have downloaded \(in [Gathering Kexts page](../../prerequisites/get-started/gathering-kexts.md)\) to `EFI/EFI/CLOVER/kexts/Other` folder.
6. You have finally made the installer! You can proceed to the [next part](../../actual-installation/actual-installation-part-1.md)! Yay! 🥳 

![Steps 1 - 2 \(Installing Clover\)](../../.gitbook/assets/installing-clover.gif)

![Steps 3 - 4 \(Copy files to Clover\)](../../.gitbook/assets/ezgif-4-7eed77270d16.gif)

