**English** | [中文](README_CN.md)

<div align="center">
<img src="https://img14.360buyimg.com/n0/jfs/t1/122699/10/10858/75075/5f4708e1Eb80b55c6/f276218d450b6840.jpg" width="350px">
</div>

# ThinkpadX390-Opencore-EFI

## Intro
 **This includes an EFI(Opencore) which works perfectly on Thinkpad-X390.**
 
## Download
**You can click this button or turn to the "Releases" page yourself and download the latest version [![Download from https://github.com/mendax955/ThinkpadX390-Opencore-EFI/releases](https://img.shields.io/github/downloads/mendax955/ThinkpadX390-Opencore-EFI/0.6.5/total?style=plastic)](https://github.com/mendax955/ThinkpadX390-Opencore-EFI/releases)**

## Disclaimer

Your warranty is now void. Please do some research if you have any concerns before replacing your EFI with mine. I am not responsible for any loss, including but not limited to Kernel Panic, device fail to boot or can not function normally, storage damage or data loss, atomic bombing, World War III, Google and Apple both go into liquidation, and so on.

## ThinkPad X390 Hackintosh

macOS Catalina/Big Sur on ThinkPad X390 (Hackintosh).

### Tested on:

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

## Devices

| Specifications | Details |
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


## What is working

#### CPU

Functioning normally.Frequency conversion is normal.

#### Battery

The power display is functioning normally.

#### USB

USB Ports Patching with HackinTool, `5 Gbps` for USB 3.0 (Dev Speed).

#### Ethernet

Functioning normally.

#### Display

The model of Integrated Graphics is `Intel UHD Graphics 620`, faked to `Intel UHD Graphics 630 (Mobile) `.

The HDMI is attached with `Intel UHD Graphics 620` and is functioning normally. `2K@60Hz` & `4K@30Hz` are supported.

#### Audio

Driven by AppleALC with `layout-id: 11`. Everything is working normally.

#### Keyboard

Functioning normally except the <kbd>Insert</kbd> , which is not presented on Magic Keyboard.And <kbd>Alt</kbd> represents Window's <kbd>Ctrl</kbd>.

#### SSD

NVMe is functioning normally and TRIM is enabled for it.

#### Bluetooth

Functioning normally.

#### Trackpad & Trackpoint

Functioning normally. Trackpoint and UltraNavs are working properly as well.

#### Wireless Card

Functioning part normally.**Credit  [@zxystd's AirportItlwm](https://github.com/OpenIntelWireless/itlwm)**


## What is not working

- Airdrops and Handoff Fail to work properly.

## Recommended BIOS Config

> Make sure you have disabled Windows login password before entering the BIOS, because you might not be able to login with "PIN" on Windows after configuring your BIOS as following.

- Security
  - Intel SGX: Software Controlled
- Boot
  - Boot Mode: UEFI Only

## Tips

### Hibernation

Hibernation is supported.

### Audio Issue

If you have faced some strange issue (like audio device is not found) after booting from Windows to macOS, you should reboot back to Windows and has a cold reboot (shutdown then start up) back to macOS. After that your audio device should be back.

> If you are using Parallel Desktop with Boot Camp mode on your hacintosh, you should not reboot directly in macOS for the same reason. You should manually shutdown Windows in Parallel Desktop, and then have your macOS cold rebooted (shutdown then start up).

## Further more help
  - For further learning please turn to http://bbs.pcbeta.com/viewthread-1852139-1-1.html

## Questions and Issues
  - If you have any questions,just push your issues on the Github , maybe l will help you!
  - Or If you have other questions or feedback, feel free to [![Gitter](https://badges.gitter.im/ThinkPad-Hackintosh-Opencore/ThinkPad-Hackintosh.svg)](https://gitter.im/ThinkPad-Hackintosh-Opencore/ThinkPad-Hackintosh?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge) [![Join the chat at https://gitter.im/ThinkpadX390-Opencore-EFI/community](https://badges.gitter.im/ThinkpadX390-Opencore-EFI/community.svg)](https://gitter.im/ThinkpadX390-Opencore-EFI/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
  
## Credits
  - [@zxystd](https://github.com/zxystd) for [itlwm](https://github.com/OpenIntelWireless/itlwm)
  - [@Acidanthera](https://github.com/acidanthera) for basic kexts.
  - [@BAndysc](https://github.com/BAndysc) for [Trackpoint and UltraNavs drive](https://github.com/BAndysc/VoodooPS2/tree/master)
  - [@SukkaW](https://github.com/SukkaW) for [Text and Templates](https://github.com/SukkaW/ThinkPad-E480-Hackintosh)
