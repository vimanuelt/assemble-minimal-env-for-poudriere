assemble-minimal-env-for-poudriere
===============
Live media creator for GhostBSD distribution

## Introduction
The purpose of this tool is provide a GhostBSD environment for Poudriere.

## Features
* Build GhostBSD from packages
* Hybrid DVD/USB image

## System requirements
* Latest version of GhostBSD 
* 20GB of free disk space
* 4GB of free memory

Note: GhostBSD should be used to build ISO.

## Initial setup
Clone the repo:
```
git clone https://www.github.com/vimanuelt/assemble-minimal-env-for-poudriere.git
```
## Starting a build
#### Enter the directory for running the LiveCD build script:
```
cd assemble-minimal-env-for-poudriere
```

#### To build a GhostBSD bootable image (ISO) file
```
./build.sh -r release
```
or
```
./build.sh -r devel
```

## Burn an image to cd:
```
cdrecord /usr/local/ghostbsd-build/iso/GhostBSD-2020-08-02.iso
```

## Write an image to usb stick:
```
dd if=/usr/local/ghostbsd-build/iso/GhostBSD-2020-08-02.iso of=/dev/da0 bs=4m
```
