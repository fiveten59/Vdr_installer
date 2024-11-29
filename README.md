A  special thanks goes to Klaus Schmidinger Vdr Developer & all plugin developers

Two scripts: 
- vdr_installer_2.7.3 installs Vdr on Ubuntu with essential plugins (in about 15 min)
- vdr_plugins_installer installs others plugins 
  
# Script name: vdr_installer_2.7.3
A script for installing Vdr 
tested on Ubuntu 22.04 - 24.04 

At first install the OS (Ubuntu 22.04 - 24.04)
then update the system (sudo apt update && sudo apt upgrade)

sudo apt install tar git wget (if not installed)
Create a new folder in your Home (mkdir -p 'a name of your choice for example myvdr')

cd 'a name of your choice'
download the file vdr_installer_2.7.x from here
and give a chmod 755 vdr_installer_2.7.x
cd /home/myvdr

Now we install the script
sudo ./vdr_installer_2.7.x

At first the script install some libraries
Then follow the script  ...

Point 1) 
* submenu a) the script creates a local repository folder (Vdr_repo) downloading FFmpeg 7.0.0 - Vdr 2.7.x - some basic plugins (softhddevice dvbapi nopacity radio iptv) + other files needed by vdr
* submenu b) reinstall all

Point 2) 
* submenu a) install ffmpeg
* submenu c) install Infra-Red Remotes Control (eventlircd)
* submenu b) Install Sat firmware 
* submenu d) ONLY FOR Intel Devices (Intel vaapi driver) in many case not needed

Point 3) 
* submenu a) Install VDR-2.7.x
* submenu b) Uninstall VDR-2.7.x

Point 4) 
* submenu a) Install Plugins (softhddevice dvbapi skinnopacity radio iptv vnsiserver)
* submenu b) Uninstall Plugins

Point 5) 
* submenu a) Configure VDR and all the system
* submenu b) you can reconfigure the system

Point 6) Exit

Info:
* You can put your channells as usual in /etc/vdr
* plugins libs are placed in /lib/vdr

If you'd like add others plugins you can use another script called Vdr_plugins_installer in the same github repo
    
#    Script name: Vdr_plugins_installer
Vdr version > 2.7.x  
Tested on Ubuntu 22.04 - 24.04
chmod the script
then load it simply typing: sudo ./Vdr_plugins_installer   

*     Have fun!
