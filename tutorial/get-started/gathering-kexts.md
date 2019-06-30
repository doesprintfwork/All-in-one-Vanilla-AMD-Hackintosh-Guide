# Gathering Kexts

### Please keep all of the downloaded kexts to a folder. We will need that later.

## What Kexts Do You Need?

### Where can I find these kexts?

All the kexts shown here are available for download on the [_**kext repo**_](https://1drv.ms/f/s!AiP7m5LaOED-m-J8-MLJGnOgAqnjGw) _****_provided and maintained by Goldfish64. **Do** _**NOT**_ **download and use all of the kexts listed below. Doing this may result a kernel panic.**

### **What is absolutely required?**

[_VirtualSMC.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455091&cid=FE4038DA929BFB23) _\(use this\)_ or [FakeSMC.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455161&cid=FE4038DA929BFB23) \(older, if VirtualSMC doesn't work, use this instead\) is as aforementioned essential. This kext is what tells macOS "Yes this is a real Mac", emulating the functionality of the SMC on real Mac's. Without it, no Hackintosh. **Do NOT use both of the SMC kexts.**

**You'll need these also.**

* [_Lilu.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455053&cid=FE4038DA929BFB23) _-_ this kext acts as a loader for other kexts. More specifically it can patch kexts, processes and libraries.
* [_Whatevergreen.kext_ ](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455095&cid=FE4038DA929BFB23)_-_ this kext fixes a lot of GPU related issues.

### Ethernet \(Choose the one you need\)

* _​_[_IntelMausiEthernet.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455134&cid=FE4038DA929BFB23) - this works with most newer Intel LAN chipsets **except I122-AT.**
* [_AppleIntelE1000e.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455998&cid=FE4038DA929BFB23) - this works with older Intel LAN chipsets - but can cause kernel panics on newer chipsets
* _​_[_AtherosE2200Ethernet.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455105&cid=FE4038DA929BFB23) - this works for most Atheros or Killer networking chipsets
* _​_[_RealtekRTL8111.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455143&cid=FE4038DA929BFB23) - this works with most gigabit Realtek LAN chipsets
* _​_[_RealtekRTL8100.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455140&cid=FE4038DA929BFB23) - for 10/100 Realtek LAN chipsets
* \*\*\*\*[_SmallTree-Intel-211-AT-PCIe-GBE.kext_](https://cdn.discordapp.com/attachments/390417931659378688/556912824228773888/SmallTree-Intel-211-AT-PCIe-GBE.kext.zip) - **for Intel I122-AT LAN chipset** only.

### USB Tethering

* \_\_[_HoRNDIS.kext_](https://github.com/midi1996/JBOG/blob/master/Extra/HoRNDIS.kext.zip?raw=true) - For USB tethering from Android **only**.

### WiFi and Bluetooth 

\(I myself don't use bluetooth nor WiFi so I don't have knowledge in that, but here is some information on the subject by CorpNewt.\) 

> Apple is pretty minimal with their WiFi support, so I'll only cover the two main chipsets I'm familiar with. I've used a BCM94360CD + PCIe adapter, and BCM94352HMB/BCM94352Z in my Hackintoshes. The BCM94360CD worked OOB with no extras as it's a native card. For the BCM94352 flavors, I've been using [_AirportBrcmFixup.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455063&cid=FE4038DA929BFB23) __and the companion [_Lilu.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455053&cid=FE4038DA929BFB23) __for WiFi setup and _BrcmBluetoothInjector.kext_ \(on 10.13.6+\) or_BrcmPatchRAM2.kext_ alongside _BrcmFirmwareData.kext_ - all of the Brcm\* kexts are from RehabMan's [_OS-X-BrcmPatchRAM_](https://github.com/RehabMan/OS-X-BrcmPatchRAM) __repo.

### Audio \(Do not get both\)

* [_AppleALC.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455056&cid=FE4038DA929BFB23) _-_ this kext supports most of the commonly used codecs, with the best quality. Intel CPUs and Ryzen CPUs are supported. **No FX support! Also, 3.5mm microphones are broken on Ryzen.**
* \*\*\*\*[_VoodooHDA.kext_ ](https://sourceforge.net/projects/voodoohda/)_-_ a jack of all trades master of none solution to audio. **Required on FX. Mic support on Ryzen.**

### **Misc \(**_**MUST GET THIS**_ **if you are using AMD or Pentium chips\)**

* [NullCPUPowerManagement.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455158&cid=FE4038DA929BFB23) **- This kext disables CPU power management,** _**as that is not supported on AMD and Pentium chips.**_

## **Source Code Links**

* [VirtualSMC](https://github.com/acidanthera/VirtualSMC)
* [FakeSMC](https://github.com/RehabMan/OS-X-FakeSMC-kozlek)
* [Lilu](https://github.com/acidanthera/Lilu)
* [WhateverGreen](https://github.com/acidanthera/WhateverGreen)
* [IntelMausiEthernet](https://github.com/Mieze/IntelMausiEthernet)
* [AppleIntelE1000e](https://github.com/chris1111/AppleIntelE1000e)
* [AtherosE2200Ethernet](https://github.com/Mieze/AtherosE2200Ethernet)
* [RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X)
* [RealtekRTL8100](https://github.com/Mieze/RealtekRTL8100)
* [AirportBrcmFixup](https://github.com/acidanthera/AirportBrcmFixup)
* [AppleALC](https://github.com/acidanthera/AppleALC)
* [NullCPUPowerManagement](https://github.com/corpnewt/NullCPUPowerManagement)
* [VoodooHDA](https://sourceforge.net/p/voodoohda/code/HEAD/tree/)

