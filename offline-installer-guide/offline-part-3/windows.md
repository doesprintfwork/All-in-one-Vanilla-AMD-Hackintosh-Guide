# 從 Windows

## 階段一 -- 格式化、分區並安裝 Clover 在你的 USB 上 <a id="jie-duan-yi-ge-shi-hua-fen-ou-bing-an-zhuang-clover-zai-ni-de-usb-shang"></a>

1. 插入你的 USB
2. 開啟 BDU \(Bootdisk Utility\)
3. 到 Options &gt; Configuration 按 Check Now 此步讓程式自動取得最新版本的 Clover
4. 選擇在列表中的 USB 並按 Format
5. 程式會把你的 USB 分成兩個分區 1. CLOVER \(EFI 分區， BDU 會自動安裝 Clover\) 2. HFS+ （主要安裝文件分區）
6. 完成後，不要關閉視窗並到下一階段

![](../../.gitbook/assets/ezgif-4-b59bb851e67a.gif)

## 階段二 -- 從 BaseSystem.dmg 中解壓縮文件並還原到 USB <a id="phase-2-extract-and-restore-files-from-basesystem-dmg"></a>

1. Go to BDU &gt; Tools &gt; Extract HFS \(HFS+\) from DMG-file.
2. Select the BaseSystem.dmg from the downloaded folder.
3. Choose Desktop as the Destination folder.
4. It will start to extract the 4.hfs file from BaseSystem.dmg. Be patient.
5. Once it is finished, the command promt window should be automatically closed.
6. Press the plus button next to the USB and choose Part 2.
7. Press Restore and choose the extracted 4.hfs file.
8. BDU will start to restore the files to your USB. Be patient.

## Phase 3 -- Extend the Volume and Convert to Full Installer

1. Open Paragon Disk Manager
2. Go to Partition Manager
3. Choose the second partition of your USB and choose Resize Partition
4. Set Space after partition to 0 and press OK
5. Press Apply
6. Close it and run TransMac as Administrator
7. Click on your USB and go to `macOS Base System (or OS X Base System)/Install macOS xxx.app/Contents`
8. Drag and drop the prepared SharedSupport folder here
9. Done! Proceed to the [next part](../../clover-installtion/usb-clover/usb-clover-win.md)!

![Steps 1 - 5](../../.gitbook/assets/ezgif-4-3f1d85748df0.gif)

![Steps 6 - 8](../../.gitbook/assets/2019-06-16-22-29-_2.gif)

