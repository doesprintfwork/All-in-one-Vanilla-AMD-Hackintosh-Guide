# Install and Configuring Clover in macOS

1. Open the Clover installer.
2. Install it to your USB with these settings. \(Choose Customize in `Installation Type` part, select settings depends on your Mobo.\) **UEFI \(For newer Mobo\):** `Clover for UEFI booting only Install Clover in the ESP UEFI Drivers:  - ApfsDriverLoader  - AptioMemoryFix  - HFSPlus (or VBoxHFS - 64) Install RC Scripts on target volume (or Install RC Scripts on other volumes)` **Legacy \(For older Mobo\):** `Install Clover in ESP Boot0ss Clover EFI Sata Drivers64: - UsbMouseDxe - UsbKbDxe - Ps2MouseDxe - XhciDxe Install Rc Scripts on target volume (or Install RC Scripts on other volumes)` More explanations [here](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/clover-setup).
3. When it is finished, a disk call EFI should be mounted. Replace the original config.plist in EFI/EFI/CLOVER with the config.plist you've made.
4. After that, put all the kexts you have downloaded \(in [Gathering Kexts page](../get-started/gathering-kexts.md)\) to `EFI/EFI/CLOVER/kexts/Other` folder.
5. You have finally made the installer! You can proceed to the [next part](../actual-installation-part-1.md)! Woo-hoo! 🥳 

![Steps 1 - 2 \(Installing Clover\)](../../.gitbook/assets/installing-clover.gif)

![Steps 3 - 4 \(Copy files to Clover\)](../../.gitbook/assets/ezgif-4-7eed77270d16.gif)

