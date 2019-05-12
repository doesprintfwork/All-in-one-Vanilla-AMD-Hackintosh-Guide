# Prerequisites

## General

* An 8GB+ USB flash drive for the installer
* A clone of [gibMacOS](https://github.com/corpnewt/gibMacOS) for making the USB installer
* Kexts for your system \([Gathering Kexts](gathering-kexts.md)\)

### **The config file for Clover \(clover.plist, clone or download the whole repositories mentioned below\):**

#### _**For Intel Users:**_

* [config.plist](https://github.com/corpnewt/Hackintosh-Guide/tree/master/Configs) from CorpNewt. \(use the one which is for you cpu architecture\)
* _**I STRONGLY recommend you to read the clover basics over**_ [_**here**_](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/config.plist-basics)_**.** This will help a lot after you have installed macOS._

_**For AMD Users:**_ 

* config.plist from AMD OSX Github \(more explanation [here](amd-clover-config.plist.md)\)
* NullCPUPowerManagement.kext
* > This kext disables CPU Power Management, as that is not supported on Pentium, Celeron, Atom &  AMD chips.

## Extra

### _**For Intel Pentium, Celeron & Atom and AMD CPUs:**_

* NullCPUPowerManagement.kext
* > This kext disables CPU Power Management, as that is not supported on Pentium, Celeron,  Atom & AMD chips.

### Things need to get if you are making the installer in macOS

* [Clover install package](https://sourceforge.net/projects/cloverefiboot/)
* [Clover Configurator](https://mackie100projects.altervista.org/download-clover-configurator/) \(for editing the config only\)

## Requirements

* **Intel or AMD \(FX or Ryzen or Zen Athlon\) CPUs**
* **Intel iGPU \(except Pentium, Celeron & Atom\) or a dedicated GPU.** Either nVidia or AMD will work. **AMD GPUs are more recommended** because of the native support from macOS Mojave. **Most of the nVidia GPUs can only goes up to macOS High Sierra** \(only Kepler GPUs are supported in Mojave\). **Non native nVidia GPUs perform even worse than Intel iGPU \(i.e.: UHD630\) on AMD CPUs in my opinion.** [_**Here**_](https://www.reddit.com/r/hackintosh/comments/b91vf5/mojave_gpu_buyers_guide/) is a compatible GPU list. _**Remember the highest supported verison.**_



