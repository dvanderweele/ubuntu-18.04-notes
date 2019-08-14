# Automatic Updates

Install the package unattended-upgrades:
```bash
sudo apt install unattended-upgrades
```
The file to configure upgrade policies:
```
/etc/apt/apt.conf.d/50unattended-upgrades
```
To enable automatic updates, edit this file:
```
/etc/apt/apt.conf.d/20auto-upgrades
```
Sample configurations can be viewed [here](https://help.ubuntu.com/lts/serverguide/automatic-updates.html) on the Ubuntu doc website.
