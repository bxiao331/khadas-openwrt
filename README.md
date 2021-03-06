# khadas openwrt [![Build Status](https://travis-ci.com/hyphop/khadas-openwrt.svg?branch=master)](https://travis-ci.com/hyphop/khadas-openwrt)

openwrt for Khadas VIMs boards https://www.khadas.com/vim (Amlogic s905 s912 a311D s905d3 )
and Edge boards https://docs.khadas.com/edge/ (RockChip rk3399 )

![khadas vims openwrt](pics/khadas_vim_openwrt.jpg)

## Change logs

+ [README.changes.md](README.changes.md)

## supported Boards

+ [khadas VIM1](https://docs.khadas.com/vim1/) - OK
+ [khadas VIM2](https://docs.khadas.com/vim2/) - OK
+ [khadas VIM3](https://docs.khadas.com/vim3/) - OK
+ [khadas VIM3L](https://docs.khadas.com/vim3/#VIM3L) - OK
+ [khadas Edge](https://docs.khadas.com/edge) - OK

## Build

```
git clone https://github.com/hyphop/khadas-openwrt.git
cd khadas-openwrt

# ./scripts/build_prepare      # if some tools missed
# ./build_prepare_from_sources # if some tools missed or wrong 

# build usage examples

## build openwrt for VIM1
./scripts/build -1  
## build openwrt for VIM2
./scripts/build -2  
## build openwrt for VIM3
./scripts/build -3  
## build openwrt for VIM3L
./scripts/build -3l 
## build openwrt for Edge
./scripts/build -e  
#
./scripts/build -emmc -3l # build openwrt for VIM3L emmc image
#
./scripts/build -2 +server # build openwrt server variant for VIM2
#
echo REL=18.06.4 > scripts/build.conf.user # build openwrt 18.06.4 series
./scripts/build -r -2
#
echo REL=19.07.3 > scripts/build.conf.user # build openwrt 19.07.0 series
./scripts/build -r -2
#

```

## Images

+ https://github.com/hyphop/khadas-openwrt/releases/
+ https://dl.khadas.com/Firmware/VIM1/OpenWrt
+ https://dl.khadas.com/Firmware/VIM2/OpenWrt
+ https://dl.khadas.com/Firmware/VIM3/OpenWrt
+ https://dl.khadas.com/Firmware/VIM3L/OpenWrt
+ https://dl.khadas.com/Firmware/Edge/OpenWrt

## Installation

just write iamge to SD card

```
cd /tmp
wget https://github.com/hyphop/khadas-openwrt/releases/download/0.1/VIM1.OPENWRT.sd.img.gz || \
wget https://dl.khadas.com/Firmware/VIM1/OpenWrt/VIM1.OPENWRT.sd.img.gz
gzip -dc VIM1.OPENWRT.sd.img.gz | sudo dd bs=1M of=/dev/SD_PATH
sync
```

## install to emmc inside openwrt booted from sd

    root@openwrt:/# mmc_install_from_sd

## docs & how to

+ [files/docs](files/docs)
+ [README.openwrt.vims.md](README.openwrt.vims.md)

## related projects

+ https://github.com/hyphop/khadas-linux-kernel
+ https://github.com/hyphop/khadas-uboot
+ https://github.com/hyphop/khadas-rescue
+ https://github.com/hyphop/khadas-rescue-tools

## links

+ https://openwrt.org/
+ https://www.khadas.com/vim
+ https://docs.khadas.com/edge/
+ https://github.com/khadas
+ https://docs.khadas.com
