# Candyhouse Routers

_Candyhouse_ is the codename for the Cisco board that powers the Cisco/Linksys EA4500, E4200v2, and EA3500 WiFi routers.  

## Building OpenWRT images

Build OpenWRT firmware images with minimal ROOter extensions for EA4500 / E4200v2
```bash
$ make viper
```
Build OpenWRT firmware images with minimal ROOter extensions for EA3500
```bash
$ make audi
```

The included [Makefile](Makefile) will clone OpenWRT trunk, and build a bin file for the EA4500 / E4200v2 / EA3500. It also adds ROOter addons (which are useful for 3G/4G USB modems), so just comment out the .openwrt_rooter target if you don't want those installed. 

A tar file is also created to allow system upgrades from an older flashed version (to maintain config).

For more info and discussion about OpenWRT on Candyhouse routers, please see the discussions [here](http://www.wolfteck.com/projects/candyhouse/openwrt/):

For more info and discussion about ROOter OpenWRT extensions, please visit:

[http://ofmodemsandmen.com](http://ofmodemsandmen.com)

## Returning to the stock firmware for reflashing

You can flash the original Linksys stock firmware from within the OpenWRT interface.

## Building / Installing Modules

No need.  All required functions are built into the kernel image.  No more mounting your router FS to you build box!

## Cleaning Up

```bash
$ make clean
```

This will remove all of the status files, the patchlog, the image, the downloaded kernel source and its extracted tree.
