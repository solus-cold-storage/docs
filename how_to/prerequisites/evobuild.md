# evobuild

### Configuring the packager information

When building Solus's **package.yml** format packages, you will need to provide packager information. Thus, we must provide this information in ```$HOME/.evolve-os/packager```, i.e. your real name and email address:


```
[Packager]
Name=Ikey Doherty
Email=ikey@some-domain.tld
```

### Initialising the build system

To first use evobuild, you must seed it with a prebuilt Solus Operating System base image. This will fetch the compressed root file system and decompress it for local use:

```
sudo evobuild init
```

### Updating evobuild

As time goes by, the base builder image can become out of date. Each time we build a package using evobuild, we use a temporary root (via **overlayfs**) to intialise the build environment. Any changes made during this time do not affect the base image we have.

If you find that many packages are being updated during build, you can simply update it as follows:

```
sudo evobuild update
```

