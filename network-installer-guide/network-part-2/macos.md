---
description: 把檔案還原到 USB
---

# 從 macOS

1. 重新命名 在 `gibMacOS/macOS Downloads/publicrelease/blahblahblah/` 中的 `XXXX.pkg` 到 `XXXX.dmg`
2. 雙擊後，會掛載一個新的容器
3. 開啟它並把 BaseSystem.dmg 複製到桌面
4. 開啟磁碟管理工具，選擇 **檢視 &gt; 顯示所有裝置，然後格式你的 USB 到（整個 USB）：** `名稱: [隨便] 格式: Mac OS Extended (Journaled)  架構: GUID Partition Map`
5. 選擇你的 **USB 的分割區並按 Restore**
6. 按 Choose image... 並選擇在桌面上的BaseSystem.dmg，再按還原
7. 漫長的等待。。。
8. 完成後到 [在 macOS 中安裝與設定 Clover](../../clover-installtion/usb-clover/usb-clover-macos.md)

![Steps 1 - 3](../../.gitbook/assets/ezgif-4-c4f2b894d040.gif)

![Steps 4 - 7](../../.gitbook/assets/restoring-to-usb.gif)

