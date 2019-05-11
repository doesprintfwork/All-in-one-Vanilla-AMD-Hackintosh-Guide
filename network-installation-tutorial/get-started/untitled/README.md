# Prerequisites

## General

* An 8GB+ USB flash drive for the installer
* A clone of [gibMacOS](https://github.com/corpnewt/gibMacOS) for making the USB installer
* Kexts for your system \([Gathering Kexts](gathering-kexts.md)\)
* _**For Intel Pentium, Celeron & Atom**_
  * NullCPUPowerManagement.kext
  * > This kext disables CPU Power Management, as that is not supported on Pentium, Celeron,  Atom & AMD chips.
* _**For AMD Users:**_ 
  * config.plist from AMD OSX Github \(more explanation [here](amd-clover-config.plist.md)\)
  * NullCPUPowerManagement.kext
  * > This kext disables CPU Power Management, as that is not supported on Pentium, Celeron, Atom &  AMD chips.

### From macOS

* [Clover install package](https://sourceforge.net/projects/cloverefiboot/)
* [Clover Configurator](https://mackie100projects.altervista.org/download-clover-configurator/)

### From Windows

* No other special things

## Requirements

* **Intel or AMD \(FX or Ryzen\) CPUs**
* **Intel iGPU \(except Pentium, Celeron & Atom\) or a dedicated GPU.** Either nVidia or AMD will work. AMD GPUs are more recommended because of the native support from macOS Mojave. Most of the nVidia GPUs can only goes up to macOS High Sierra \(only Kepler GPUs are supported in Mojave\). [Here](https://www.reddit.com/r/hackintosh/comments/b91vf5/mojave_gpu_buyers_guide/) is a compatible GPU list. _**Remember the highest supported verison.**_



