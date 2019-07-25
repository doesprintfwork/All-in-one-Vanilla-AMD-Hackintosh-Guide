# Configuring Clover in Windows

## Part 1 - Config and Kexts

1. Once finished, you should be able to see a new partition called `CLOVER` is mounted. Open it and go into `EFI/CLOVER`. Replace the original one with the config.plist you've made.
2. After that, put all the kexts you have downloaded \(in [Gathering Kexts page](../../prerequisites/get-started/gathering-kexts.md)\) to `EFI/CLOVER/kexts/Other` folder. **Skip all of the SMC kexts** \(except VirtualSMC.kext and FakeSMC.kext\) as they might cause Kernel Panic\(s\).
3. And delete the FakeSMC.kext. \(if you are using VirtualSMC.kext\)

![Config and Kexts](../../.gitbook/assets/ezgif-4-106771fe2b5a.gif)

## Part 2 - Drivers

### For Clover version older than r4988 \(not including r4988\):

#### For UEFI:

1. Go back to `EFI/CLOVER` and go to the drivers64UEFI folder.
2. Delete everything **except** `ApfsDriverLoader-64.efi` and `VBoxHFS.efi`.
3. Go back to `EFI/CLOVER` and go to `drivers-off/drivers64UEFI` folder.
4. Copy `OsxAptioFix3Drv.efi` to `EFI/CLOVER/drivers64UEFI`.
5. Yay! You are ready to [install macOS](../../actual-installation/actual-installation-part-1.md)!

### For Clover version newer than r4988 \(including r4988\):

#### For UEFI:

1. Go back to `EFI/CLOVER` and go into `drivers/UEFI`
2. Delete everything except: - `ApfsDriverLoader.efi` - `OsxAptioFix3Drv.efi` - `VBoxHFS.efi`
3. Yay! You are ready to [install macOS](../../actual-installation/actual-installation-part-1.md)! 🥳 

### If you don't know your Clover version:

* If you already have made an installer before and you are trying to configure Clover with my guide, check your directory structure. If it has the same structure as below, your Clover version should be older than r4988.

  ```text
  EFI
    ├ BOOT
    | └ BOOTX64.efi
    └ CLOVER
      ├ doc
      | └ <some files here>
      ├ drivers-Off
      | └ <some folders here>
      ├ drivers64
      | └ <some files here>
      ├ drivers64UEFI
      | └ <some files here>
      ├ kexts
      | └ <some folders here>
      ├ themes
      | └ <some folders here>
      ├ tools
      | └ <some files here>
      ├ CLOVERX64.efi
      └ config.plist 
  ```

* Else, your Clover version should be r4988 or higher.

