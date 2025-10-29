
<div align="center">

# ThinkPad T470 - macOS Sequoia Hackintosh

![macOS Sequoia on ThinkPad T470](https://github.com/jabaldoo/ThinkPad-t470-sequoia/blob/main/Photos/hackintosh.png)

**An OpenCore-based EFI configuration for running macOS Sequoia on the Lenovo ThinkPad T470.**

</div>

---

This repository provides a complete and stable EFI setup to help you run macOS Sequoia on a ThinkPad T470. (Sort of functional always sort of)

## 📋 Project Status

| Feature                 | Status | Notes                                            |
| ----------------------- | :----: | ------------------------------------------------ |
| **Audio**               |   ✅   | Realtek ALC298 (ALC id=13)                       |
| **Ethernet**            |   ✅   | Intel I219-V                                     |
| **Wi-Fi**               |   ✅   | Requires `itlwm.kext` + `HeliPort.app`           |
| **Bluetooth**           |   ✅   | Works natively.                                  |
| **USB Ports**           |   ✅   | All ports functional.                            |
| **Trackpad & Keyboard** |   ✅   | Full gesture support with VoodooI2C.             |
| **Battery Status**      |   ✅   | Fully working.                                   |
| **Sleep / Wake**        |   ✅   | Supported.                                       |
| **HDMI**                |   ✅   | Audio and video output.                          |
| **SD Card Reader**      |   ✅   | Working.                                         |
| **USB-C**               |   ⚠️   | Data transfer only. No video or charging.        |
| **Built-in Camera**     |   ❌   | Not functional.                                  |
| **Fingerprint Reader**  |   ❌   | ThinkPad doesnt have one.                    |

---

## Hardware Specifications

| Component        | Model                                   |
| ---------------- | --------------------------------------- |
| **CPU**          | Intel Core i5-6300U                     |
| **GPU**          | Intel HD Graphics 520                   |
| **RAM**          | 16GB DDR4                               |
| **Storage**      | 512GB NVMe SSD                          |
| **Wi-Fi/BT**     | Intel Wireless-AC 8265                  |
| **Display**      | 14" FHD (1920x1080) IPS                 |
| **Audio**        | Realtek ALC298                          |

---

## 🚀 Installation

### 1. Prerequisites
- A USB drive (16GB or larger).
- Access to a machine running macOS to create the installer.
- A genuine copy of macOS Sequoia.

### 2. Create macOS Installer
Use the official `createinstallmedia` command or a tool like [gibMacOS](https://github.com/corpnewt/gibMacOS) to create a bootable USB.

### 3. EFI Setup
- Mount the EFI partition of your USB drive.
- Clone this repository and copy the `Thinkpad_Sequoia_EFI` folder to the root of the EFI partition.

### 4. BIOS Configuration
- **Security -> Security Chip**: Disabled
- **Memory Protection -> Execution Prevention**: Enabled
- **Virtualization -> Intel Virtualization Technology**: Enabled
- **Internal Device Access -> Bottom Cover Tamper Detection**: Disabled
- **Anti-Theft -> Current Setting**: Disabled
- **Secure Boot -> Secure Boot**: Disabled
- **UEFI/Legacy Boot**: UEFI Only
- **CSM Support**: No

### 5. Install macOS
- Boot from the USB drive.
- At the OpenCore boot picker, select "Install macOS Sequoia".
- Follow the on-screen instructions.

### 6. Post-Installation
- After installation, mount your system drive's EFI partition.
- Copy the `Thinkpad_Sequoia_EFI` folder from your USB to the system's EFI partition to make the drive bootable.
- For Wi-Fi, install the `HeliPort.app` included in the `itlwm` release.

---

## 📸 Screenshots

<div align="center">

| Desktop | About This Mac |
| :---: | :---: |
| ![Desktop Screenshot](https://github.com/jabaldoo/ThinkPad-t470-sequoia/blob/main/Screenshots/Screenshot%202025-03-18%20at%2012.23.11.png) | ![About This Mac](https://github.com/jabaldoo/ThinkPad-t470-sequoia/blob/main/Screenshots/Screenshot%202025-03-18%20at%2012.22.06.png) |

</div>

---

## 🤝 Contributing
Feel free to contributte if you found some issues or kexts that can help with something else not listed in here

## 📜 License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 📚 Useful Resources
- [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [r/hackintosh Subreddit](https://www.reddit.com/r/hackintosh/)


