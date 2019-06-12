# Actual Installation - Part 2

## Now you're ready to plug-n-play.

To start the installation:

1. Plug the Ethernet
2. Plug the USB
3. Start the computer into the boot menu \(refer to your motherboards manual or google\)
4. Select your USB device \(make sure it says UEFI or PX before it, some motherboards with only legacy may not find UEFI, it's fine, tho I'm not supporting Legacy booting atm\).
5. Select Boot macOS Recovery from ... \(or Boot macOS Install from OS X Base System, this changes depends on the release chosen\)
6. Wait for the wall of text to make you feel like a _hackerman_
   * Note: if it gets stuck with a Stop sign, change your USB drive's port, use a USB2.0 drive, or use a USB2.0 extension cord.
   * Note2: if you get a black screen at then end of the installer on Intel HD GPUs, reboot to Clover, Press `O` \(letter\), go to Graphics Injection, change FakeID to 0x12345678, go back and boot. You will have to do this on every reboot until you get to the desktop. The Graphics will be slow and sluggish, fix it asap. Use google then.
7. When you get to the Installer screen \(it may take several minutes for it to load\), open Utilities &gt; Network Utility. Check if there is a connection, if not, check your LAN cable, and your LAN drivers from above.
8. Go back, select Disk Utility, select the drive to format, nuke it as MacOS Extended Journaled, name it something and go back.
   * Note: if you want to multiboot, go [here](https://github.com/midi1996/JBOG/blob/master/Multiboot.md) \[reminder\]
   * Note2: _**DATA == GONE, BYE**_
9. Click on Disk Utility on top &gt; Quit Disk Utility.
10. Select Reinstall macOS
11. _**YES YOU AGREE**_
12. Select your disk
13. Let it install \(the faster the internet the better\).

After that, it will reboot for the second stage of the install, boot clover, it should now autoselect Boot `Install macOS from <your hdd name>`, if not, then select it on your own and boot it up, let it finish.

