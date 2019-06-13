# Posty!!!

## Clover Installation

Basically, Install Clover again with the settings which you have chosen for your USB. Then, mount the EFI partitions of your USB and your hard disk which has installed macOS. Open both EFI partitions and replace the original EFI files in the hard disk with your USB files. \(Tips: hold down the `option` key to copy files and the merge option should appear.

## Others

I don't want to write anything more. [This page](https://internet-install.gitbook.io/macos-internet-install/posty-posty...) from Midi's guide contains all post install guide for Intel.

Here\(Link is down\) is another link for Post-Installation on AMD.

### For Ryzen

#### Audio Solution

* AppleALC. [Here is the link](https://forum.amd-osx.com/viewtopic.php?f=24&t=6043&p=45449#p45449).

#### Fixing multiple monitors setup

1. Open Clover Configurator.
2. Go to Mount EFI tab in the side bar.
3. Find your macOS disk in the EFI partition part and click Mount Partition. You may need password.
4. After you have mounted the disk, open it and 
5. Disable CSM Support in BIOS

