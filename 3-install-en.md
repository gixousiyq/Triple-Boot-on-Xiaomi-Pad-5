<img align="right" src="https://raw.githubusercontent.com/erdilS/Port-Windows-11-Xiaomi-Pad-5/main/nabu.png" width="425" alt="Windows 11 Running On A Xiaomi Pad 5">

# Running Windows on the Xiaomi Pad 5

## Installation

### Prerequisites
- ```Brain```

- [```DriveLetterAssigner```](https://github.com/Misha803/My-Scripts/releases/tag/DriveLetterAssigner)
  
- [```ARM Windows ESD```](https://arkt-7.github.io/woawin/)
    
- [```Drivers```](https://github.com/erdilS/Port-Windows-11-Xiaomi-Pad-5/releases/tag/Drivers)

- [```UEFI image```](https://github.com/erdilS/Port-Windows-11-Xiaomi-Pad-5/releases/download/UEFI/uefi-v3.img)

- [```Modified recovery image```](https://github.com/erdilS/Port-Windows-11-Xiaomi-Pad-5/releases/download/1.0/recovery.img)

### Boot into the modded recovery
> Replace `path\to\recovery.img` with the actual path of the recovery image
```cmd
fastboot boot path\to\recovery.img
```

### Execute msc 
> If it asks you to run it once again, do so
```cmd
adb shell msc
```

### Make partition space for Wndows
> If it asks you to run it once again, do so
```cmd
adb shell partition 80
```

### Assign letters to WINNABU and ESPNABU
> Open the **DriveLetterAssigner** script and press `Y` on you your keyboard to automatically assign the letters **X** and **Y** to **WINNABU** and **ESPNABU**

### Installing Windows
> [!Important]
> Make sure that you are running CMD/Powershell as an **Administrator**

> Replace `path\to\install.esd` with the actual path of install.esd (it may also be named install.wim or 22631.2861.XXXXXXX.esd)

```cmd
dism /apply-image /ImageFile:path\to\install.esd /index:6 /ApplyDir:X:\
```

> If you get `Error 87`, check the index of your image with `dism /get-imageinfo /ImageFile:path\to\install.esd`, then replace `index:6` with the actual index number of **Windows 11 Pro** in your image

### Copying your boot.img into Windows
- Drag and drop the **rooted_boot.img** from the **platform-tools** folder into the **WINNABU** disk in Windows Explorer, then rename it to **boot.img**.

### Installing Drivers
- Unpack the driver archive, then open the `OfflineUpdater.cmd` file (if an error shows up, run `OfflineUpdaterFix.cmd` instead)

> If it asks you to enter a letter, enter the drive letter of **WINNABU** (which should be **X**), then press enter

#### Create Windows bootloader files for the EFI
> If an error occurs when copying boot files, run **DriveLetterAssigner** again, then run the following command again, replacing **Y** with **U**
```cmd
bcdboot X:\Windows /s Y: /f UEFI
```

#### Remove the drive letter for ESPNABU
> If this does not work, ignore it and skip to the next command. This phantom drive will disappear the next time you reboot your PC.
```cmd
mountvol y: /d
```

### Reboot to fastboot
```cmd
adb reboot bootloader
```

#### Boot into the UEFI
> Replace `path\to\nabu-uefi.img` with the actual path of the UEFI image
```cmd
fastboot boot path\to\nabu-uefi.img
```

###Now finish SETTING UP windows





















