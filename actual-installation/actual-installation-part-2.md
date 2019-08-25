# Actual Installation - Part 2

## Now you're ready to plug-n-play.

To start the installation:

1. Plug the Ethernet if you are using Network Installer.
2. Plug the USB.
3. Start the computer into the boot menu. \(Refer to the manual of your motherboard or google.\)
4. Select your USB device. \(Make sure it says UEFI or PX before it.\)
5. Select Boot macOS Recovery from ... \(or Boot macOS Install from OS X Base System, depends on the release chosen.\)
6. Wait for the wall of text to make you feel like a _hackerman._
   * Note: If it gets stuck with a Stop sign, reboot your computer. Boot with USB 2. When it gets to the Stop Sign screen🚫, hot-swap it to USB 3.
   * Note2: If you get a black screen at the end of the installer on Intel HD GPUs, reboot to Clover, Press `O` \(letter\), go to Graphics Injection, change FakeID to 0x12345678, go back and boot. You will have to do this on every reboot until you get to the desktop. The Graphics will be slow and sluggish, fix it asap. Use google then.
7. When you get to the Installer screen \(it may take several minutes for it to load\):
8. **Skip this step if you made an Offline Installer.** Open Utilities &gt; Network Utility. Check if there is a connection, if not, check your LAN cable, and your LAN drivers from above. Close it after you have finish checking.
9. Select Disk Utility, select View &gt; Show all Devices, select the drive to format, format it as: `Name:`  **`<Whatever you want>`** `Format:`**`APFS`** \(if you are installing macOS Mojave or installing macOS High Sierra to an SSD\)        ``**`MacOS Extended Journaled`** \(if you are installing macOS High Sierra to an HDD\) `Scheme:`**`GUID Partition Map`**
   * Note: if you want to multiboot, go [here](https://hackintosh-multiboot.gitbook.io/hackintosh-multiboot/) \[reminder\]
   * Note2: _**DATA == GONE, BYE**_
10. Click on Disk Utility on top &gt; Quit Disk Utility.
11. Select Reinstall macOS or Install macOS.
12. _**YES, YOU AGREE.**_
13. Select your disk.
14. Let it install. \(For the Network Installer, the faster the internet the better. For the Offline Installer, the faster the USB the better.\)

After that, it will reboot for the second stage of the install, boot clover, it should now autoselect `Boot Install macOS from <your disk name>`. If not, select it on your own and boot it up, let it finish.

