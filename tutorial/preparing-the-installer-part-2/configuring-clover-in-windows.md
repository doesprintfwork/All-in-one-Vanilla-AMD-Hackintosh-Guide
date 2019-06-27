# Configuring Clover in Windows

1. Once finished, you should be able to see a new partition called `CLOVER` is mounted. Go into `CLOVER/EFI/CLOVER`. Replace the original one with the config.plist you've made.
2. After that, put all the kexts you have downloaded \(in [Gathering Kexts page](../get-started/gathering-kexts.md)\) to `CLOVER/EFI/CLOVER/kexts/Other` folder.
3. Go back to `CLOVER/EFI/CLOVER` and go to the drivers64UEFI folder.
4. Delete everything except ApfsDriverLoader-64.efi.
5. Go back to `CLOVER/EFI/CLOVER` and go to `Drivers-off/drivers64UEFI` folder.
6. Copy `HFSPlus.efi`and `AptioMemoryFix-64.efi` to `CLOVER/EFI/CLOVER/drivers64UEFI`.
7. Yay! You are ready to [install macOS](../actual-installation-part-1.md)! 🥳 

![Steps 1 - 2 \(Copying kexts and config.plist\)](../../.gitbook/assets/ezgif-4-106771fe2b5a.gif)

![Steps 3 - 6 \(Copying drivers for Clover\)](../../.gitbook/assets/ezgif-4-dcd1cd3e8f07.gif)

