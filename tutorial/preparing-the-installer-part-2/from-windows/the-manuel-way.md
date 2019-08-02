# The Manual Way

## Preparation

Download [Boot Disk Utility](http://cvad-mac.narod.ru/index/bootdiskutility_exe/0-5)

## Let's get started

1. Open your gibMacOS folder and go into `macOS Downloads/publicrelease/blahblahblah`
2. You should see a file that ends with .pkg. Copy it to your Desktop
3. Open it with 7-zip
4. Open `RecoveryHDMetaDmg.dmg` and copy BaseSystem.dmg to your Desktop
5. Open Boot Disk Utility
6. Go to Options &gt; Configuration and press the Check Now button
7. After the blue words appear, press OK
8. Plug in your USB and choose your USB
9. Press Format. This will take a while, be patient
10. When it says All Done, go to Tools &gt; Extract HFS \(HFS+\) partition from DMG-files
11. Choose the BaseSystem.dmg on your desktop and press Open
12. Choose Desktop as the destination and press OK
13. A CMD window should pop up and it will be closed when it finished, this shouldn't take so long
14. When it is closed, press the plus button in front of your USB in Boot Disk Uitlity and choose Part 2
15. Press Restore and choose the extracted 4.hfs and press Open
16. Boot Disk Utility will start restoring files to your USB. Be patient
17. If there isn't any error, done! You can go to the [next part](../../../clover-installtion/preparing-the-installer-part-3/configuring-clover-in-windows.md)!

