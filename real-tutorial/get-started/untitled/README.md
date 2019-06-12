# Prerequisites

## General

* An 8GB+ USB flash drive for the installer
* Kexts for your system \([Gathering Kexts](gathering-kexts.md)\)

### **The config file for Clover:**

#### _**For Intel Users:**_

* **PLEASE READ THE PLIST BASICS OVER** [**HERE**](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/config.plist-basics) **AND MAKE YOUR OWN config.plist with ProperTree config editor mentioned** [**below**](./#things-need-to-get-if-you-are-making-the-installer-in-windows)**.**

_**For AMD Users:**_ 

* [config.plist](https://github.com/AMD-OSX/AMD_Vanilla) from AMD OSX Github \(more explanation [here](amd-clover-config.plist.md)\)
* **PLEASE ALSO READ THE PLIST BASICS OVER** [**HERE**](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/config.plist-basics)**. THIS WILL BE HELPFUL FOR DEBUGGING AND POST-INSTALLING**

## Extra

### _**For Intel Pentium and AMD CPUs:**_

* NullCPUPowerManagement.kext
* > This kext disables CPU Power Management, as that is not supported on Pentium & AMD chips.

### Things need to get if you are making the installer in macOS

* [Clover install package](https://sourceforge.net/projects/cloverefiboot/)
* [Clover Configurator](https://mackie100projects.altervista.org/download-clover-configurator/) \(for editing the config only\)
* A clone of [gibMacOS](https://github.com/corpnewt/gibMacOS) for making the USB installer. **\(Only if you are making offline installer. More explanation** [**here**](../../preparing-the-installer-part-2/from-macos.md#youll-need-ethernet-connection-while-installing-macos-if-you-dont-have-a-ethernet-connection-go-to-the-next-page-for-offline-installation)**.\)**
* **macOS Install Mojave.app or macOS Install High Sierra.app.** \(Read the Requirements part below to know which version of macOS is compatible.\)
* **AMD USERS,** please note that only the versions that is on the vanilla patch github page will work. \(Go to this page to know how to check the version number of your installer.\)

### Things need to get if you are making the installer in Windows

* A clone of [gibMacOS](https://github.com/corpnewt/gibMacOS) for making the USB installer.
* A clone of [ProperTree](https://github.com/corpnewt/ProperTree) for configuring the config.plist.

## Requirements

* **Intel \(Core, Xeon or Pentium series\) or AMD \(FX or Ryzen or Zen Athlon\) CPUs**
* **Intel iGPU or a dedicated GPU.** _**Remember that the iGPU of AMD is not supported.**_ Either nVidia or AMD will work. **AMD GPUs are more recommended** because of the native support from macOS Mojave. **Most of the nVidia GPUs can only goes up to macOS High Sierra** \(only Kepler GPUs are supported in Mojave\). [_**Here**_](https://www.reddit.com/r/hackintosh/comments/b91vf5/mojave_gpu_buyers_guide/) is a compatible GPU list. _**Remember the highest supported version.**_
* _**Ethernet connection if you are making the installer from windows.**_

