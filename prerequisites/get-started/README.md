# Get Started


!> <big>_**Please READ everything CAREFULLY!**_</big>

---

# General Prerequisites

### General

* An 8GB+ USB flash drive for the installer
* Kexts for your system \([Gathering Kexts](gathering-kexts.md)\)
* A clone of [gibMacOS](https://github.com/corpnewt/gibMacOS)
* [PYTHON 3](https://www.python.org/downloads/)

### The config file for Clover:

* **PLEASE READ THE PLIST BASICS OVER** [HERE](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/config.plist-basics) **AND MAKE YOUR OWN config.plist with Clover Configurator** \(On macOS\)**,** [Clover Cloud Editor](http://cloudclovereditor.altervista.org/cce/index.php) \(On Windows\) **or ProperTree config editor** \(Cross Platform Plist Editor, but difficult for people without any basis at programming\)**.**
  * _**DO NOT GET THE SAMPLE CONFIG.**_
* **After reading the plist basics guide, go to** [this page](../amd-clover-config.plist/) **to make your own config.plist**.
* [AptioMemoryFix.efi](https://cdn.discordapp.com/attachments/251043252046659586/609234258732515329/AptioFix-R27-RELEASE.zip) **\(the one from the Clover Installer may be broken\)**

---

# Network Installer Prerequisites

!> <big><big><b>Apparently, the latest version of Clover doesn't inject Etherent kexts \(which is needed for network installer\). Make an [Offline Installer](offline-installer-prerequisites.md) instead!!!</b></big></big>

~~You'll need to have **LAN \(Ethernet\) connection** if you are making a **Network Installer**. If you do _**NOT**_ have, please make an~~ [~~**Offline Installer**~~](offline-installer-prerequisites.md) ~~instead.~~

### ~~General~~

* ~~You **MUST** have fast Internet Speed \(at least 20 Mbps\). If your Internet Speed is slow, make an Offline Installer instead as the Installer might be locked while installing.~~

### ~~Preparation for making an Offline Installer from macOS~~

* ~~[Clover install package](https://cloverdb.com) \(Get the latest and remember the version\)~~
* ~~[Clover Configurator](https://mackie100projects.altervista.org/download-clover-configurator/) \(for editing the config\)~~

### ~~Preparation for making an Network Installer from Windows~~

* ~~[Clover Cloud Editor](http://cloudclovereditor.altervista.org/cce/index.php) \(You'll need this site later for making you config.plist\)~~

---

# Offline Installer Prerequisites

### General

* A clone of [MakeInstallmacOS](https://github.com/doesprintfwork/MakeInstallmacOS)
* **\[OPTIONAL\]** Fast Internet Speed
* [PYTHON 3.4 or above \(Recommended: 3.7, with add to PATH selected\)](https://www.python.org/downloads/)

### Preparation for making an Offline Installer from macOS

* [Clover install package](https://cloverdb.com) \(Get the latest and remember the version\)
* [Clover Configurator](https://mackie100projects.altervista.org/download-clover-configurator/) \(for editing the config\)

### Preparation for making an Offline installer in Windows

* [Clover Cloud Editor](http://cloudclovereditor.altervista.org/cce/index.php) \(You'll need this site later for making you config.plist\)
* [TransMac](https://www.acutesystems.com/scrtm.htm)
* [Paragon Hard Disk Manager](https://www.paragon-software.com/free/pm-express/#) -- Although there are some issues, it is the only way we can resize an HFS+ Volume in Windows \(if you can find any better ways, tell me!\)
* [Boot Disk Utility](http://cvad-mac.narod.ru/index/bootdiskutility_exe/0-5) \(BDU\) -- For formatting disk and restoring files
* **You'll need** [7-zip](https://www.7-zip.org/) **\(installed to** `C:\Program Files (x86)\7zip`**\)** for the Scripts you'll use later.

---

# Requirements

* **AMD \(FX, Ryzen or Zen Athlon\) CPUs**
* **A dedicated GPU**
* _**Remember that the iGPU of AMD CPUs is not supported.**_
* For a complete list of supported GPUs, please refer to the [**GPU Buyers Guide**](https://khronokernel-3.gitbook.io/catalina-gpu-buyers-guide/) **and** _**remember your Highest Supported OS.**_
* As I haven't finished the Configuring Legacy Clover Part yet, this guide **requires a motherboard which support UEFI.** Sorry for keeping Legacy booting user waiting.

---

# Gathering Kexts

?> **<big>Please keep all of the downloaded kexts to a folder. We will need them later.</big>**

### What Kexts Do You Need?

#### Where can I find these kexts?

All the kexts shown here \(except SmallTreeIntel82576\) are available for download on the [kext repo](https://1drv.ms/f/s!AiP7m5LaOED-m-J8-MLJGnOgAqnjGw) provided and maintained by Goldfish64. **Do** _**NOT**_ **download and use all of the kexts listed below. Doing this may result a kernel panic.**

#### **What is absolutely required?**

[VirtualSMC.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455091&cid=FE4038DA929BFB23) _\(use this\)_ or [FakeSMC.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455161&cid=FE4038DA929BFB23) \(older, if VirtualSMC doesn't work, use this instead\) is as aforementioned essential. This kext is what tells macOS "Yes this is a real Mac", emulating the functionality of the SMC on real Mac's. Without it, no Hackintosh. **Do NOT use both of the SMC kexts.**

**You'll need these also.**

* [Lilu.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455053&cid=FE4038DA929BFB23) _-_ this kext acts as a loader for other kexts. More specifically it can patch kexts, processes and libraries.
* [Whatevergreen.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455095&cid=FE4038DA929BFB23)_-_ this kext fixes a lot of GPU related issues.
* [NullCPUPowerManagement.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455158&cid=FE4038DA929BFB23) **- This kext disables CPU power management,** _**as that is not supported on AMD chips.**_

#### Ethernet \(Choose the one you need\)

* [IntelMausiEthernet.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455134&cid=FE4038DA929BFB23) - this works with most newer Intel LAN chipsets **except I122-AT.**
* [AppleIntelE1000e.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455998&cid=FE4038DA929BFB23) - this works with older Intel LAN chipsets - but can cause kernel panics on newer chipsets
* [AtherosE2200Ethernet.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455105&cid=FE4038DA929BFB23) - this works for most Atheros or Killer networking chipsets
* [RealtekRTL8111.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455143&cid=FE4038DA929BFB23) - this works with most gigabit Realtek LAN chipsets
* [RealtekRTL8100.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455140&cid=FE4038DA929BFB23) - for 10/100 Realtek LAN chipsets
* [SmallTreeIntel82576.kext](https://drive.google.com/file/d/0B5Txx3pb7pgcOG5lSEF2VzFySWM/view) - **for Intel I122-AT LAN chipset** only.

#### USB Tethering

* [HoRNDIS.kext](https://github.com/midi1996/JBOG/blob/master/Extra/HoRNDIS.kext.zip?raw=true) - For USB tethering from Android **only**.

#### WiFi and Bluetooth 

\(I myself don't use bluetooth nor WiFi so I don't have knowledge in that, but here is some information on the subject by CorpNewt.\) 

> Apple is pretty minimal with their WiFi support, so I'll only cover the two main chipsets I'm familiar with. I've used a BCM94360CD + PCIe adapter, and BCM94352HMB/BCM94352Z in my Hackintoshes. The BCM94360CD worked OOB with no extras as it's a native card. For the BCM94352 flavors, I've been using [AirportBrcmFixup.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455063&cid=FE4038DA929BFB23) and the companion [Lilu.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455053&cid=FE4038DA929BFB23) for WiFi setup and _BrcmBluetoothInjector.kext_ \(on 10.13.6+\) or _BrcmPatchRAM2.kext_ alongside _BrcmFirmwareData.kext_ - all of the Brcm\* kexts are from RehabMan's [OS-X-BrcmPatchRAM](https://github.com/RehabMan/OS-X-BrcmPatchRAM) repo.

#### Audio \(Do not get both\)

* [AppleALC.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455056&cid=FE4038DA929BFB23) _-_ this kext supports most of the commonly used codecs, with the best quality. Ryzen CPUs are supported. **No FX support! Also, 3.5mm microphones are broken on Ryzen.**
* [VoodooHDA.kext ](https://sourceforge.net/projects/voodoohda/)_-_ a jack of all trades master of none solution to audio. **Required on FX. Mic support on Ryzen.**

### **Source Code Links**

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

---
