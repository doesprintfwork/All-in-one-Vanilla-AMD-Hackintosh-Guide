# Gathering Kexts

## What Kexts Do You Need?

### **What is absolutely required?**

[_VirtualSMC.kext_](https://github.com/acidanthera/VirtualSMC) _\(use this\)_ or [FakeSMC.kext](https://github.com/RehabMan/OS-X-FakeSMC-kozlek) \(older, if VirtualSMC doesn't work, use this instead\) is as aforementioned essential. This kext is what tells macOS "Yes this is a real Mac", emulating the functionality of the SMC on real Mac's. Without it, no Hackintosh.

### Where can I find these kexts?

All the kexts shown here are available for download on the [_**kext repo**_](https://1drv.ms/f/s!AiP7m5LaOED-m-J8-MLJGnOgAqnjGw) _****_provided and maintained by Goldfish64. All these kexts are automatically built when a new kext update is committed. All Hyperlinks \(except SmallTree kext\) are links to their GitHub. **Remeber to download the built version on the** [_**kext repo**_**.**](https://1drv.ms/f/s!AiP7m5LaOED-m-J8-MLJGnOgAqnjGw) **Do** _**NOT**_ **download and use all kexts. Doing this may result a kernel panic.**

### Ethernet \(Choose the one you need\)

* _​_[_IntelMausiEthernet.kext_](https://github.com/Mieze/IntelMausiEthernet) - this works with most newer Intel LAN chipsets
* [_AppleIntelE1000e.kext_](https://sourceforge.net/projects/osx86drivers/) - this works with older Intel LAN chipsets - but can cause kernel panics on newer chipsets
* _​_[_AtherosE2200Ethernet.kext_](https://github.com/Mieze/AtherosE2200Ethernet) - this works for most Atheros or Killer networking chipsets
* _​_[_RealtekRTL8111.kext_](https://github.com/Mieze/RTL8111_driver_for_OS_X) - this works with most gigabit Realtek LAN chipsets
* _​_[_RealtekRTL8100.kext_](https://github.com/Mieze/RealtekRTL8100) - for 10/100 Realtek LAN chipsets
* \*\*\*\*[**SmallTree-Intel-211-AT-PCIe-GBE.kext**](https://cdn.discordapp.com/attachments/390417931659378688/556912824228773888/SmallTree-Intel-211-AT-PCIe-GBE.kext.zip) - for Intel I122-AT LAN chipset only. \(Download this by clicking the bold blue words.\)

### Graphics \(You'll need all of these\)

* [_Whatevergreen.kext_ ](https://github.com/acidanthera/WhateverGreen)_-_ this kext fixes a lot of GPU related issues.
* [_Lilu.kext_](https://github.com/acidanthera/Lilu) _-_ this kext acts as a loader for other kexts. More specifically it can patch kexts, processes and libraries.

### WiFi and Bluetooth 

\(I myself don't use bluetooth nor WiFi so I don't have knowledge in that, but here is some information on the subject by CorpNewt.\) 

`Apple is pretty minimal with their WiFi support, so I'll only cover the two main chipsets I'm familiar with. I've used a BCM94360CD + PCIe adapter, and BCM94352HMB/BCM94352Z in my Hackintoshes. The BCM94360CD worked OOB with no extras as it's a native card. For the BCM94352 flavors, I've been using` [_`AirportBrcmFixup.kext`_](https://github.com/acidanthera/AirportBrcmFixup)`and the companion`[_`Lilu.kext`_](https://github.com/vit9696/Lilu/releases)`for WiFi setup and` _`BrcmBluetoothInjector.kext`_`(on 10.13.6+) or` _`BrcmPatchRAM2.kext`_ `alongside` _`BrcmFirmwareData.kext`_ `- all of the Brcm* kexts are from RehabMan's` [_`OS-X-BrcmPatchRAM`_](https://github.com/RehabMan/OS-X-BrcmPatchRAM)`repo.`

### Audio

* [_AppleALC.kext_](https://github.com/acidanthera/AppleALC) _-_ this kext supports most of the commonly used codecs, with the best quality. Intel CPUs and Ryzen CPUs are supported. **No FX support!**
* \*\*\*\*[_VoodooHDA.kext_ ](https://sourceforge.net/projects/voodoohda/)_-_ a jack of all trades master of none solution to audio. **Required on FX.**

