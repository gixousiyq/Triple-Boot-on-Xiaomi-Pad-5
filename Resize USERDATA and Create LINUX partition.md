# Resize USERDATA and Create LINUX partition


### After setting up Windows , Now boot to fastboot

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
resize # @GB $GB
```
- REPLACE # with USERDATA partition Number
- REPLACE @ with (USERDATA start Minus space you want for linux) Number
- REPLACE $ with (USERDATA end) Number
