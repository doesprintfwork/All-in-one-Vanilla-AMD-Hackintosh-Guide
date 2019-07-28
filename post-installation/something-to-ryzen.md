# Something to Ryzen

## First thing first

Ok, so you have your working Hackintosh, right? If you see a lot of performance lose, that's normal because the kernel patches causes it. \(I don't know why, better asks an expert in AMD-OSX Forum or Discord Server\) Most of the cases are using Zen cpus.

**Here is a little fix for it: Change your patches from 17H to 15H\_16H**

{% hint style="danger" %}
But you may have some audio and video desync problem so decide it by your own
{% endhint %}

## How to do it?

1. Open your config.plist and make a copy of it
2. Rename the copy to config\_15h.plist \(or whatever name you want started with config\_ and ends with .plist\)
3. Open config\_15h.plist with clover configurator
4. Go to Kernel and Kext Patches and go to KernelToPatch
5. Delete all of the patches by pressing the Minus button➖
6. Save and quit
7. Download this [repo](https://github.com/corpnewt/AMDVanillaPatches)
8. Right-click open AMDVanillaPatches.command
9. A terminal window should pop up. You should see CPU Type there. The default should be FX. If it is not FX, enter 1, press enter, enter 1 and press enter. Now it should be in FX
10. Now enter 2 and press enter. It will automatically update the patches.plist file
11. After it finishes, enter 3, press enter, drag and drop your config\_15h.plist to the terminal window and press enter
12. Enter 4 and press enter
13. If there aren't any error, excellent!
14. Reboot
15. When it boots to Clover, choose Options &gt; Configs &gt; config\_15h \(or whatever the name is\) and return
16. Boot now and see if it works
17. If it works, you can now delete the original config.plist and rename the config\_15h.plist to config.plist
18. Profit!



