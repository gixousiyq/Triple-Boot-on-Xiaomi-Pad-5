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
