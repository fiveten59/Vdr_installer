A  special thanks goes to Klaus Schmidinger Vdr Developer & all plugin developers

Five scripts: 
- vdr_installer_2.7.8 installs Vdr on Ubuntu - Debian system with essential plugins
- fedora_vdr_installer_2.7.8 installs Vdr on Fedora system with essential plugins
- vdr_installer_2.7.8_rpi installs Vdr on Raspberry pi4-5 with essential plugins
- vdr_plugins_installer installs others plugins (Ubuntu - Debian - Raspberry systems)
- fedora_vdr_plugins_installer installs others plugins (Fedora system)
  
# Script name: vdr_installer_2.7.8
A script for installing Vdr 
tested on Ubuntu 22.04 - 24.04 - Debian 13 (Trixie) 

At first install the OS (Ubuntu 22.04 - 24.04 - Debian 13 (Trixie))
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
* submenu a) the script creates a local repository folder (Vdr_repo) downloading FFmpeg 7.1.1 - Vdr 2.7.x - some basic plugins (softhddevice dvbapi skinflatplus radio iptv vnsiserver) + other files needed by vdr
* submenu b) update all

Point 2) 
* submenu a) install ffmpeg (ubuntu repo)
* submenu b) install ffmpeg (7.1.1)
* submenu c) install Lirc (Only Ubuntu 24.04 manually)
* submenu d) install Infra-Red Remotes Control (eventlircd) 
* submenu e) Install Sat firmware 

Point 3) 
* submenu a) Install VDR-2.7.x
* submenu b) Uninstall VDR-2.7.x

Point 4) 
* submenu a) Install Plugins (softhddevice dvbapi skinnopacity radio iptv tvguide vnsiserver)
* submenu b) Uninstall Plugins

Point 5) 
* submenu a) Configure VDR and all the system
* submenu b) you can reconfigure the system

Point 6) Exit

Info:
* You can put your channells list in /var/lib/vdr
* plugins libs are placed in /usr/local/lib/vdr

If you'd like add others plugins you can use another script called Vdr_plugins_installer in the same github repo
    
#    Script name: Vdr_plugins_installer
Vdr version > 2.7.x  
Tested on Ubuntu 22.04 - 24.04 - Debian 13 (Trixie)
chmod the script
then load it simply typing: sudo ./Vdr_plugins_installer

# Simple script for installing Vdr on Raspberry Pi4 - Pi5

Os: 
Bookworm/Trixie Lite or Desktop 64 bit for Rpi4 - Rpi5

At first install Raspberry Pi OS  (script tested with Debian Bookworm)

After installation update the system (sudo apt update && sudo apt full-upgrade)
and configure through Raspi-config (sudo raspi-config)
- System Options - Set Wireless LAN (optional) - Set Boot on Console autologin wit Lite OS)
- Interface Options (optional but I suggest enable SSH for check and work from remote)
- 
- Localisation Options (Set 1,2 & 4  item - for the language L1 use yourlanguage-UTF8)
At the end reboot the system

Create a new folder in your Home (mkdir -p 'a name of your choice' f.e "myvdr")

Now we install the script

cd new folder
download the file

or copy/paste in this folder the script vdr_installer_2.7.X_rpi via Usb or SSH (ifconfig gives your IP address) or via Lan using Filezilla

chmod 755 vdr_installer_2.7.X_rpi

now we open the file
sudo su
./vdr_installer_2.7.X_rpi

And follow the script  ...
Trick: at point 1 type 'First install libraries' just only now

 1 creates a new folder downloading progs & libraries needed by Vdr 
 2 install some DVB firmware FFMPEG e Eventlircd
 3 install Vdr
 4 install Vdr  Basic plugins Softhddevice-drm-gles - Skinnopacity - Iptv - Radio - Dvbapi - Vnsiserver - TvGuide)

 5 configure all the Vdr system (remember when requested type b) Console)
Select a) installing shared parts 

 6 Final install
Select a) installing Vdr on consolle
Select b) installing Vdr on Desktop

Reboot

Tips & Tricks

Using a simple USB Audio Device [f.e. USB PnP Sound Device] from a remote terminal check
aplay -l and control where is your Usb - In my case I have
"card 1: Device [USB PnP Sound Device], device 0: USB Audio [USB Audio]"
so we have to change alsa.conf with
sudo nano /usr/share/alsa/alsa.conf
and change the two follwing lines
defaults.ctl.card 0
defaults.pcm.card 0
with
defaults.ctl.card 1
defaults.pcm.card 1

Using a solid sound device like hifiberry or similar add to (for example)
sudo nano /boot/config.txt
dtoverlay=hifiberry-dac 

- Libraries are in /usr/local/lib/vdr folder
- You can put your channells as usual in /var/lib/vdr


Have fun
