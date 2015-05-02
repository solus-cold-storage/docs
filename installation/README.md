# Installation
###Requirements:
- USB drive of 2GB or more
- Ability to boot via USB
- ISO file from https://solus-project.com/download/

####Windows Tools:
**SUSE Image Writer** - https://github.com/downloads/openSUSE/kiwi/ImageWriter.exe
**Rufus** - https://rufus.akeo.ie/

####Linux:
**Gnome Multi-Writer**

https://wiki.gnome.org/Apps/MultiWriter

**DD**:
1. Insert USB drive of 2GB or more.
2. Open your terminal
3. Type:
```
lsblk
```
You will get output similar to this:
```
NAME   MAJ:MIN RM   SIZE RO TYPE MOUNTPOINT
fd0      2:0    1     4K  0 disk
sda      8:0    0 111.8G  0 disk
├─sda1   8:1    0   100M  0 part
├─sda2   8:2    0  50.1G  0 part
├─sda3   8:3    0  30.9G  0 part
├─sda4   8:4    0     1K  0 part
└─sda5   8:5    0  30.8G  0 part /
sde      8:64   1   7.5G  0 disk
└─sde1   8:65   1   754M  0 part
```
4. You will see one disk, in my case "sde" that is roughly the size of your USB Drive, note this down.
5. Locate the downloaded ISO e.g cd ~/Downloads
6. **Dangerous Step**
   This is where we **OVER-WRITE** the contents of your USB drive so please ensure you identified the CORRECT drive in lsblk above.
   My command would be below, however you will need to replace sde with the drive we located above
   ```
sudo dd if=Solus-Beta1.1.iso of=/dev/sde bs=1M;sync
```
This will write the contents of the ISO to the thumb drive so you can boot it and also make sure the data is synchronised so you can eject the USB safely.
7. Reboot and select your USB Drive in your PC's boot menu (usually a function key like F10).
8. Enjoy!
