# Prerequisites

## General

* An 8GB+ USB flash drive for the installer
* Kexts for your system \([Gathering Kexts](gathering-kexts.md)\)

### **The config file for Clover:**

#### _**For Intel Users:**_

* **PLEASE READ THE PLIST BASICS OVER** [**HERE**](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/config.plist-basics) **AND MAKE YOUR OWN config.plist with ProperTree config editor mentioned** [**below**](./#things-need-to-get-if-you-are-making-the-installer-in-windows)**.**

_**For AMD Users:**_ 

* [config.plist](https://github.com/AMD-OSX/AMD_Vanilla) from AMD OSX Github. \(More explanation [here](amd-clover-config.plist.md)\)
* **PLEASE ALSO READ THE PLIST BASICS OVER** [**HERE**](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/config.plist-basics)**. THIS WILL BE HELPFUL FOR DEBUGGING AND POST-INSTALLING.**

## Extra

### Things need to get if you are making the installer in macOS

* [Clover install package](https://sourceforge.net/projects/cloverefiboot/)
* [Clover Configurator](https://mackie100projects.altervista.org/download-clover-configurator/) \(for editing the config\)
* A clone of [gibMacOS](https://github.com/corpnewt/gibMacOS) for making the USB installer. **\(Only if you are making Network Installer. More explanation** [**here**](../../preparing-the-installer-part-2/from-macos.md#youll-need-ethernet-connection-while-installing-macos-if-you-dont-have-a-ethernet-connection-go-to-the-next-page-for-offline-installation)**.\)**
* \*\*\*\*[**macOS Install Mojave.app**](https://drive.google.com/open?id=1fp7cBfkWZcyCnt0gy6zIxf6uN_nD-v1G)**\(10.14.1 18B75\) or** [**macOS Install High Sierra.app**](https://drive.google.com/file/d/17U2GMCfIbLPN8SOfGoKl40vuIDZp3rt7/view)**\(10.13.6 17G65\).** You can either use your own install app or use the one provided here. Please read the [Requirements](./#requirements) part below to know which version of macOS is compatible. The installer provided is a compressed app file of the installer \[of course it is vanilla\] which is compatible for AMD. **\(This is for Offline Installer\)**
* **AMD USERS,** please note that only the versions of macOS Installer which are listed on [the vanilla patches github page](https://github.com/AMD-OSX/AMD_Vanilla) will work. \(Go to [this page](version-number.md) to know how to check the version number of your installer.\)

### Things need to get if you are making the installer in Windows

* A clone of [**gibMacOS**](https://github.com/corpnewt/gibMacOS) for making the USB installer.
* A clone of [**ProperTree**](https://github.com/corpnewt/ProperTree) for configuring the config.plist.
* [**macOS Install Mojave.app**](https://drive.google.com/open?id=1fp7cBfkWZcyCnt0gy6zIxf6uN_nD-v1G)**\(10.14.1 18B75\) or** [**macOS Install High Sierra.app**](https://drive.google.com/file/d/17U2GMCfIbLPN8SOfGoKl40vuIDZp3rt7/view)**\(10.13.6 17G65\).** \(Only if you want to make an Offline Installer. More explanation [here](../../preparing-the-installer-part-2/from-macos.md#youll-need-ethernet-connection-while-installing-macos-if-you-dont-have-a-ethernet-connection-go-to-the-next-page-for-offline-installation). The installer provided is a pure zip file of the installer. It is compatible for AMD.\)
* \*\*\*\*[**TransMac**](https://www.acutesystems.com/scrtm.htm) ****\(Only if you want to make an Offline Installer. More explanation [here](../../preparing-the-installer-part-2/from-macos.md#youll-need-ethernet-connection-while-installing-macos-if-you-dont-have-a-ethernet-connection-go-to-the-next-page-for-offline-installation).\)

## Requirements

* **Intel \(Core, Xeon or Pentium series\) or AMD \(FX, Ryzen or Zen Athlon\) CPUs**
* **Intel iGPU or a dedicated GPU.** _**Remember that the iGPU of AMD CPUs is not supported.**_ Either nVidia or AMD will work. **AMD GPUs are recommended** because of the native support from macOS Mojave. **Most of the nVidia GPUs can only goes up to macOS High Sierra** \(only Kepler GPUs are supported in Mojave\). [_**Here**_](https://www.reddit.com/r/hackintosh/comments/b91vf5/mojave_gpu_buyers_guide/) is a compatible GPU list. _**Remember the highest supported version.**_
* _**Ethernet connection if you are making the installer from windows or you are making a Network Installer from macOS.**_

