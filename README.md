<h1 align="center">
  <sub><sup><img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Telegram-Animated-Emojis/main/Activity/Sparkles.webp" alt="Sparkles" width="25" height="25"/></sup></sub> Arch Installation
  <sub><sup><img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Telegram-Animated-Emojis/main/Activity/Sparkles.webp" alt="Sparkles" width="25" height="25"/></sup></sub>
</h1>

<p align="center">
  <sub><sup><img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Telegram-Animated-Emojis/main/Activity/Sparkles.webp" alt="Sparkles" width="25" height="25"/></sup></sub>
    <a href="https://github.com/hey1me/ARCH_INSTALLATION/"><img src="https://img.shields.io/badge/Guide%20To%20Install-Arch-0092CD?style=for-the-badge&logo=archlinux&color=1793D1&logoColor=D9E0EE&labelColor=000000"/></a>
    <a href="https://github.com/hey1me/HEY_HyprArch/"><img src="https://img.shields.io/badge/HEY_HyprArch-Linux-0092CD?style=for-the-badge&logo=hyprland&color=58E1FF&logoColor=D9E0EE&labelColor=000000"/></a>
  <sub><sup><img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Telegram-Animated-Emojis/main/Activity/Sparkles.webp" alt="Sparkles" width="25" height="25"/></sup></sub>
</p>
<p align="center">
  <a href="https://hey1me.com"><img src="https://img.shields.io/badge/Hey1Me-Official%20Website-0092CD?style=for-the-badge&logo=linux&color=0092CD&logoColor=D9E0EE&labelColor=000000"/></a>
  <a href="https://www.youtube.com/@hey1me"><img src="https://img.shields.io/badge/Hey1me-YouTube-5865F2?style=for-the-badge&logo=youtube&color=FF0000&logoColor=D9E0EE&labelColor=000000"/></a>
  <a href="mailto:hey1me@protonmail.com"><img src="https://img.shields.io/badge/Hey1Me-Mail-5865F2?style=for-the-badge&logo=gmail&color=6D4AFF&logoColor=D9E0EE&labelColor=000000"/></a>
</p>

## 📋 Index:

‼️ Operation Will Wipe Your SSD/Storage Card
<br>
‼️ If your are looking for dual-boot OS, refer to other guide

