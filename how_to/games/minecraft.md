# Minecraft

How to install Minecraft on Solus.

Grab the Java Run-time Environment here:
```
http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html
```

Extract JRE and move it to /opt:
```
cd ~/Downloads
tar xf jre-8u40-linux-x64.tar.gz
sudo mv jre1.8.0_40 /opt/
sudo ln -s /opt/jre1.8.0_40/bin/java /usr/bin/java
```

Grab the Minecraft files and menu entry:
```
sudo mkdir /opt/Minecraft
sudo wget https://s3.amazonaws.com/Minecraft.Download/launcher/Minecraft.jar -O /opt/Minecraft/Minecraft.jar
sudo wget http://users.on.net/justin.zobel/minecraft -O /usr/bin/minecraft
sudo chmod +x /usr/bin/minecraft
sudo wget http://users.on.net/justin.zobel/minecraft.desktop -O /usr/share/applications/minecraft.desktop
```

You know have a Minecraft Entry in Budgie Menu and you can run it from any terminal by typing:
```
minecraft
```
