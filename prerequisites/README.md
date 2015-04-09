# Packaging documentation
### Preface

This documentation serves as a guide for those wishing to contribute to the Solus Project. Notablly it revolves around the topic of packaging.

### Expectations

It is assumed the user is experienced with the command line, and as such has at least a basic working knowledge of Linux or Unix-like systems.

# Prerequisites

To build packages for the Solus Operating System, you must first ensure your system is ready to do so.

### Build Types

Builds can be separated into two distinct categories, local native builds, or chroot builds. For local packaging needs it may be sufficient to use the build system directly, however it is recommeneded to use **evobuild** to build your packages in a clean chroot environment.

### Native Solus Operating System builds

To perform local native builds on Solus will require you to install many build dependencies, which may be undesirable if you do not routinely use these packages, for example for development work.

To enable this, at minimum you will be required to install the **system.devel** component:

```
sudo eopkg it -c system.devel
```

### Chroot builds, including foreign distributions

We provide the **evobuild** tool to enable clean chroot builds of Solus packages, which enables clean and controlled build of our packages not only on the Solus operating system, but on other Linux distributions too.

#### Requirements


* Modern kernel, with **overlayfs** enabled
* Root privileges (via sudo)
* A lot of disk space.
*

#### Installation of evobuild


Solus installations are already equipped with evobuild, thus no steps are required here.
Users of foreign distributions will need to install evobuild as follows:

```
wget https://raw.githubusercontent.com/solus-project/repository/master/system/base/pisi/files/evobuild.py
sudo mv evobuild.py /usr/local/bin/evobuild && sudo chmod +x /usr/local/bin/evobuild
```

The pythonic build system also requires pyyaml to operate.

### Configuring evobuild

Please proceed to the next section to see how to use evobuild.
