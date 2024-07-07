<div align="center">
<img width="768" src="https://cdn.jsdelivr.net/gh/haiibo/OpenWrt/images/openwrt.png"/>

# Action Openwrt 云自动编译
⏰ **每周自动拉取最新源码自动编译**

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
</div>

<br />

<p align="center">

  <h3 align="center">Openwrt/LEDE 云编译(带应用商店)</h3>
  <p align="center">
    👉 每周定时自动拉取Openwrt最新源码编译，自动发布到 [<a herf="https://github.com/dreamskr/OpenWrts/releases"> Releases </a>]👈
    <br />
    <br />
    <a href="https://github.com/dreamskr/OpenWrts/releases">下载地址</a>
    ·
    <a href="https://github.com/dreamskr/OpenWrts/actions">Action</a>
    ·
    <a href="https://github.com/dreamskr/OpenWrts/issues">提出新特性</a>
  </p>

</p>

## 目录

- [Action Openwrt 云自动编译](#action-openwrt-云自动编译)
  - [目录](#目录)
  - [支持的设备](#支持的设备)
    - [🎯固件默认设置](#固件默认设置)
  - [固件特性](#固件特性)
  - [自带插件](#自带插件)
  - [文件目录说明](#文件目录说明)
  - [定制固件](#定制固件)
    - [注意事项](#注意事项)
  - [固件预览](#固件预览)
  - [版权说明](#版权说明)
  - [项目支持](#项目支持)
  - [Stargazers over time](#stargazers-over-time)

<br>


## 支持的设备
🎯 带应用商店的固件：`x86Lite`
|           支持的设备        |         固类别         |        Action         |            状态          |              下载页          |
| :------------------------: | :---------------------: | :-------------------: | :-------------------: | :--------------------------: |
|             x86_64                    |  [LEDE](https://github.com/coolsnowwolf/lede) |[🍕](https://github.com/dreamskr/OpenWrts/actions/workflows/x86_64.yml) | ![x86_64](https://github.com/dreamskr/openwrts/actions/workflows/x86_64.yml/badge.svg) |  [✔](https://github.com/dreamskr/OpenWrts/releases) |
| x86_64Lite | [LEDE](https://github.com/coolsnowwolf/lede) |[🍕](https://github.com/dreamskr/OpenWrts/actions/workflows/x86_64Lite.yml) | ![x86_64Lite](https://github.com/dreamskr/openwrts/actions/workflows/x86_64Lite.yml/badge.svg) | [✔](https://github.com/dreamskr/OpenWrts/releases) |
|             树莓派 2B             | [LEDE](https://github.com/coolsnowwolf/lede) | [🍕](https://github.com/dreamskr/OpenWrts/actions/workflows/RaspberryPi2.yml) | ![RaspberryPi3](https://github.com/dreamskr/openwrts/actions/workflows/RaspberryPi2.yml/badge.svg) | [✔](https://github.com/dreamskr/OpenWrts/releases) |
|             树莓派 3B/3B+             | [LEDE](https://github.com/coolsnowwolf/lede) | [🍕](https://github.com/dreamskr/OpenWrts/actions/workflows/RaspberryPi3.yml) | ![RaspberryPi3](https://github.com/dreamskr/openwrts/actions/workflows/RaspberryPi3.yml/badge.svg) | [✔](https://github.com/dreamskr/OpenWrts/releases) |
|             树莓派 4B             |  [LEDE](https://github.com/coolsnowwolf/lede) | [🍕](https://github.com/dreamskr/OpenWrts/actions/workflows/RaspberryPi4.yml) | ![RaspberryPi4](https://github.com/dreamskr/openwrts/actions/workflows/RaspberryPi4.yml/badge.svg) |  [✔](https://github.com/dreamskr/OpenWrts/releases) |
|             树莓派 5             |  [LEDE](https://github.com/coolsnowwolf/lede) | [🍕](https://github.com/dreamskr/OpenWrts/actions/workflows/RaspberryPi5.yml) | ![RaspberryPi5](https://github.com/dreamskr/openwrts/actions/workflows/RaspberryPi5.yml/badge.svg) |  [✔](https://github.com/dreamskr/OpenWrts/releases) |
|             NanoPi R2S             |  [LEDE](https://github.com/coolsnowwolf/lede) | [🍕](https://github.com/dreamskr/OpenWrts/actions/workflows/Rockchip_armv8.yml) | ![R2S](https://github.com/dreamskr/openwrts/actions/workflows/Rockchip_armv8.yml/badge.svg) | [✔](https://github.com/dreamskr/OpenWrts/releases) |
|             NanoPi R4S             |  [LEDE](https://github.com/coolsnowwolf/lede) | [🍕](https://github.com/dreamskr/OpenWrts/actions/workflows/Rockchip_armv8.yml) | ![R4S](https://github.com/dreamskr/openwrts/actions/workflows/Rockchip_armv8.yml/badge.svg) | [✔](https://github.com/dreamskr/OpenWrts/releases) |
|             NanoPi R5C             |  [LEDE](https://github.com/coolsnowwolf/lede) | [🍕](https://github.com/dreamskr/OpenWrts/actions/workflows/Rockchip_armv8.yml) | ![R5C](https://github.com/dreamskr/openwrts/actions/workflows/Rockchip_armv8.yml/badge.svg) | [✔](https://github.com/dreamskr/OpenWrts/releases) |
|             NanoPi R5S             |  [LEDE](https://github.com/coolsnowwolf/lede) | [🍕](https://github.com/dreamskr/OpenWrts/actions/workflows/Rockchip_armv8.yml) | ![R5S](https://github.com/dreamskr/openwrts/actions/workflows/Rockchip_armv8.yml/badge.svg) | [✔](https://github.com/dreamskr/OpenWrts/releases) |
|             FastRhino R68S             |  [LEDE](https://github.com/coolsnowwolf/lede) | [🍕](https://github.com/dreamskr/OpenWrts/actions/workflows/Rockchip_armv8.yml) | ![R68S](https://github.com/dreamskr/openwrts/actions/workflows/Rockchip_armv8.yml/badge.svg) | [✔](https://github.com/dreamskr/OpenWrts/releases) |
|             Orange Pi R1 Plus             |  [LEDE](https://github.com/coolsnowwolf/lede) | [🍕](https://github.com/dreamskr/OpenWrts/actions/workflows/Rockchip_armv8.yml) | ![OrangePiR1](https://github.com/dreamskr/openwrts/actions/workflows/Rockchip_armv8.yml/badge.svg) | [✔](https://github.com/dreamskr/OpenWrts/releases) |

<br>

### 🎯固件默认设置
- 路由器地址: `192.168.10.1`
- 默认用户名: `root`
- 默认密码  : `password`

<br>

## 固件特性
⏰ 固件编译改为`周更`(稳定为主，减少资源浪费)

✨ iStore应用商店 [AppStore](./assets/images/appstore.png)

✨ 自带常用的插件

✨ Arm集成所有openwrt的USB驱动

✨ ~~集成Python3.x(带pip)环境~~

✨ 集成Docker-CE

✨ ~~集成Node.js(14.xLTS 带npm、yarn)~~

✨ 全新的 [Them](https://github.com/jerrykuku/luci-theme-argon)

✨ x86_64 vmdk固件集成vm-tools

✨ x86_64 iso格式镜像

✨ x86_64 Lite版本(必要插件&应用商店)

<br>

## 自带插件
🍕 默认插件
- PassWall2 / SSR Plus
- AdGuard Home
- Mentohust
- ~~luci-app-vssr~~
- luci-adbyby-plus
- luci-app-unblockmusic
- luci-app-ddns
- luci-app-pushbot (全能推送)
- luci-app-onliner
- luci-app-ttyd
- luci-app-turboacc
- luci-app-upnp
- luci-app-netdata
- luci-usb-printer
- luci-app-nps
- luci-app-frpc
- luci-app-n2n
- luci-app-syncdial (多播插件)
- luci-app-turboacc
- luci-app-kms
- luci-app-docker
- luci-app-serverchan
- luci-app-control-timewol (定时wol唤醒)
- luci-app-aliyundrive-webdav (阿里云盘)
- luci-app-filebrowser
- luci-app-nfs   
......

<br>

## 文件目录说明

```
filetree
├── .github/workflows
│  ├── Rockchip_armv8.yml
│  ├── RaspberryPi2.yml
│  ├── RaspberryPi3.yml
│  ├── RaspberryPi4.yml
│  ├── RaspberryPi5.yml
│  ├── x86_64.yml
│  ├── x86_64Lite.yml
│  ├── update-checker.yml
├── /configs/ (配置文件目录)
│  ├── LuciApp.config (插件配置文件)
│  ├── LuciApp_Lite.config (简洁配置文件)
│  ├── RPi2.config
│  ├── RPi3.config
│  ├── RPi4.config
│  ├── RPi5.config
│  ├── x86_64.config
│  ├── Rockchip.config
├── configure.sh (固件参数修改)
├── package.sh (luci-app)

Tips:
x86.conf | RPi4.config - 该类型配置文件主要为机型配置文件
LuciApp.conf / LuciApp_Lite.conf - 主要用于配置固件插件应用 
```
<br>

## 定制固件
1. Fork 此项目
2. 按需修改 ```configure.sh``` 和 ```package.sh``` 文件
3. 上传你自己的 ```xx.config``` 配置文件到configs目录
4. 添加或修改自己的``````xx.yml``````文件
5. 最后根据个人喜好修改 ```update-checker.yml``` 需自行添加 ```Actions secrets``` (触发自动编译)

### 注意事项：
📌 修改默认系统参数 👉 ```configure.sh```   
📌 添加其它Luci插件 👉 ```package.sh```   
📌 插件 / 应用配置文件 👉 ```configs/LuciApp.config```   
<br>

## 固件预览
<details>
<summary><b>&nbsp;ARMv8 盒子 Mini 精简版本插件预览</b></summary>
  
**主界面(主题一)：**
![主界面](./assets/images/openwrt.png)

**应用商店/插件**
![应用商店/插件](./assets/images/appstore.png)

**服务/插件：**
![服务/插件](./assets/images/service.png)

**网络：**
![网络](./assets/images/network.png)

**经典主题二：**
![登录页](./assets/images/infinityfreedom-theme.png)

**主界面：**
![主界面](./assets/images/infinityfreedom-theme-main.png)

</details>


## 项目参考
- [1.markdown折叠风格、自动编译](https://github.com/haiibo/OpenWrt)
- [2.电视盒子自动编译](https://github.com/ophub/amlogic-s9xxx-openwrt)
- [3.luci-theme-argon](https://github.com/jerrykuku/luci-theme-argon)
- [4.istore](https://github.com/linkease/istore)



## 其它教程
[![电视盒子专用：利用Flippy内核工具打包，将OpenWrt固件转成img镜像文件，](https://res.cloudinary.com/marcomontalbano/image/upload/v1692927730/video_to_markdown/images/youtube--EPNsHRj3eXE-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://youtu.be/EPNsHRj3eXE "电视盒子专用：利用Flippy内核工具打包，将OpenWrt固件转成img镜像文件，")

