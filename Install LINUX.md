# Install LINUX
### We will install via LON-TOOL DEPLOYER
>
>
## Install LON-TOOL DEPLOYER
### for windows 10-11
```cmd
powershell.exe -C "irm https://s.tx0.su/ltw | iex"
```
>
### for LINUX/MAC OS
```cmd
curl -Ls s.tx0.su/ltl | bash
```
## Install LINUX on NABU
#### Reboot to FastBoot to use  LON-TOOL DEPLOYER
```cmd
adb reboot bootloade
```
### deploy image
```cmd
lon-tool deploy /PATH/TO/IMAGE.LNI
```
>[!WARNING]
>When LON-TOOL say
>
>Found compatible partition table. Do you want to change it? [y/N]
>
>PLEASE SAY NO!
>

### Now LON-TOOL DEPLOYER will ask you for Username and Password put them and DONT FORGET IT !

### Wait for LON-TOOL DEPLOYER to flash LINUX

#### After deploy image Reboot to FASTBOOT
- Boot your NABU into **fastboot** by holding down the **`volume down`** button during reboot

### Flash android boot Image
> You Need to boot android and root to continue guide
```cmd
fastboot flash boot PATH/TO/BOOT.IMG
```
> Now Reboot to Android
```cmd
fastboot reboot
```
