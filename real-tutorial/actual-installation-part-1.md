---
description: Configuring the Bios settings
---

# Actual Installation - Part 1

### Go into Bios and configure these settings:

* XHCI Handoff: Enabled \(if applicable, some may not have this option\)
* EHCI Handoff: Enabled \(if applicable, some may not have this option\)
* OS Type: Other \(if applicable\)
* Secure Boot: Disabled \(refer to google or your motherboard's manual on how to disable it\)
* Legacy/CSM support: Disabled \[if you see a garbled screen, enable this\]
* **AHCI mode: SATA**

### Some more configurations:

* If you have an nVidia/AMD GPU:
  * NO DISPLAY is connected to the motherboard's DP/HDMI/VGA/DVI ports
  * Under System Agent \(SA\) \[or some other menu\], Graphics Settings, Main Display: PEG or PCIE
  * Disable anything like: Hybrid Graphics, Dual Graphics, DVMT size, APU ... that are related to intergrated graphics.
* If you have Intel GPU:
  * Make sure your DVMT pre-alloc \(not to be confused with DVMT size\), is set to 64MB \(or higher, 64 is enough\), DMVT size/apertures/whatever, to the max.

