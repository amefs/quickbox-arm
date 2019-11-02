

![QB-arm](https://img.nyamoe.com/images/2019/09/22/quickbox-arm-logo.png)

# QuickBox-ARM

[English Ver](https://github.com/amefs/quickbox-arm/blob/master/README.md)

---

该项目是 QuickBox 社区版的 mod. 它的主要功能同 QuickBox Lite，不同的是该项目支持 armhf 构架。对于 aarch64 构架的平台，仅在运行 armhf 兼容系统时提供支持，若运行 arm64 系统，则需要 QuickBox ARM64(尚在开发)。

---

## 主要特性

1. 图形化的安装界面 (目前支持中英双语)
2. 使用 Nginx 替代 Apache
3. 模块化安装
4. 支持最新的 Debian 系系统
5. 最新的软件支持 (包含预编译的 deb 安装包)

---

## 当前版本

![Version](https://img.shields.io/badge/version-1.0.0%20beta-orange?style=flat-square)![GNU v3.0 License](https://img.shields.io/badge/license-GNU%20v3.0%20License-blue.svg?style=flat-square)

---

## 如何安装

### 安装须知

硬件需求:

- CPU: armhf 构架
- 内存: 大于 1GB (推荐使用更多内存)
- 硬盘: 20GB HDD 

系统支持 (仅支持 armhf):

![Ubuntu18.04](https://img.shields.io/badge/Ubuntu%2018.04-passing-brightgreen.svg?style=flat-square)![Ubuntu16.04](https://img.shields.io/badge/Ubuntu%2016.04-passing-brightgreen.svg?style=flat-square)![Debian9](https://img.shields.io/badge/Debian%209-passing-brightgreen.svg?style=flat-square)![Debian10](https://img.shields.io/badge/Debian%2010-passing-brightgreen.svg?style=flat-square)![Raspbian](https://img.shields.io/badge/Raspbian-passing-brightgreen.svg?style=flat-square)

服务器支持:

- 基于 armhf 构架的服务器或开发板

已测试平台:

- Banana-PI M2B/M2U/M3 (Ubuntu 16.04/Debian 9/Raspbian Stretch)
  - 提示：阅读[该教程](https://blog.nyamoe.com/2019/09/hoe-to-boot-bpi-m2u-m2b-up-from-sata-device/)了解如何从 SATA 设备启动系统
- Scaleway Baremetal C1 (Ubuntu 16.04/Debian 9)
- SoyouStart ARM 服务器 (Ubuntu 16.04/Debian 9)
  - 提示：阅读[该教程](https://github.com/amefs/quickbox-arm/wikis/%E5%9C%A8-SoyouStart-ARM-%E7%8B%AC%E6%9C%8D%E5%AE%89%E8%A3%85-QuickBox-ARM)了解如何在 SYS 安装该脚本

### 安装项目

**你需要首先以 root 身份登录**

**运行以下指令来抓取最新的代码 ...**

```
apt-get -yqq update; apt-get -yqq upgrade; apt-get -yqq install git lsb-release dos2unix; \
git clone https://github.com/amefs/quickbox-arm.git /etc/QuickBox; \
dos2unix /etc/QuickBox/setup.sh; \
bash /etc/QuickBox/setup.sh
```

### 如何直接安装开发者模式?

**在抓取源码时使用如下指令 ...**

```
mkdir /install/ && touch /install/.developer.lock; \
apt-get -yqq update; apt-get -yqq upgrade; apt-get -yqq install git lsb-release dos2unix; \
git clone --branch "development" https://github.com/amefs/quickbox-arm.git /etc/QuickBox; \
dos2unix /etc/QuickBox/setup.sh; \
bash /etc/QuickBox/setup.sh
```

### 已经安装 QuickBox 希望切换到开发者模式?

**运行如下指令以切换分支 ...**

```
mkdir /install/ && touch /install/.developer.lock; \
sudo box update quickbox
```

---

## 默认安装的功能

- pureftp - vsftp (FTP客户端)
- SSH Server
- Web 控制台 (Shellinabox)
- QuickBox 面板

---

## 可选的软件

### 安装时可选的软件

- rTorrent (*0.9.4-0.9.8*)
  - ruTorrent
  - flood
- Transmission (*2.94*)
- qBittorrent (*4.1.8*)
- Deluge (*1.3.15, 2.0.3*)
- mktorrent (可以使用 `createtorrent` 在命令行中使用表单快速创建种子)
- FFmpeg
- Linux RAR(仅限unrar)
- File Browser

### 面板中可选的软件

- Autodl-irssi
- BTSync
- FlexGet
- Netdata
- noVNC
- Plex
- Syncthing
- x2Go

### 命令行中可选的软件

- Denyhosts
- Fail2ban
- Let's Encrypt
- ZNC