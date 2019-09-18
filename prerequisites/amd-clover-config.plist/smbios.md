---
description: 設定 SMBIOS.
---

# SMBIOS

1. 準備你的 config.plist
2. 下載 [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
3. 開啟 GenSMBIOS.bat \(Windows\) 或右鍵開啟 GenSMBIOS.command \(macOS\)
4. 輸入 1 後按 Enter \(下載或更新 MacSerial\)
5. 輸入 2 後按 Enter
6. 拖曳你的 config.plist 到程式裡後按 Enter
7. Y
8. 輸入 3 後按 Enter
9. 輸入你需要的 SMBIOS 並輸入你所需要的 SMBIOS 的量後按 Enter **對於 AMD,** 以下列出所有推薦的 SMBIOS - _**iMacPro1,1**_ \(最推薦\) - _**iMac14,2**_ \(亦推薦\) - MacPro6,1 \(比較舊\) - MacPro5,1 \(很舊且已在 Catalina 中失去支援\) - Other SMBIOS \(不推薦 可能會造成其他問題\)
10. 第一個 SMBIOS 會被加到 config.plist 中
11. 到[此網站](https://checkcoverage.apple.com/)去確認你的序號 \(Serial Number\) 為_**無效的 \(invalid\)**_
12. 如果你得到無效的序號，完成。如果並沒有，請由第 9 步重做直至找到無效的序號

![Steps 1 - 10 \(Generating SMBIOS\)](../../.gitbook/assets/ezgif-5-2d971096ef3a.gif)

![Steps 11 - 12 \(Checking Serial Number\)](../../.gitbook/assets/ezgif-5-776e8fe4f7f4.gif)



