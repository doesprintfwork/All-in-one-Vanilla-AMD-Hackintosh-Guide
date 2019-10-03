---
description: We are going to restore files to your USB.
---

# From Windows

## Phase 1 -- Restore Files to your USB

1. Plug in your USB if you haven't plug it in yet
2. Run MakeInstall.bat in gibMacOS
3. A Command Prompt window should pop up. Your USB should be listed. Enter the number in front of your USB and press Enter
4. It will format your USB. After that, shift + right click and copy the path of the downloaded macOS **Recovery** package `gibMacOS/macOS Downloads/publicrelease/xxx-xxxxx - xx.xx.x macOS xxxx/RecoveryHDMetaDmg.pkg`

    to the cmd window and press enter

5. It will start to extract the resources and restore them to your USB drive. This will take some time depending your USB speed. Be patient \(again\)! The script will automatically install Clover \(boot-loader\) to your USB after restoring the files

![](../../.gitbook/assets/ezgif-4-8fa1279bb84c.gif)

## Phase 2 -- Extend the Volume and Convert to Full Installer

1. Open Paragon Disk Manager
2. Go to Partition Manager
3. Choose the second partition of your USB and choose Resize Partition
4. Set Space after partition to 0 and press OK
5. Press Apply
6. Close it and run TransMac as Administrator
7. Click on your USB and go to `macOS Base System (or OS X Base System)/Install macOS xxx.app/Contents`
8. Drag and drop the prepared SharedSupport folder here
9. Done! Proceed to the [next part](../../clover-installtion/usb-clover/usb-clover-win.md)!

![Steps 1 - 5](../../.gitbook/assets/ezgif-4-3f1d85748df0.gif)

![Steps 6 - 8](../../.gitbook/assets/2019-06-16-22-29-_2.gif)

