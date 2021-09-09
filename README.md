# SunFounder NAS Kit Fix
Sun Founder Raspberry Pi NAS Kit Fix
## Walkthrough
Originally found reviewing SunFounder's Github rebo here:<BR />
https://github.com/sunfounder/nas-kit/issues/4<BR />

## Fix required the following:
Download of current Raspian OS
Installation of Raspbian
Enable SSH and SPI in Raspi-Config
Update of Raspberry PI OS
sudo apt update -y

## Installation of Open Media Vault
wget -O - https://raw.githubusercontent.com/OpenMediaVault-Plugin-Developers/installScript/master/install | sudo bash

## Download of SunFounder NAS Kit repo
cd ~<BR />
git clone https://github.com/sunfounder/nas-kit<BR />

## Installation of Sunfounder NAS Kit
cd ~/nas-kit<BR />
sudo python3 setup.py<BR />
## Make omv-epd executable
ln -s /home/pi/nas-kit/bin/omv-epd /etc/init.d/omv-epd<BR />
chmod u+x /etc/init.d/omv-epd<BR />
chmod u+x /home/pi/nas-kit/bin/omv-epd<BR />
## Make omv-epd a service
sudo systemctl daemon-reload<BR />
sudo systemctl enable omv-epd<BR />
sudo systemctl start omv-epd<BR />
sudo reboot<BR />

# Connect with me at

<a href="https://twitter.com/HMInfoSecViking?ref_src=twsrc%5Etfw"><IMG SRC="https://github.com/bvoris/bvoris/blob/master/twitter.jpg" WIDTH=10% HEIGHT=10% ALIGN=LEFT></a>

<a href="https://www.linkedin.com/in/brad-voris" target="_blank"><IMG SRC="https://github.com/bvoris/bvoris/blob/master/linkedin.png" WIDTH=10% HEIGHT=4% ALIGN=RIGHT></a>

<BR /><BR />
<BR /><BR />

<A HREF="https://www.victimoftechnology.com">Victim Of Technology<A />
<BR /><BR />
<A HREF="https://www.cyberforgesecurity.com">Cyber Forge Security, Inc.<A />
<BR /><BR />

