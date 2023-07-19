# Ubuntu-Modded-OS
Ubuntu Modded Os for termux-x11

This is a preinstalled Ubuntu Distro with XFCE Desktop.For Android 12 & 13,before you install it,disable phantom process killer. 

[Watch Video Here](https://youtu.be/UxmQSETvAOc) 


## Preview 

![](https://raw.githubusercontent.com/atamshkai/Ubuntu-Modded-OS/main/focal-xfce.png)

![](https://raw.githubusercontent.com/atamshkai/Ubuntu-Modded-OS/main/gold.png)

![](https://raw.githubusercontent.com/atamshkai/Ubuntu-Modded-OS/main/neon.png)

# To Do

### First,Download Ubuntu-Linux Distro From Here. 
[Download](https://archive.org/download/focal-xfce/focal-xfce.tar.xz
) 

## Installation 
Download focal-xfce.tar.xz to Device's Download folder first. 

### Install zsh 
``` 
pkg up -y && pkg i -y zsh wget
wget https://github.com/atamshkai/Termux-Zsh/raw/main/zsh.tar.xz 
tar -xvJf zsh.tar.xz && mv ~/zsh/.* ~/
rm -rf ~/zsh
chsh -s zsh 
``` 
#### For Sound, 
``` 
echo "killall pulseaudio &>/dev/null" >>~/.zshrc 
``` 
```
echo "pulseaudio --start --exit-idle-time=-1; pacmd load-module module-native-protocol-tcp auth-ip-acl=127.0.0.1 auth-anonymous=1" >>~/.zshrc 
```
#### Install needed packages 
``` 
pkg up -y && pkg i -y x11-repo && pkg i -y proot-distro pulseaudio termux-x11-nightly 
``` 
#### Give Storage Permission

``` 
termux-setup-storage 
```
### Move focal-xfce.tar.xz to termux's home
```
mv /sdcard/download/focal-xfce.tar.xz ~/
```
### Unzip Ubuntu Distro
```
tar -xvJf ~/focal-xfce.tar.xz
 
```
### Move ~/focal-xfce/focal-xfce-binds & ~/focal-xfce/focal-xfce.sh to ~/
```
mv ~/focal-xfce/focal-xfce-binds ~/focal-xfce/focal-xfce.sh ~/
 
```
```
exit
```
#### Login again to terminal 
Before login to proot,start termux-x11 first. 
``` 
termux-x11 :1 
```
#### Open another session & start focal-xfce
```
bash ~/focal-xfce.sh
```
#### Start focal-xfce
```
xfce
```
#### Delete some bugs
```
rm -rf /usr/bin/.l2s.perlbug0001 /usr/bin/perlthan* /usr/bin/perlbug
```
#### Change Style (Default is windows style)

##### Change to gold style
```
gold
```
#### Login to focal-xfce again
```
exit
```
##### Change Style to windows style
```
windows
```
 
## Termux 
[Download](https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_universal.apk) 
## Termux-x11 
[Download](https://archive.org/download/termux-x11/app-universal-debug.apk) 
## Termux-x11 Custom Resolution
1920:1080
