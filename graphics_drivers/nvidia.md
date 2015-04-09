# NVIDIA
During install when prompted to install 32-bit libraries say no and yes to running nvidia-xconfig

Ensure your system is up to date and install dependencies:
```
sudo eopkg up
sudo eopkg it kernel-headers kernel-libc-devel
sudo eopkg it -c system.devel
```
Download the latest NVIDIA driver from (NVIDIA-Linux-x86_64-346.47.run, 70.1MB):
```
http://goo.gl/BI2WyG
```

Blacklist the nouveau driver and reboot:
```
sudo mkdir /etc/modprobe.d
echo "blacklist nouveau" | sudo tee /etc/modprobe.d/blacklist.conf
sudo reboot
```


Once rebooted hit Ctrl + Alt + F1 and type:
```
sudo systemctl stop lightdm
cd ~/Downloads;chmod +x NVIDIA-Linux-x86_64-346.47.run
sudo ./NVIDIA-Linux-x86_64-346.47.run
sudo reboot
```
