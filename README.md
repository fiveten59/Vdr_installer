A  special thanks goes to Klaus Schmidinger Vdr Developer & all plugin developers

Three scripts:
cross_vdr_installer_2.8.x
Debian_Suse_plugins_installer_1.x
Fedora_Arch_plugins_installer_1.x

# Script name: cross_vdr_installer_2.8.x

A cross platform script for installing Vdr
Tested on Fedora 44, Debian 13.6, EndeavourOS (Arch), Ubuntu 26.04 + Rpi 4/5 Debian Os Lite & Debian Desktop

At first install one of the above Os and as usual update the system
Create a new folder in your Home (mkdir -p 'a name of your choice for example myvdr')

cd 'a name of your choice'
download the file cross_vdr_installer_2.8.x from here
and give a chmod 755 cross_vdr_installer_2.8.x
cd /home/myvdr

Now we install the script
sudo ./cross_vdr_installer_2.8.x

Point A)
the script automatically recognize which is the Os you have and install the needed libraries

Point B) 
* submenu a) the script creates a local repository folder (Vdr_repo) downloading Vdr 2.8.x - some basic plugins: softhddevice (softhddevice-drm-gles in case of Rpi) dvbapi skinflatplus radio iptv & many patches needed by  
* submenu b) update all (the repository folder)

Point C)
* submenu a) PLS READ THIS SECTION THIS IS THE MORE COMPLICATED PART OF THE PROCESS!!! 
CHECK BEFORE IF FFMPEG IS ALREADY INSTALLED (in a terminal type ffmpeg: none means no ffmpeg)!!!
If not installed (usually is not) you can proceed with the script  
At first the script recognize which is the Os you have and install the needed libraries followed by the ffmpeg  
In any case:
Fedora: need use the script for installing FFmpeg
EndeavourOS: use the script for installing FFmpeg
Debian 13.6: skip (already installed)
Ubuntu 26.04: use the script for installing FFmpeg
Raspberry Os Lite: use the script for installing Rpi-FFmpeg
Raspberry Desktop Os: skip (already installed)
* submenu b) Install Inputlircd (needed by your remote)
* submenu c) Install some dvb drivers (hauppauge - skydvb)

Point D)
* Now install Vdr

Point E)
* Install some plugins (softhddevice, skinflatplus, dvbapi, iptv, radio, tvguide)

Point F)
* Install shared parts Desktop/Server systems (pls note the server version is under costruction)

Point G)
* Install Desktop Os Final configuration

Point H)
* Under construction

Point X)
* Exit the script
