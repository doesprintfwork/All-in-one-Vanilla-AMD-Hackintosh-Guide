# 收集 Kexts

### 請將所有已下載的 Kexts 放到一個資料夾內

## 你需要什麼 Kexts?

### 我可以在哪裡找到這些 Kexts?

* 所有在此顯示的 Kexts（除 SmallTreeIntel82576 以外）都可從由 Goldfish64 提供以及維護的 [_**Kext Repo**_](https://kext.goldfish64.com) _**取得**_
* _**不要**_ **下載並使用所有 Kexts （可能會導致內核崩潰 Kernel Panic）**

### **什麼是必需的？**

[_VirtualSMC.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455091&cid=FE4038DA929BFB23) _\(使用這個\)_ 或 [FakeSMC.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455161&cid=FE4038DA929BFB23) \(較舊，會在 FAQ 中提到\) 這個 kext 告訴 macOS "對這是一台真的 Mac", 模擬在真 Mac 上 SMC 的功能。如果沒有了它，便沒有黑蘋果。**不要同時使兩個 SMC kexts.**

**你亦需要這些**

* [_Lilu.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455053&cid=FE4038DA929BFB23) _-_ 這個 Kext 就像其它 Kexts 的載入器
* [_Whatevergreen.kext_ ](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455095&cid=FE4038DA929BFB23)_-_ 這個 Kext 可修複許多 GPU 的問題

### Ethernet \(Choose the one you need\)

* _​_[_IntelMausiEthernet.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455134&cid=FE4038DA929BFB23) - this works with most newer Intel LAN chipsets **except I122-AT.**
* [_AppleIntelE1000e.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455998&cid=FE4038DA929BFB23) - this works with older Intel LAN chipsets - but can cause kernel panics on newer chipsets
* _​_[_AtherosE2200Ethernet.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455105&cid=FE4038DA929BFB23) - this works for most Atheros or Killer networking chipsets
* _​_[_RealtekRTL8111.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455143&cid=FE4038DA929BFB23) - this works with most gigabit Realtek LAN chipsets
* _​_[_RealtekRTL8100.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455140&cid=FE4038DA929BFB23) - for 10/100 Realtek LAN chipsets
* \*\*\*\*[_SmallTreeIntel82576.kext_](https://drive.google.com/file/d/0B5Txx3pb7pgcOG5lSEF2VzFySWM/view) - **for Intel I122-AT LAN chipset** only.

### USB Tethering

* \_\_[_HoRNDIS.kext_](https://github.com/midi1996/JBOG/blob/master/Extra/HoRNDIS.kext.zip?raw=true) - For USB tethering from Android **only**.

### WiFi and Bluetooth 

\(I myself don't use bluetooth nor WiFi so I don't have knowledge in that, but here is some information on the subject by CorpNewt.\) 

> Apple is pretty minimal with their WiFi support, so I'll only cover the two main chipsets I'm familiar with. I've used a BCM94360CD + PCIe adapter, and BCM94352HMB/BCM94352Z in my Hackintoshes. The BCM94360CD worked OOB with no extras as it's a native card. For the BCM94352 flavors, I've been using [_AirportBrcmFixup.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455063&cid=FE4038DA929BFB23) __and the companion [_Lilu.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455053&cid=FE4038DA929BFB23) __for WiFi setup and _BrcmBluetoothInjector.kext_ \(on 10.13.6+\) or_BrcmPatchRAM2.kext_ alongside _BrcmFirmwareData.kext_ - all of the Brcm\* kexts are from RehabMan's [_OS-X-BrcmPatchRAM_](https://github.com/RehabMan/OS-X-BrcmPatchRAM) __repo.

### Audio \(Do not get both\)

* [_AppleALC.kext_](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455056&cid=FE4038DA929BFB23) _-_ this kext supports most of the commonly used codecs, with the best quality. Intel CPUs and Ryzen CPUs are supported. **No FX support! Also, 3.5mm microphones are broken on Ryzen.**
* \*\*\*\*[_VoodooHDA.kext_ ](https://sourceforge.net/projects/voodoohda/)_-_ a jack of all trades master of none solution to audio. **Required on FX. Mic support on Ryzen.**

### **Misc \(**_**MUST GET THIS**_**\)**

* [NullCPUPowerManagement.kext](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455158&cid=FE4038DA929BFB23) **- This kext disables CPU power management,** _**as that is not supported on AMD chips.**_

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

