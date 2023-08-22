A  special thanks goes to Klaus Schmidinger Vdr Developer & all plugin developers

Two scripts: 
- vdr_installer_2.6.4 installs Vdr on Ubuntu with essential plugins (in about 15 min)
- vdr_plugins_installer installs others plugins 
  
# Script name: vdr_installer_2.6.4
A script for installing Vdr (stand alone) and Vdr Server (frontenf Kodi)
tested on Ubuntu 20.04 - 22.04 Linux Mint 21 Debian 11

At first install the OS (Ubuntu 20.04 - 22.04 Linux Mint 21 Debian 11)
then update the system (sudo apt update && sudo apt upgrade)

sudo apt install tar git wget (if not installed)
Create a new folder in your Home (mkdir -p 'a name of your choice for example myvdr')

cd 'a name of your choice'
download the file vdr_installer_2.6.x from here
and give a chmod 755 vdr_installer_2.6.x
cd /home/myvdr

Now we install the script
sudo ./vdr_installer_2.6.x

At first the script install some libraries
Then follow the script  ...

Point 1) 
* submenu a) the script creates a local repository folder (Vdr_repo) downloading FFmpeg 5.0.1 - Vdr 2.6.x - some basic plugins (softhddevice dvbapi skinlcarsng radio iptv) + other files needed by vdr
* submenu b) reinstall all

Point 2) 
* submenu a) install ffmpeg
* submenu b) Install Sat firmware
*submenu c) install Infra-Red Remotes Control (choice between lirc or eventlircd)
* submenu d) ONLY FOR Intel Devices (Intel vaapi driver) in many case not needed

Point 3) 
* submenu a) Install VDR-2.6.x
* submenu b) Uninstall VDR-2.6.x

Point 4) 
* submenu a) Install Plugins (softhddevice dvbapi skinlcarsng radio iptv)
* submenu b) Uninstall Plugins

Point 5) 
* submenu a) Configure VDR and all the system creating icons and something else :-)
  Pls note this point add the icons relating at Vdr Server (in this case Vdr will starts with only three plugins dvbapi radio iptv)
* submenu b) you can reconfigure the system

Point 6)
* submenu a) Install Kodi (plus kodi-pvr-iptvsimple & kodi-pvr-vdr-vnsi needed for using kodi as frontend for Vdr)
* submenu b) Uninstall Kodi

Point 7) Exit

Vdr starts at boot!!!
* The "dark" is in /usr/local/etc
* You can put your channells as usual in /etc/vdr
* plugins libs are placed in /lib/vdr

If you'd like add others plugins you can use another script called Vdr_plugins installer in the same github repo
    
#    Script name: Vdr_plugins_installer
Vdr version > 2.4.x  
Tested on Ubuntu 20.04 - Mint 20.3 - Ubuntu 22.04
chmod the script
then load it simply typing: sudo ./Vdr_plugins_installer   

*     Have fun!
