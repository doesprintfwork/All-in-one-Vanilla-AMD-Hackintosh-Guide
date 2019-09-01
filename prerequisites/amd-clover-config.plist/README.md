---
description: AMD CPU 的 Config.plist
---

# AMD Clover config.plist

## 事先準備

* 請到 AMD OS X 的 Github 中 拿到 patches.plist \([Ryzen](https://raw.githubusercontent.com/AMD-OSX/AMD_Vanilla/master/17h/patches.plist), [FX](https://raw.githubusercontent.com/AMD-OSX/AMD_Vanilla/master/15h_16h/patches.plist), 右鍵另存新檔\)
* 使用 Clover Configurator \(CCG\) 或 [Clover Cloud Editor](http://cloudclovereditor.altervista.org/cce/index.php) \(CCE\) 打開 patches.plist

{% hint style="info" %}
**如果你使用 CCE**, 請到主頁把_`Show Find/Replace/TgtBridge values as:`_設定為_`Hex`_
{% endhint %}

{% hint style="success" %}
**請根據截圖設定後，再使用 RAW XML 檢查**
{% endhint %}

## ACPI

### RAW XML

```markup
<key>ACPI</key>
<dict>
	<key>DSDT</key>
	<dict>
		<key>Fixes</key>
		<dict>
			<key>DeleteUnused</key>
			<true/>
			<key>FixHPET</key>
			<true/>
			<key>FixRTC</key>
			<true/>
			<key>FixShutdown</key>
			<true/>
			<key>FixTMR</key>
			<true/>
			<key>FixIPIC</key>
			<true/>
		</dict>
		<key>Patches</key>
		<array>
			<dict>
				<key>Comment</key>
				<string>change SAT0 to SATA</string>
				<key>Disabled</key>
				<false/>
				<key>Find</key>
				<data>U0FUMA==</data>
				<key>Replace</key>
				<data>U0FUQQ==</data>
			</dict>
		</array>
	</dict>
	<key>FixHeaders</key>
	<true/>
</dict>
```

### **解釋**

**Patches:**

首先，我們先設定 _Patches_ 部分。這一部分讓我們能使用 Clover 動態地重新命名 DSDT 中的部件。由於我們並不是在運行一部真的 Mac, 而 macOS 對部件的命名比較特別，所以我們可以無傷地更改部件名稱令到它們對 Mac 友善。我們只需一個：

* _change SAT0 to SATA_（更改 SAT0 到 SATA）- 更好的 SATA 兼容性

**開啟 Fix Shutdown**

* 可以修複一些關機的問題，例如按關機卻重新開機的問題等等。但這個選項又可能會在某些主機板上造成關機問題（沒錯神奇不神奇），所以如果你在開啟後有關機問題的話，關掉這個

**開啟 Fix IPIC, TMR, HPET and RTC**

* 可以修複一些音頻的問題

### CCE 截圖

![](../../.gitbook/assets/acpi.png)

## Boot

### RAW XML

```markup
<key>Boot</key>
<dict>
	<key>Arguments</key>
	<string>-v npci=0x2000</string>
	<key>DefaultVolume</key>
	<string>LastBootedVolume</string>
	<key>Legacy</key>
	<string>PBR</string>
	<key>Timeout</key>
	<integer>-1</integer>
</dict>
```

### **解釋**

**Arguments:**

* **-v** - 開啟囉嗦模式，把所有_幕後的事情_ 都顯示出來，可以更容易地找出問題與修複它們
* **npci=0x2000** - 修複卡住在 \[PCI Configuration Start\].

**Default Volume** - 設定預設開機容器 

* **LastBootedVolume** - 讓 Clover 自動選擇上次開機的容器（不論有沒有成功）

**Timeout \(秒\)** - 設定自動開機前時間

* **-1** - 關閉自動開機

**Legacy \(PBR\)** - 讓 Clover 使用 PBR 去啟動 Legacy 系統

### CCE 截圖

![](../../.gitbook/assets/boot.jpg)

## Boot Graphics \(which doesn't matter much\)

We have nothing to do here. You can tweak it if Clover doesn't show correctly.

## CPU

We have nothing to do here also.

## Devices

### RAW XML

```markup
<key>Devices</key>
<dict>
	<key>Audio</key>
	<dict>
		<key>ResetHDA</key>
		<true/>
	</dict>
	<key>USB</key>
	<dict>
		<key>Inject</key>
		<true/>
		<key>FixOwnership</key>
		<true/>
	</dict>
</dict>
```

### **解釋**

* **Reset HDA** - Puts the codec back in a neutral state between OS reboots. This prevents some issues with no audio after booting to another OS and then back.
* **USB** - Under this section, we ensure that _Inject_ and _FixOwnership_ are selected to avoid issues with hanging at a half-printed line somewhere around the `Enabling Legacy Matching` verbose line. You can also get past that by enabling _XHCI Hand Off_ in BIOS.

### CCE 截圖

![](../../.gitbook/assets/devices.png)

## Disable Drivers <a id="disable-drivers"></a>

We have nothing to do here.

## GUI

### RAW XML

```markup
<key>GUI</key>
<dict>
	<key>Scan</key>
	<dict>
		<key>Entries</key>
		<true/>
		<key>Linux</key>
		<true/>
		<key>Tool</key>
		<true/>
	</dict>
</dict>
```

### **解釋**

**Scan:**

The only settings I've tweaked on this page are the _Scan_ settings. I've selected _Custom_, then checked everything except _Legacy_ and _Kernel_. This just omits some of the unbootable entries in Clover to clean up the menu.

### CCE 截圖

![](../../.gitbook/assets/graphics.png)

## Graphics

### RAW XML

```markup
<key>Graphics</key>
<dict>
	<key>Inject</key>
	<false/>
	<key>RadeonDeInit</key>
	<false/>
</dict>
```

**Please refer to** [**GPU Buyers Guide**](https://khronokernel-3.gitbook.io/catalina-gpu-buyers-guide/) **and see which settings do you need for your GPU.**

## Kernel And Kexts Patches

The patches.plist \(which you are editing\) already has all of the patches you want to have. Those patches are used to patch the native Kernel.

* **AppleRTC \(enabled\)** - this ensures that we don't have a BIOS reset on reboot.

### CCE 截圖

![](../../.gitbook/assets/kernel-and-kext-patches.png)

## Rt Variables and SMBIOS

### RAW XML \(Rt Variables\)

```markup
<key>RtVariables</key>
<dict>
	<key>BooterConfig</key>
	<string>0x28</string>
	<key>CsrActiveConfig</key>
	<string>0x3e7</string>
	<key>ROM</key>
	<string>UseMacAddr0</string>
</dict>
```

### **解釋**

**RT Variables:** \(From CorpNewt's Vanilla Guide\)

We set _Rt Variables -&gt; ROM_ to `UseMacAddr0` which just utilizes our onboard Mac address - this should be unique enough to not conflict with any others.

_BooterConfig_ gets set to `0x28`, and _CsrActiveConfig_ is set to `0x3e7` which effectively disables SIP **as SIP is not supported on AMD Systems unfortunately**.

**SMBIOS:**

[Please read this page after saving the config](smbios.md)

### CCE 截圖

![](../../.gitbook/assets/annotation-2019-06-21-101320.png)

## System Parameters

### RAW XML

```markup
<key>SystemParameters</key>
<dict>
	<key>InjectKexts</key>
	<string>Yes</string>
	<key>InjectSystemID</key>
	<true/>
</dict>
```

### **解釋**

**Inject Kexts:**

This setting has 3 modes:

* `Yes` - this tells Clover to inject kexts from the EFI regardless.
* `No` - this tells Clover not to inject kexts from the EFI.
* `Detect` - this has Clover inject kexts only if _FakeSMC.kext_ or _VirtualSMC.kext_ are not in the kext cache.

We set it to `Yes` to make sure that all the kexts we added before get injected properly.

**Inject System ID:**

This setting tells clover to set the SmUUID as the `system-id` at boot - which is important for iMessage and such.

**NvidiaWeb:**

This setting will force `nvda_drv=1` on every boot, this is recommended for users with non-functional NVRAM ****\(EmuVariableUEFI\) or issues switching from the default macOS drivers to the Nvidia WebDrivers.

### CCE 截圖

![](../../.gitbook/assets/system-parameters.png)

## Save and Exit

At this point, you can do _File -&gt; Save_ to save the config.plist \(or go back to home page and download your config.plist if you are using CCE\). Keep it to somewhere you'll remember.

