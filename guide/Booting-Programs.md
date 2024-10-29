# Booting Program's

## on this step we will create switch system apps for each system

## 1st. Switch to WINDOWS/ANDROID
### Switch to WINDOWS for Android [WoA Helper] by [<img alt="Marius586" src="https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/80272004?v=4&w=45&fit=cover&mask=circle&maxage=7d" />](https://github.com/Marius586)
### Download WoA Helper from [HERE](https://github.com/Marius586/WoA-Helper-update/releases/tag/WOA)
- install the apk file
- open the app and grant it root access
- open FILE MANGER and put the UEFI image inside folder named `UEFI` on youre internal storage
### Create Switch to Android app for Windows [STA]
- on WoA Helper press WOA TOOLBOX
- Now press STA CREATOR
### Now Windows and Android is Ready 

## 2nd. Switch to LINUX/ANDROID
### Switch to Linux for Android [Switch2Linux] by [<img alt="timoxa0" src="https://avatars.githubusercontent.com/u/29687603?v=4" width="35" />](https://github.com/timoxa0)
### Download and install file named `linuxswitch.apk` from [HERE](https://git.timoxa0.su/timoxa0/Switch2Linux-Nabu/releases)
#### You don't need to Dump android images Because You already have it
- move `linux.boot.img` to `/sdcard/linux/` on youre NABU
- open the app and press `Switch to Linux` to set-up linux
### when linux put youre Username And Password youre putted them on LON-TOOL DEPLOYER
### on linux you need to download and install [s2a] by [<img alt="timoxa0" src="https://avatars.githubusercontent.com/u/29687603?v=4" width="35" />](https://github.com/timoxa0)
### Download and install file named `s2a.zip` from [HERE](https://git.timoxa0.su/timoxa0/Switch2Linux-Nabu/releases)
- Unzip `s2a.zip`
- put `root.boot.img` inside `/s2a/s2a/` and rename it to `android.boot.img`
- put `dtbo.img` inside `/s2a/s2a/` and rename it to `android.dtbo.img`
- install it with
```terminal
sudo ./install.sh
```
- After this command Switch2Android app will be installed on youre linux
### Now Linux and Android is Ready

### [Switch to linux for windows] and [Switch to Windows for linux] is not been developed yet.


# Now Triple Boot is Done.
