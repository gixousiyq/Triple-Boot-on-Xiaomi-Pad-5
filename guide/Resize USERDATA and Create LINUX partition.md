# Resize USERDATA and Create LINUX partition

#### You dont need create esp for LINUX becuase Windows installation guide create esp automatically

### After setting up Windows , Now reboot to fastboot
- Boot your NABU into **fastboot** by holding down the **`volume down`** button during reboot

- Connect it to your PC/Laptop using a cable

### Boot into the modded recovery
> Replace `path\to\recovery.img` with the actual path of the recovery image
```cmd
fastboot boot path\to\recovery.img
```

### ADB SHELL
> run this command to get the shell , If it asks you to run it once again, do so
```cmd
adb shell
```

### Parted tool
> run this command to use parted tool
```cmd
parted /dev/block/sda
```

### print partition information
> to see partition numbers and space
```cmd
print
```

>[!WARNING]
>REMEMBER THE USERDATA START NUMBER BEFORE RESIZE , YOU WILL USE IT ON LINUX PARTITION CREATE STEP

### Resize USERDATA
> For make space for linux partition , DONT REMOVE GB!
```cmd
resizepart # @GB $GB
```
- REPLACE # with USERDATA partition Number
- REPLACE @ with (USERDATA start Minus space you want for linux) Number
- REPLACE $ with (USERDATA end) Number

### Make LINUX partition
> DO NOT REMOVE GB!
```cmd
mkpart linux ext4 #GB $GB
```
- REPLACE # with (old USERDATA start Number before Resize)
- REPLACE $ with (New USERDATA start Number after Resize)

### Check if partition is created
> make sure you have a partition name linux
```cmd
print
```

### Exit the SHELL
> for exit parted tool type
```cmd
quit
```
> for exit adb shell press CTRL + D or type
```cmd
exit
```
