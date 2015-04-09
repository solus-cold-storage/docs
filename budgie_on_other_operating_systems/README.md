# Budgie on other Operating Systems
####Ubuntu 15.04
- Ubuntu isn't officially supported so your results may vary
- This was done from Ubuntu Gnome 15.04 ISO
- Please ensure you have universe enabled in your sources list for mutter.
- This only works on Ubuntu 15.04 as it's the only one that has a new enough mutter.
- It could be possible to compile mutter on older Ubuntu versions.
- Install a theme other than Adwaita etc. Maybe even EvoPop https://github.com/poltertec/evopop-gtk-theme

````
sudo apt-get update && sudo apt-get dist-upgrade
sudo apt-get install build-essential python2.7 gnome-common gobject-introspection libglib2.0-dev libgtk-3-dev libpulse-dev libpulse-mainloop-glib0 libmutter-dev libwnck-3-dev libupower-glib-dev libgnome-menu-3-dev libc6-dev libpeas-dev libgee-dev libgee-0.8-dev valac git
git clone https://github.com/evolve-os/budgie-desktop.git
cd budgie-desktop
./autogen.sh --prefix=/usr
make;sudo make install
````


####Debian 8 (Jessie)
- This assumes you already have A desktop environment installed and a login manager.
- From Debian Jessie netinst ISO:
````
sudo apt-get update;sudo apt-get upgrade -y
sudo apt-get install build-essential gnome-common gobject-introspection libglib2.0-dev libgtk-3-dev libpulse-dev libpulse-mainloop-glib0 libmutter-dev libwnck-3-dev libupower-glib-dev libgnome-menu-3-dev libc6-dev libpeas-dev libgee-dev libgee-0.8-dev valac git -y
git clone https://github.com/evolve-os/budgie-desktop.git;cd budgie-desktop;./autogen.sh --prefix=/usr;make;sudo make install
````
Now you should be able to select Budgie from your login manager e.g GDM/lightdm

####Arch
AUR packages

Stable:
```
https://aur.archlinux.org/packages/budgie-desktop/
```
Git:
```
https://aur.archlinux.org/packages/budgie-desktop-git/
```

####Fedora 20, 21 & OpenSUSE
On OpenSUSE's Software Portal
```
http://software.opensuse.org/download.html?project=home%3Aikeydoherty%3Aevolve&package=budgie-desktop
```
