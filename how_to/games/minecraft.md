# Minecraft

How to install Minecraft on Solus.

Grab the Java Run-time Environment here:
```
http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html
```

Extract JRE and move it to /opt:
```
cd ~/Downloads
tar xf jre-8u45-linux-x64.tar.gz
sudo mv jre1.8.0_45 /opt/
sudo ln -sv /opt/jre1.8.0_45/bin/java /usr/bin/java
```

Grab the Minecraft files and menu entry:
```
sudo mkdir -p /opt/Minecraft
sudo wget https://s3.amazonaws.com/Minecraft.Download/launcher/Minecraft.jar -O /opt/Minecraft/Minecraft.jar
sudo wget http://users.on.net/justin.zobel/minecraft -O /usr/bin/minecraft
sudo chmod +x /usr/bin/minecraft
sudo wget http://users.on.net/justin.zobel/minecraft.desktop -O /usr/share/applications/minecraft.desktop
```
