# Prerequisites

## General

* An 8GB+ USB flash drive for the installer
* Kexts for your system \([Gathering Kexts](gathering-kexts.md)\)

### **The config file for Clover:**

* **PLEASE READ THE PLIST BASICS OVER** [**HERE**](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/config.plist-basics) **AND MAKE YOUR OWN config.plist with Clover Configurator** \(On macOS\)**,** [**Clover Cloud Editor**](http://cloudclovereditor.altervista.org/cce/index.php) ****\(On Windows\) **or ProperTree config editor** \(Cross Platform Plist Editor, but difficult for people without any basis at programming\)**.**
* **For AMD:** Please also **read** the plist basics before going to [**this page**](../amd-clover-config.plist/).
* _**DO NOT GET THE SAMPLE CONFIG.**_

## Extra

{% hint style="danger" %}
You'll need to have **LAN \(Ethernet\) connection** if you are making a **Network Installer**. If you do _**NOT**_ have one, please make an **Offline Installer** instead.
{% endhint %}

### Things need to get if you are making the installer in macOS

* [Clover install package](https://sourceforge.net/projects/cloverefiboot/)
* [Clover Configurator](https://mackie100projects.altervista.org/download-clover-configurator/) \(for editing the config\)
* A clone of [gibMacOS](https://github.com/corpnewt/gibMacOS) for making the USB installer. **\(Only if you are making Network Installer. More explanation** [**here**](../preparing-the-installer-part-2/from-macos.md#youll-need-ethernet-connection-while-installing-macos-if-you-dont-have-a-ethernet-connection-go-to-the-next-page-for-offline-installation)**.\)**
* \*\*\*\*[**macOS Install Mojave.app**](https://drive.google.com/open?id=1fp7cBfkWZcyCnt0gy6zIxf6uN_nD-v1G) **\(10.14.1 18B75\) or** [**macOS Install High Sierra.app**](https://drive.google.com/file/d/17U2GMCfIbLPN8SOfGoKl40vuIDZp3rt7/view) **\(10.13.6 17G65\).** Please use the one provided here. Please read the [Requirements](prerequisites.md#requirements) part below to know which version of macOS is compatible. The installer provided is a compressed app file of the installer \[of course it is vanilla\] which is compatible for AMD. **\(This is for Offline Installer\)**

### Things need to get if you are making the installer in Windows

* A clone of [**gibMacOS**](https://github.com/corpnewt/gibMacOS) for making the USB installer.
* A clone of [**ProperTree**](https://github.com/corpnewt/ProperTree) for configuring the config.plist.
* [**macOS Install Mojave.app**](https://drive.google.com/open?id=1fp7cBfkWZcyCnt0gy6zIxf6uN_nD-v1G) **\(10.14.1 18B75\) or** [**macOS Install High Sierra.app**](https://drive.google.com/file/d/17U2GMCfIbLPN8SOfGoKl40vuIDZp3rt7/view) **\(10.13.6 17G65\).** \(**Only if you want to make an Offline Installer**. More explanation [here](../preparing-the-installer-part-2/from-macos.md#youll-need-ethernet-connection-while-installing-macos-if-you-dont-have-a-ethernet-connection-go-to-the-next-page-for-offline-installation). The installer provided is a pure zip file of the installer. It is compatible for AMD.\)
* \*\*\*\*[**TransMac**](https://www.acutesystems.com/scrtm.htm) ****\(Only if you want to make an Offline Installer. More explanation [here](../preparing-the-installer-part-2/from-macos.md#youll-need-ethernet-connection-while-installing-macos-if-you-dont-have-a-ethernet-connection-go-to-the-next-page-for-offline-installation).\)

## Requirements

* **Intel \(Core, Xeon or Pentium series\) or AMD \(FX, Ryzen or Zen Athlon\) CPUs**
* **Intel iGPU or a dedicated GPU.** _**Remember that the iGPU of AMD CPUs is not supported.**_ Either nVidia or AMD will work. **AMD GPUs are recommended** because of the native support from macOS Mojave. **Most of the nVidia GPUs can only goes up to macOS High Sierra** \(only Kepler GPUs are supported in Mojave\). [_**Here**_](https://www.reddit.com/r/hackintosh/comments/b91vf5/mojave_gpu_buyers_guide/) is a compatible GPU list. _**Remember the highest supported version.**_
* _**Ethernet connection if you are making the installer from windows or you are making a Network Installer from macOS.**_

