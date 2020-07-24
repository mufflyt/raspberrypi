# raspberrypi

## Excellent tutorial on going headless for the raspberry pi
https://www.youtube.com/watch?v=4mwXUAHsMEM

Terminal
touch Volumes/boot/ssh #adds ssh file to the SD card
ping raspberrypi.local #returns ping when it is on the network
ssh pi@raspberrypi.local

password: raspberry

#When we have multiple raspberry pis on one network then we need to rename then
sudo hostnamectl set-hostname raspberry001
sudo reboot
ssh pi@raspberry001.local
ip a #gives the ip address of 10.0.0.148/24

passwd #resets the password on the raspberry pi

raspi-config #settings
#Expand the boot drive so you have access to the entire card

##Installing Tor on the pi
#https://learn.adafruit.com/setting-up-a-raspberry-pi-as-a-wifi-access-point/check-ethernet-and-wifi

sudo apt-get update
sudo apt-get install hostapd isc-dhcp-server

sudo apt-get install iptables-persistent

#https://www.raspberrypi.org/documentation/remote-access/vnc/
New desktop is raspberry001:1 (10.0.0.147:1)
pi
f1-8
