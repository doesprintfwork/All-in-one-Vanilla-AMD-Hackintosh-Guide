---
description: We'll use MakeInstall in gibMacOS folder.
---

# From Windows

1. Now, run MakeInstall.bat inside the gibMacOS folder.
2. A Command Prompt window should pop up. Your USB should be listed. Enter the number in front of your usb USB and press Enter.
3. It will format your USB. After that, shift and right click and copy the path of the downloaded macOS package \(`gibMacOS/macOS Downloads/publicrelease/xxx-xxxxx - xx.xx.x macOS xxxx/RecoveryHDMetaDmg(or RecoveryHDUpdate)`

   \) to the cmd window and press enter.

4. It will start to extract the resources and restore them to your USB drive. This will take some time depending your USB speed. Be patient \(again\)!
5. After restoring the resources, the script will automatically install Clover \(boot-loader\) to your USB.
6. **AMD Users, skip this step.** By the time you are restoring the resources, go to this [site](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/config.plist-basics) and find the sample config file for your cpu architecture at the bottom of the config explanation. Download it.
7. Once finish, you should be able to see a new partition called `CLOVER` is mounted. Go into `CLOVER/EFI/CLOVER` . Replace the original one with the downloaded sample config.plist \(**AMD Users:** Use the one inside the Zen or 15H:16H folder\).
8. After that, put all kexts you have downloaded \(in [Gathering Kexts page](../get-started/untitled/gathering-kexts.md)\) to `CLOVER/EFI/CLOVER/kexts/Other` folder.

