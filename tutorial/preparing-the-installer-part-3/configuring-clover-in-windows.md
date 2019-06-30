# Configuring Clover in Windows

## Part 1 - Config and Kexts

1. Once finished, you should be able to see a new partition called `CLOVER` is mounted. Go into `CLOVER/EFI/CLOVER`. Replace the original one with the config.plist you've made.
2. After that, put all the kexts you have downloaded \(in [Gathering Kexts page](../get-started/gathering-kexts.md)\) to `CLOVER/EFI/CLOVER/kexts/Other` folder. **Skip all of the SMC kexts** \(except VirtualSMC and FakeSMC\) as they might cause Kernel Panic\(s\).
3. And delete the FakeSMC.kext. \(if you are using VirtualSMC.kext\)

![Config and Kexts](../../.gitbook/assets/ezgif-4-106771fe2b5a.gif)

## Part 2 - Drivers

### For UEFI:

1. Go back to `CLOVER/EFI/CLOVER` and go to the drivers64UEFI folder.
2. Delete everything **except** ApfsDriverLoader-64.efi.
3. Go back to `CLOVER/EFI/CLOVER` and go to `Drivers-off/drivers64UEFI` folder.
4. Copy `HFSPlus.efi`and `AptioMemoryFix-64.efi` to `CLOVER/EFI/CLOVER/drivers64UEFI`.
5. Yay! You are ready to [install macOS](../actual-installation-part-1.md)! 🥳 

![Drivers - UEFI](../../.gitbook/assets/ezgif-4-dcd1cd3e8f07.gif)

### WIP ~~For Legacy\(BIOS\):~~

Still not finished.

