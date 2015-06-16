# Installation

### Requirements:
- USB drive of 2GB or more
- Ability to boot via USB
- ISO file from https://solus-project.com/download/
****

### Windows Tools:
**SUSE Image Writer**

https://github.com/downloads/openSUSE/kiwi/ImageWriter.exe

**Rufus**

https://rufus.akeo.ie/
****
### Linux Tools:
**Note unetbootin does NOT work**

**Gnome Multi-Writer (GUI)**

https://wiki.gnome.org/Apps/MultiWriter

**DD (Terminal)**:
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
├─sda1   8:1    0   350M  0 part
├─sda2   8:2    0  39.7G  0 part
└─sda3   8:3    0  71.8G  0 part /
sdb      8:64   1   7.5G  0 disk
├─sdb1   8:65   1   712M  0 part
└─sdb2   8:66   1  17.2M  0 part
```
4. You will see one disk, in my case "sdb" that is roughly the size of your USB Drive, note this down.
5. Locate the downloaded ISO e.g cd ~/Downloads
6. **Dangerous Step** This is where we **OVER-WRITE** the contents of your USB drive so please ensure you identified the CORRECT drive in lsblk above.
   My command would be below, however you will need to replace sde with the drive we located above
   ```
sudo dd if=Solus-Beta2.iso of=/dev/sdb bs=1M;sync
```
This will write the contents of the ISO to the thumb drive so you can boot it and also make sure the data is synchronised so you can eject the USB safely.
7. Reboot and select your USB Drive in your PC's boot menu (usually a function key like F10).
8. Enjoy!
