# Solus as Guest
Mount the Guest Additions ISO from VirtualBox's menu. Then in the guest machine do the following:
```
sudo mkdir -p /mnt/cdrom
sudo mount -t iso9660 -o ro /dev/cdrom /mnt/cdrom
cd /mnt/cdrom
sudo sh VBoxLinuxAdditions.run
sudo reboot
```
