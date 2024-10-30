# Resize userdata and Create Linux partition
>
>You don't need to create ESP for Linux; because you already created ESP in Windows installation guide 

### After setting up Windows, Now reboot to fastboot
- Boot your NABU into **fastboot** by holding down the **`volume down`** button during reboot

- Connect it to your PC/Laptop using a cable

### Boot into the modded recovery
> Replace `path\to\recovery.img` with the actual path of the recovery image
```cmd
fastboot boot path\to\recovery.img
```

### Get to the recovery shell
> Run this command to get the shell
```cmd
adb shell
```

### Parted tool
> Run this command to start parted tool
```cmd
parted /dev/block/sda
```

### Print partitions information
> Run this to see partition numbers and the space they take
```cmd
print
```

>[!WARNING]
>REMEMBER THE USERDATA END ADDRESS BEFORE RESIZE, YOU WILL USE IT ON LINUX PARTITION CREATION STEP

### Resize USERDATA
> To make space for linux partition, DONT REMOVE GB!
```cmd
resizepart # @GB 
```
- REPLACE # with userdata partition Number
- REPLACE @ with (userdata end Minus space you want for linux)

  The mathematical formula would look something like:
  
  (userdata end) - (Size you want linux to have)

### Make LINUX partition
> DO NOT REMOVE GB!
```cmd
mkpart linux ext4 #GB $GB
```
- REPLACE # with (Old userdata end before Resize)
- REPLACE $ with (New userdata end
  after Resize)

### Check if partition is created
> make sure you have a partition name linux
```cmd
print
```

### Exit the SHELL
> to exit parted tool type
```cmd
quit
```
> to exit adb shell press CTRL + D or type
```cmd
exit
```

# [NEXT STEP: Install Linux](/guide/Install-LINUX.md)
