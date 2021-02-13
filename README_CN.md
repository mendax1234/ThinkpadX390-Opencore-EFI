[English](README.md) | **中文**

[![Download from https://github.com/mendax955/ThinkpadX390-Opencore-EFI/releases](https://img.shields.io/github/downloads/mendax955/ThinkpadX390-Opencore-EFI/total?label=Download)](https://github.com/mendax955/ThinkpadX390-Opencore-EFI/releases) [![Gitter](https://badges.gitter.im/ThinkpadX390-Opencore-EFI/Hackintosh-ThinkPad.svg)](https://gitter.im/ThinkpadX390-Opencore-EFI/Hackintosh-ThinkPad?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge) [![GitHub issues](https://img.shields.io/github/issues-raw/mendax1234/ThinkpadX390-Opencore-EFI?label=Open%20issues)](https://github.com/mendax1234/ThinkpadX390-Opencore-EFI/issues) [![GitHub pull requests](https://img.shields.io/github/issues-pr/mendax1234/ThinkpadX390-Opencore-EFI?label=Pull%20requests)](https://github.com/mendax1234/ThinkpadX390-Opencore-EFI/pulls)

[Detailed Support](https://github.com/mendax1234/Pi-introduction)

<div align="center">
<img src="https://img14.360buyimg.com/n0/jfs/t1/122699/10/10858/75075/5f4708e1Eb80b55c6/f276218d450b6840.jpg" width="350px">
</div>

# ThinkpadX390-Opencore-EFI

# 目录

- [介绍](#介绍)
- [下载](#下载)
- [声明](#声明)
- [ThinkPad X390 Hackintosh](#ThinkPad-X390-Hackintosh)
  - [测试过的系统](#测试过的系统)
- [设备](#设备)
- [正常工作的部分](#正常工作的部分)
  - [详细的设备驱动情况](#详细的设备驱动情况)
- [已知的问题](#已知的问题)
- [推荐的BIOS配置](#推荐的BIOS配置)
- [补充](#补充)
- [更多帮助](#更多帮助)
- [疑问](#疑问)
- [鸣谢](#鸣谢)

## 介绍

**这包括一个EFl(Opencore)，它在Thinkpad-X390上工作完美**

## 下载

**你可以按下此按钮 [![GitHub release (latest by date)](https://img.shields.io/github/v/release/mendax1234/ThinkpadX390-Opencore-EFI)](https://github.com/mendax955/ThinkpadX390-Opencore-EFI/releases) 或者转到"Releases"界面去下载最新版本的EFI**

## 声明

你的保修单现在无效了。如果你有任何顾虑，请在我的 EFI 取代你的 EFl 之前做一些研究。我不负责任何损失，包括但不限于内核恐慌，设备无法启动或不能正常工作，存储损坏或数据丢失，原子弹爆炸，第三次世界大战，谷歌和苹果都倒闭，等等

## ThinkPad-X390-Hackintosh

可以完美地在ThinkPad X390上安装*Catalina/Big Sur*或者任何之前的版本，如*Mojave , High Sierra , Sierra , EI Captain , Yosemite , Mavericks ……*

### 测试过的系统

**Catalina**
- 10.15.2
- 10.15.3
- 10.15.4
- 10.15.5
- 10.15.6
- 10.15.7

**Big Sur**
- 11.0.1
- 11.1
- 11.2
- 11.2.1

## 设备

| 名称 | 细节 |
|:---|:---|
| Computer Model | ThinkPad X390 (39CD) |
| CPU | Intel Core i5-8265U |
| Mainboard |  Lenevo 20Q00039CD（I/O - 9D84 for mobile 8th Gen Intel Core processor family） |
| Displayer | Lenevo LEN4094 ( 13.3 inch  ) |
| Memory | DDR4 2667 Mhz. Onboard 8 GB |
| NVMe SSD | WDC PC SN730 SDBQNTY-256G-1001 (256G/SSD) |
| Integrated Graphics | Intel UHD Graphics 620 |
| Ethernet |  Intel(R) Ethernet Connection (6) I219-V |
| Sound Card | Realtek High Defination Audio@Intel Intel Smart Sound Technology Audio Controller (layoutid:11) |
| Wireless Card |  Intel(R) Wireless-AC 9560 160MHz |


## 正常工作的部分

### 详细的设备驱动情况

#### CPU

功能正常。变频正常。

#### 电池

电池电量显示正常。

#### 以太网

功能正常。

#### 显卡

集成显卡的型号是`Intel UHD Graphics 620`，仿冒`Intel UHD Graphics 630 (Mobile) `
HDMI与`Intel UHD Graphics 620` 连接，功能正常。支持`2K@60Hz` & `4K@30Hz` 。

#### 声卡

用AppleALC正常驱动`layout-id: 11`. 一切功能都正常。

#### 键盘

功能正常，除了 <kbd>Insert</kbd>，Magic Keyboard上没有。<kbd>Alt</kbd> 表示Windows上的<kbd>Ctrl</kbd>。

#### 硬盘

NVMe 功能正常并且开启了TRIM.

#### 蓝牙

功能正常。

#### 触控板和小红点

功能正常。Trackpoint和ultranav也工作正常

#### 无线网卡

功能部分正常.**感谢  [@zxystd's AirportItlwm](https://github.com/OpenIntelWireless/itlwm)**

#### 内置摄像头

已使用正确的USBInjectAll.kext完美驱动，功能正常。


## 已知的问题

- 隔空投送和接力无法正常工作

## 推荐的BIOS配置

>在进入BIOS之前，请确保您已经禁用了Windows登录密码，因为在按照以下方式配置BIOS后，您可能无法在Windows上使用“PIN”登录。

- Security
  - Intel SGX: Software Controlled
- Boot
  - Boot Mode: UEFI Only

## 补充

### 睡眠

睡眠完美支持。

### 声卡方面的疑问解答

如果你在从Windows启动到macOS后遇到了一些奇怪的问题(比如找不到音频设备)，你应该重启回到Windows，并进行冷重启(先关机再启动)回到macOS。在那之后你的音频设备应该回来了。

> 如果你在你的Hacintosh上使用带有Boot Camp模式的并行桌面，你不应该在macOS中直接重启
> 同样的原因。您应该在并行桌面中手动关闭Windows，然后重新启动macOS(先关闭再启动)。

## 更多帮助
  - 如需了解更多，请移步 [远景论坛]( http://bbs.pcbeta.com/viewthread-1852139-1-1.html) & [CSDN](https://blog.csdn.net/weixin_45498173/article/details/113092016)

## 疑问
  - 如果你有任何问题，尽管在Github上提出来，也许我会帮助你!
  - 或者你有其他别的问题，欢迎在[![Gitter](https://badges.gitter.im/ThinkpadX390-Opencore-EFI/Hackintosh-ThinkPad.svg)](https://gitter.im/ThinkpadX390-Opencore-EFI/Hackintosh-ThinkPad?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)上提出！
  - 我们只接受在GitHub issues的bug报告，在打开一个issue之前，建议您在[Gitter](https://gitter.im/ThinkpadX390-Opencore-EFI/Hackintosh-ThinkPad?utm_source=share-link&utm_medium=link&utm_campaign=share-link)上与我们重新确认它
  
## 鸣谢
  - [Apple](https://www.apple.com) for [macOS](https://www.apple.com/macos)
  - [@zxystd](https://github.com/zxystd) for developing [itlwm](https://github.com/OpenIntelWireless/itlwm)
  - [@Acidanthera](https://github.com/acidanthera) for basic kexts.
  - [@BAndysc](https://github.com/BAndysc) for [Trackpoint and UltraNavs drive](https://github.com/BAndysc/VoodooPS2/tree/master)
  - [@SukkaW](https://github.com/SukkaW) for [Text and Templates](https://github.com/SukkaW/ThinkPad-E480-Hackintosh)
