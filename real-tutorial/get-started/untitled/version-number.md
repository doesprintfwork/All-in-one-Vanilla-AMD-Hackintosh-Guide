---
description: Guide for getting the version number of your offline installer.
---

# Version Number

### EXCLUSIVE FOR OFFLINE INSTALLER

1. Right click on your macOS Installer and select `Show Package Contents`
2. Go into SharedSupport and double click on BaseSystem.dmg to mount the disk.
3. Go into the mounted disk and go to `System/Library/CoreServices`
4. Open SystemVersion.plist with a text or plist editor.
5. The version number of your installer is the string value of the `VersionNumber`key.

