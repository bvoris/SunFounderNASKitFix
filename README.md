# SunFounderNASKitFix
Sun Founder Raspberry Pi NAS Kit Fix

## Fix required the following:
Download of current Raspian OS
Installation of Raspbian
Enable SSH and SPI in Raspi-Config
Update of Raspberry PI OS
sudo apt update -y

## Installation of Open Media Vault
wget -O - https://raw.githubusercontent.com/OpenMediaVault-Plugin-Developers/installScript/master/install | sudo bash

## Download and installation of SunFounder NAS Kit repo
cd ~< BR/>
git clone https://github.com/sunfounder/nas-kit
cd ~/nas-kit
sudo python3 setup.py
chmod u+x /etc/init.d/omv-epd
chmod u+x /home/pi/nas-kit/bin/omv-epd
ln -s /home/pi/nas-kit/bin/omv-epd /etc/init.d/omv-epd
sudo systemctl daemon-reload
sudo systemctl enable omv-epd
sudo systemctl start omv-epd
