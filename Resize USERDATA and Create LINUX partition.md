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
