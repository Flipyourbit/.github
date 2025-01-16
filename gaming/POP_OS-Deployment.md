
![POP-OS Deployment](https://avatars.githubusercontent.com/u/33131755?s=200&v=4)
Donate if you can [POP__OS](https://pop.system76.com/ )
# POP OS Deployment


 # Contents
- [POP OS Deployment](#pop-os-deployment)
- [Contents](#contents)
- [POP\_OS! configuration guide](#pop_os-configuration-guide)
  - [Quick Start](#quick-start)
  - [Configure POP  network adapter](#configure-pop--network-adapter)
- [Configure Remote Desktop Access](#configure-remote-desktop-access)
  - [New user](#new-user)
  - [Add software](#add-software)
  - [Configure thinlinc server](#configure-thinlinc-server)
  - [Issues I have had](#issues-i-have-had)
  - [Join  POP to Flipyourbit Domain](#join--pop-to-flipyourbit-domain)
  
 :pushpin:  If you forget to run SUDO on a command you can run ***SUDO !!***  it will rerun the last command as sudo

# POP_OS! configuration guide

## Quick Start
 Place useful commands here 

```bash 
# Gives speed os SATA Devices
sudo dmesg | grep -i sata | grep 'link up'

#ip address  with color 
ip -c a 
#netadapter link status 
ip -c link 

```


## Configure POP  network adapter
link to doc in teams linux channel
```bash
ip link set dev {DEVICE} {up|down}
```
# Configure Remote Desktop Access 

[source](https://wiki.metalevel.tech/wiki/XRDP_on_Ubuntu_Desktop_and_Pop!_OS)


```bash
sudo apt update
sudo apt install xrdp
sudo systemctl enable xrdp
sudo systemctl status xrdp

echo 'export XDG_CURRENT_DESKTOP=ubuntu:GNOME' >> ~/.**xsessionrc**
```

Add the three export commands
```bash
sudo nano /etc/xrdp/startwm.sh

#!/bin/sh
# xrdp X session start script (c) 2015, 2017, 2021 mirabilos
# published under The MirOS Licence

# Rely on /etc/pam.d/xrdp-sesman using pam_env to load both
# /etc/environment and /etc/default/locale to initialise the
# locale and the user environment properly.

export GNOME_SHELL_SESSION_MODE=pop
export GDMSESSION=pop
export XDG_CURRENT_DESKTOP=pop:GNOME

if test -r /etc/profile; then
	. /etc/profile
fi

test -x /etc/X11/Xsession && exec /etc/X11/Xsession
exec /bin/sh /etc/X11/Xsession
```



## New user


##  Add software 
Pull Software from discord
- Remote Desktop and remote access client
  - Remmina  ```pop shop```
  - SPICE
- Office Tools
  - I use o365  yes yes I know irony 
  - libreoffice ```pop shop```
  - nano  ``` sudo apt install nano```
  - Drawio  ```pop shop```
  - xournal  ```pop shop```
  - Pinta for basic pic editing ```pop shop```
  - kirta  paint ```pop shop```
  - kolour paint ```pop shop```
  
- System Tools 
  - Btop is the one i lIke ```sudo apt install btop```
  - Htop
  - Gpu viwer ```pop shop```
  - Powershell 7   ``` google as many install guides```
  - cpux ```pop shop```
  
- Terminal
  - Tilix   ```pop shop```
  - VSCode ```download linux version from site```
- Chat Apps
  - Discord > Download the Deb pckg from their site, dont use the popshop 
- Password Managers
  - Bitwarden  ```Download the Deb from there site```
- GUI 
  - Gnome tweaks ``` google it many guides ```
- Gaming
  - Steam ``` download deb```
  - AMD drivers ``` AMD sites has the linux drivers```
  - Prims Launcher (Minecraft) ```pop shop```
  - Bottles ( will run almost any game launcher) ```pop shop```
  - 



## Configure thinlinc server 
  what the in hell was I talking about.



Linux Raid: <br> will flush this out later 
https://www.golinuxcloud.com/mdadm-command-in-linux/


## Issues I have had

- sleep function on  AMD hardware was broken I havent come back to this in like a years so probably fixed
- gnome randomly locks up had this on AMD hardware  but I think it was me not knowing what I was doing in the begining but wanted to mention it 

---
## Join  POP to Flipyourbit Domain
>  :construction: this document was created using Flipyourbit 

- ***Required Pacakages*** <br> 


- ***Verify DNS Settinges***<br>

 
- ***Verify Realm discovery***


- ***Join Server to domain***
    
- ***Configure SUDO access** <br>


        #EOF
