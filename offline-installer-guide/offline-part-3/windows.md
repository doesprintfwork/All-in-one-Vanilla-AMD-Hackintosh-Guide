# 從 Windows

## 階段一 -- 把檔案複製到 USB 中

1. 插入你的 USB
2. 在 gibMacOS 資料夾中運行 MakeInstall.bat
3. 在視窗中，你的 USB 應被列出。輸入你的 USB 代號後按 Enter
4. 格式化你的 USB 後，程序會要求你輸入檔案的路徑，只需在以下的檔案：`gibMacOS/macOS Downloads/publicrelease/xxx-xxxxx - xx.xx.x macOS xxxx/RecoveryHDMetaDmg.pkg`

    按下 Shift 加右鍵，複製成路徑並到視窗中貼上後按 Enter

5. 程序會開始解壓安裝檔並把檔案還原到你的 USB 上，並會自動安裝 Clover

![](../../.gitbook/assets/ezgif-4-8fa1279bb84c.gif)

## Phase 2 -- Extend the Volume and Convert to Full Installer

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

