# Hackintosh macOS Sequoia on ThinkPad T470 🖥️🍎

![ThinkPad T470](https://github.com/jabaldoo/ThinkPad-t470-sequoia/blob/main/Photos/hackintosh.png)  

This repository contains the necessary files, configurations, and instructions to install macOS Sequoia on a Lenovo ThinkPad T470. This setup is intended for educational purposes and personal use. Please ensure you have a valid license for macOS before proceeding.

---

## Table of Contents
1. [Introduction](#introduction-)
2. [Hardware Specifications](#hardware-specifications-)
3. [Prerequisites](#prerequisites-)
4. [Installation Guide](#installation-guide-)
5. [Post-Installation](#post-installation-)
6. [What Works](#what-works-)
7. [What Doesn't Work](#what-doesnt-work-)
8. [Troubleshooting](#troubleshooting-)
9. [Screenshots](#screenshots-)
10. [Contributing](#contributing-)
11. [License](#license-)

---

## Introduction 📖
This guide will walk you through the process of installing macOS Sequoia on a Lenovo ThinkPad T470 using OpenCore or Clover bootloader. The goal is to achieve a stable and functional Hackintosh setup.

---

## Hardware Specifications 💻
| Component       | Details                                   |
|------------------|-------------------------------------------|
| **Model**        | Lenovo ThinkPad T470                      |
| **Processor**    | Intel Core i5-6300U                       |
| **Graphics**     | Intel HD Graphics 520                     |
| **RAM**          | 16GB DDR4                                 |
| **Storage**      | 512 GB NVMe                               |
| **Wi-Fi**        | Intel Wireless-AC 8265 (Replaced with compatible card) |
| **Ethernet**     | Intel I219-V                              |
| **Display**      | 14" FHD (1920x1080) IPS                   |
| **Audio**        | Realtek ALC298                            |

---

## Prerequisites 📋
Before starting, ensure you have the following:
- A compatible Wi-Fi card (e.g., Broadcom BCM94352Z or similar).
- A USB drive (16GB or larger).
- A working macOS environment (for creating the installer).
- A copy of macOS Sequoia (download from the App Store or other sources).
- OpenCore or Clover bootloader files (included in this repo).

---

## Installation Guide 🛠️
1. **Create macOS Installer**  
   Use `createinstallmedia` or a tool like [GibMacOS](https://github.com/corpnewt/gibMacOS) to create a bootable USB installer.

2. **Configure Bootloader**  
   Copy the provided EFI folder to the EFI partition of your USB drive.

3. **BIOS Settings**  
   - Disable Secure Boot.
   - Enable AHCI mode.
   - Set DVMT Pre-Allocated to 64MB or higher.

4. **Install macOS**  
   Boot from the USB drive and follow the on-screen instructions to install macOS.

5. **Post-Installation**  
   After installation, mount the EFI partition of your system drive and copy the EFI folder from the USB drive.

---

## Post-Installation 🎉
- **Wi-Fi and Bluetooth**: Use kexts or replace the Wi-Fi card with a compatible one.
- **Audio**: Use AppleALC.kext with the correct layout-id.
- **Trackpad**: Use VoodooPS2 or VoodooI2C kexts.
- **Power Management**: Use CPUFriend and CPUFriendDataProvider for better power management.

---

## What Works ✅
- [x] Audio (ALC id=13)
- [x] Ethernet
- [x] USB Ports
- [x] Trackpad and Keyboard
- [x] Sleep/Wake
- [x] Battery Status
- [x] Bluetooth
- [x] Wifi (but through itlwm.kext and heliport app)
- [x] SD Card Reader
- [x] HDMI (but only on HDMI port, no USB-C)
- [x] USB-C (only data transfer)

---

## What Doesn't Work ❌
- [ ] Built-in Camera
- [ ] Fingerprint Reader (unsupported)
- [ ] USB-C (partially working)

---

## Troubleshooting 🛑
- **No Bootable Device**: Ensure BIOS settings are correct and the USB drive is properly formatted.
- **Kernel Panics**: Check for incompatible kexts or incorrect configurations.
- **No Audio**: Look in Hackintool for your ALC id.
- **Wifi Wireless**: Use itlwm.kext and HeliPort app.

---

## Screenshots 📸
Here are some screenshots of the ThinkPad T470 running macOS Sequoia:  
*(Add your screenshots here with descriptions)*  
1. ![Screenshot 1](https://github.com/jabaldoo/ThinkPad-t470-sequoia/blob/main/Screenshots/Screenshot%202025-03-18%20at%2012.23.11.png)  
2. ![Screenshot 2](https://github.com/jabaldoo/ThinkPad-t470-sequoia/blob/main/Screenshots/Screenshot%202025-03-18%20at%2012.22.06.png) 
3. ![Screenshot 3](https://github.com/jabaldoo/ThinkPad-t470-sequoia/blob/main/Screenshots/20250318_202420.jpg)  

---

## Contributing 🤝
Contributions are welcome! If you have improvements or fixes, please open a pull request or issue.

---

## License 📜
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Useful Links 🔗
- [macOS Sequoia Official Page](https://www.apple.com/macos/sequoia)
- [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [OpenCore Official Website](https://opencore.slowgeek.com/)

---

**Disclaimer**: This project is for educational purposes only. I am not responsible for any damage to your hardware or software. Use at your own risk.