- [Tools Requirement](https://github.com/hey1me/ARCH_INSTALLATION/#tools-requirement)
- [Arch Linux ISO File](https://github.com/hey1me/ARCH_INSTALLATION/#arch-linux-iso-file)
- [Boot Arch Live Step](https://github.com/hey1me/ARCH_INSTALLATION/#boot-arch-live-steps)
- **[In Arch Live Step](https://github.com/hey1me/ARCH_INSTALLATION/#in-arch-live)**
  - [Internet Connection](https://github.com/hey1me/ARCH_INSTALLATION/#internet-connection)
  - [Create Partitions](https://github.com/hey1me/ARCH_INSTALLATION/#create-partitions)
  - [Format Partitions](https://github.com/hey1me/ARCH_INSTALLATION/#format-partitions)
  - [Mount Partitions](https://github.com/hey1me/ARCH_INSTALLATION/#mount-partitions)
  - [Start ArchInstall](https://github.com/hey1me/ARCH_INSTALLATION/#start-archinstall)
- [After Boot Up](https://github.com/hey1me/ARCH_INSTALLATION/#after-boot-up)
- **[💫 HEY_HyprArch 💫](https://github.com/hey1me/ARCH_INSTALLATION/#-----hey_hyprarch-)**
  - [Install](https://github.com/hey1me/HEY_HyprArch)
- **[SUPPORT](https://github.com/hey1me/ARCH_INSTALLATION/#-----support-)**
  - [YouTube](https://www.youtube.com/@hey1me)
  - [Telegram](https://t.me/Hey_HyprArch)
  - [GumRoad](https://hey1me.gumroad.com/)
  - [Ko-Fi](https://ko-fi.com/hey1me)
  - [PayPal](https://paypal.me/TengQing1016)

### Tools Requirement

<details>
  <summary>Flash Drive</summary>
  
- `Recommended` - at least 2GB
</details>
<details>
  <summary>Devices</summary>
  
- `Processor` - x86_64 (64-bit) architecture
- `RAM` - At least 2 GB
- `Storage` - At least 20GB
- `Internet Connection`
</details>

### Arch Linux ISO File
[Download](https://geo.mirror.pkgbuild.com/iso/latest/)

### Boot Arch Live Steps
1. [Download](https://www.ventoy.net/en/download.html)
2. **In Ventoy App**
   - Select Your Flash Drive & ISO File
3. **Reboot Your Computer & Boot into Your BIOS/UEFI**
     - Don't have to unplug your Flash Drive
     - Google: 'Bios Key for [computer_manufacturer]'
     - Press & Hold The Key when booting computer
    - **For Windows OS**
      - Open Command Prompt as an administrator
      - Type the command `shutdown /r /fw` and press Enter
4. **In BIOS/UEFI**
    - **Method 1**
      - Disable 'Secure Boot' Mode
      - Choose Flash Drive as the first 'Boot Option'
      - Save Changes & Exit
      - Boot Computer
    - **Method 2** (HIGHLY RECOMMENDED)
      - Disable 'Secure Boot' Mode
      - Save Changes & Exit
      - Google: 'Boot Key for [computer_manufacturer]'
      - Press & Hold The Key when booting computer
5. **In Ventoy Bootloader**
    - Select Arch Linux ISO file
    - Boot 'Normal Mode'.
6. **In Arch Bootloader**
    - Select 'Boot Arch Linux (x86_64)'

### In Arch Live

#### Internet Connection
```bash
  ...
```

#### Create Partitions
1. ```bash
    fdisk -l
    cfdisk [partition you want to install Arch]
   ```
- **Example**
  - `cfdisk /dev/sda`

2. Select [Delete] Button. (Delete/Clear All)
3. **Select [New] Button to Create 2 partitions**
    - 1G [first partition]
    - (Choose Storage Size You Want/Recommended: All) [second partition]
    - (Recommend create Swap File instead of Swap Partition)
4. Select [Bootable] Button to Flag First Partition[1G]
5. **Use [Type] Button to Change**
    - [first partition] (fdisk: 'ef' Code)
    - [second partition] (fdisk: '83' Code)
6. **Select [Write] Button**
    - **Type:**
      - yes

#### Format Partitions
```bash
  mkfs.ext4 [second partition]
  mkfs.fat -F 32 [first partition]
```

#### Mount Partitions
```bash
  mount [second partition] /mnt
  mount --mkdir [first partition] /mnt/boot
```

#### Start ArchInstall
```bash
  archinstall
```
- Modify Options From Up to Down
- **Mirror**
  - Select Country (Nearest)
- **Disk Configuration**
  - Select [Pre-Mounted Configuration]
  - **Type:**
    - `/mnt`
- **Swap**
  - **Swap on zram**
    - Change to 'Disabled'
- **Authentication**
  - **Root Password**
    - [Enter Root/Admin Password]
  - **User Account**
    - [Add User]
    - Select 'Yes' to add into Sudoers File/List
- **Profile**
  - Select [Minimal]
- **Applications**
  - **Bluetooth**
    - 'Enabled'
  - **Audio**
    - Select [Pipewire]
- **Additional Packages**
  - Select [curl], [git]  (Use 'Tab' to Select, Type '/' to Search)
- **Network Configuration**
  - Select [Use NetworkManager]
- **Timezone**
  - Select [TimeZone]
- **Install**
  - Select [Yes]
- **After Completed**
  - Select [Reboot System]
  - (You can unplug your Flash Drive)

### After Boot-Up
- **Login**
  - Enter [Username]
  - Enter [Password]
- **Optional**
  - **Create Swap File**
    - ```bash
        sudo mkswap -U clear --size 4G --file /swapfile
        sudo swapon /swapfile
      ```
    - ```bash
        sudo bash -c 'cat >> /etc/fstab <<EOF
        /swapfile none swap defaults 0 0
        EOF'
      ```

      
   
<h2 align="center">
    💫 HEY_HyprArch 💫
</h2>

<div align="center">
    <a href="https://hey1me.com"><kbd> <br> Official Website <br> </kbd></a>&ensp;&ensp;
    <a href="https://ko-fi.com/album/HEYHyprArch-K3K61OMD0T"><kbd> <br> Gallery <br> </kbd></a>&ensp;&ensp;
    <a href="https://t.me/Hey_HyprArch"><kbd> <br> Telegram <br> </kbd></a>&ensp;&ensp;
</div>

- **Work Well With New & Advanced Users**
  - 💫 HEY_HyprArch is [Arch + Hyprland]
  - Good Customizations, Privacy & Secure, Easy-to-Use
  - Best for Daily Use & Gaming
  - Only Works for Arch Linux or any Arch Linux-based distros
- **Publish in April 2026**
  - [Install](https://github.com/hey1me/HEY_HyprArch)


<h2 align="center">
    💌 SUPPORT
</h2>

- Donate A 🌟 on my GitHub repos
- You can also support by ☕ or PayPal 💕

[![Ko-Fi](https://img.shields.io/badge/Ko--fi-F16061?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/hey1me)

or

[![PayPal](https://img.shields.io/badge/PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white)](https://paypal.me/TengQing1016)
