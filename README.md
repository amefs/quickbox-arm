

![QB-arm](https://img.nyamoe.com/images/2019/09/22/quickbox-arm-logo.png)

# Project QuickBox-ARM

[中文版](https://github.com/amefs/quickbox-arm/blob/master/README_zh.md)

---

This project is a modified version of QuickBox community edition. Most functions is the same as QuickBox Lite, but this project support armhf instead of x86_64. You can run this project in an aarch64 platform only in an armhf OS. You need QuickBox ARM64(Still in developing) to get full support of arm64 OS.

---

## Main feature

1. Graphical installation guide (Multi-language available)
2. Use nginx instead of apache
3. Modular installation
4. Latest OS support
5. up to date apps (include prebuild deb packages)

---

## Script status

![Version](https://img.shields.io/badge/version-1.0.0%20beta-orange?style=flat-square)![GNU v3.0 License](https://img.shields.io/badge/license-GNU%20v3.0%20License-blue.svg?style=flat-square)

---

## How to install

### before install

Hard ware requirement:

- CPU: armhf architecture
- RAM: large than 1GB (recommend more for better performance)
- Storage: 20GB HDD (for seeding, you need more)

OS Support (armhf only):

![Ubuntu18.04](https://img.shields.io/badge/Ubuntu%2018.04-passing-brightgreen.svg?style=flat-square)![Ubuntu16.04](https://img.shields.io/badge/Ubuntu%2016.04-passing-brightgreen.svg?style=flat-square)![Debian9](https://img.shields.io/badge/Debian%209-passing-brightgreen.svg?style=flat-square)![Debian10](https://img.shields.io/badge/Debian%2010-passing-brightgreen.svg?style=flat-square)![Raspbian](https://img.shields.io/badge/Raspbian-passing-brightgreen.svg?style=flat-square)

Server Support:

- Server/Development Boards  based on armhf

Tested Platform:

- Banana-PI M2B/M2U/M3 (Ubuntu 16.04/Debian 9/Raspbian Stretch)
  - Tips: See [this tutorial]( https://blog.nyamoe.com/2019/09/hoe-to-boot-bpi-m2u-m2b-up-from-sata-device/ ) to know how to boot from SATA device
- Scaleway Baremetal C1 (Ubuntu 16.04/Debian 9)
- SoyouStart ARM server (Ubuntu 16.04/Debian 9)
  - Tips: See [this tutorial](https://github.com/amefs/quickbox-arm/wikis/Install-QuickBox-ARM-in-SoyouStart-ARM) to know how to install quickbox arm in SYS

### install the project

**You must be logged in as root to run this installation.**

**Run the following command to grab our latest stable release ...**

```
apt-get -yqq update; apt-get -yqq upgrade; apt-get -yqq install git lsb-release dos2unix; \
git clone https://github.com/amefs/quickbox-arm.git /etc/QuickBox; \
dos2unix /etc/QuickBox/setup.sh; \
bash /etc/QuickBox/setup.sh
```

### Want to run in development mode?

**Run the following command to grab current development repos ...**

```
mkdir /install/ && touch /install/.developer.lock; \
apt-get -yqq update; apt-get -yqq upgrade; apt-get -yqq install git lsb-release dos2unix; \
git clone --branch "development" https://github.com/amefs/quickbox-arm.git /etc/QuickBox; \
dos2unix /etc/QuickBox/setup.sh; \
bash /etc/QuickBox/setup.sh
```

### Already have QuickBox installed and want to switch over to development?

**EASY! Run the following command to grab current development repos ...**

```
mkdir /install/ && touch /install/.developer.lock; \
sudo box update quickbox
```

---

## Installed Features

- pureftp - vsftp (CuteFTP multi-segmented download friendly)
- SSH Server (for SSH terminal and sFTP connections)
- Web Console (Shellinabox)
- QuickBox Dashboard

---

## Available software

### Available when setup

- rTorrent (*0.9.4-0.9.8*)
  - ruTorrent
  - flood
- Transmission (*2.94*)
- qBittorrent (*4.2.1*)
- Deluge (*1.3.15, 2.0.3*)
- mktorrent (with `createtorrent` command as wrapper)
- FFmpeg
- Linux RAR(unrar only)
- File Browser

### Available in dashboard

- Autodl-irssi
- BTSync
- FlexGet(both 2.x and 3.x)
- Netdata
- noVNC
- Plex
- Syncthing
- x2Go

### Available in CLI

- Denyhosts
- Fail2ban
- Let's Encrypt
- ZNC