# Solus as Host
Download the latest VirtualBox Installer from here:
```
https://www.virtualbox.org/wiki/Linux_Downloads
```
Now install the dependencies and VirtualBox like so:
```
sudo eopkg it -c system.devel
sudo eopkg it kernel-headers
sudo ./VirtualBox-4.3.26-98988-Linux_amd64.run
sudo /etc/init.d/vboxdrv setup
```
Replace version number of file with the one you download.

**Note:**
You will need to run this command after each reboot of your host machine or VMs will not start:
```
sudo /etc/init.d/vboxdrv setup
```
