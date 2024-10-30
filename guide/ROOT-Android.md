# ROOT Android

## We will ROOT Android with MAGISK

### Download MAGISK app
#### You Can find MAGISK app [HERE](https://github.com/topjohnwu/Magisk/releases)

### Patch BOOT.IMG
> Follow this guide to ROOT and PATCH BOOT.IMG
- Open MAGISK app
- Select First INSTALL Button
- Press [Select and Patch a File]
- Select The BOOT.IMG File You saved it
- Press [Let's Go]
- After Patch BOOT.IMG Open FILE MANGER app and Rename It to [root.boot.img]
- Upload the Patched Boot Image to Computer

### Reboot to FASTBOOT
- Boot your NABU into **fastboot** by holding down the **`volume down`** button during reboot

### Flash Patched Boot Image
```cmd
fastboot flash boot PATH/TO/root.boot.img
```
> Reboot to Android
```cmd
fastboot reboot
```
## Now You have rooted Android
##### DONT DELETE root.boot.img YOU WILL NEED IT !!!

# [NEXT STEP: Create Boot Image For LINUX by timoxa0](/guide/Create-Boot-Image-For-LINUX.md)
