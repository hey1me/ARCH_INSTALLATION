<h1 align="center">
  ARCH Installation
</h1>
<p align="center">
  <img src="https://img.shields.io/badge/Arch%20Linux-111111.svg?logo=archlinux"/>
</p>

## 📋 Index:

‼️ Operation Will Wipe Your SSD/Storage Card
<br>
‼️ If your are looking for dual-boot OS, refer to other guide

- [Tools Requirement](https://github.com/hey1me/ARCH_INSTALLATION/#tools-requirement)
- [Arch Linux ISO File](https://github.com/hey1me/ARCH_INSTALLATION/#arch-linux-iso-file)
- [Boot Arch Live Step](https://github.com/hey1me/ARCH_INSTALLATION/#boot-arch-live)
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
- **Flash Drive**
  - Recommended at least 2GB
- **Devices**
  - Processor: x86_64 (64-bit) architecture
  - RAM: At least 2 GB
  - Storage: At least 20GB
  - Internet Connection

### Arch Linux ISO File
[Download](https://geo.mirror.pkgbuild.com/iso/latest/)

### Boot Arch Live
1. [Download](https://www.ventoy.net/en/download.html)
2. **In Ventoy App**
   - Select Your Flash Drive & ISO File
3. **Restart Your Computer & Boot into Your BIOS/UEFI**
     - Don't have to unplug your Flash Drive
     - Google: 'Boot Key for [computer_manufacturer]'
     - Press & Hold The Key when booting computer
    - **For Windows OS**
      - Open Command Prompt as an administrator
      - Type the command `shutdown /r /fw` and press Enter
4. **In BIOS/UEFI**
    - **Method 1**
      - Disable 'Secure Boot' Mode
      - Choose Flash Drive as the first 'Boot Option'
      - Save Changes & Exit
    - **Method 2**
      - Disable 'Secure Boot' Mode
      - Save Changes & Exit
      - Press 
5. Turn On Your Computer
6. **In Ventoy Bootloader**
    - Select Arch Linux ISO file
    - Boot 'Normal Mode'.
7. **In Arch Bootloader**
    - Select 'Boot Arch Linux (x86_64)'

### In Arch Live

#### Internet Connection
```bash
  ...
```

#### Create Partitions
1. ```bash
    fdisk -l`
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
    - [first partition] 'ef' Code
    - [second partition] '83' Code
6. **Select [Write] Button**
    - **Type:**
      - yes

#### Format Partitions
```bash
  mkfs.ext4 [third partition]
  mkfs.fat -F 32 [first partition]
```

#### Mount Partitions
```bash
  mount [third partition] /mnt
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
- **Root Password**
  - [Enter Root/Admin Password]
- **User Account**
  - [Add User]
  - Select 'Yes' to add into Sudoers File/List
- **Profile**
  - Select [Minimal]
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
    <a href="https://(HEY_HyprArch Website)"><kbd> <br> Official Website <br> </kbd></a>&ensp;&ensp;
    <a href="https://(HEY_HyprArch FAQ)"><kbd> <br> FAQ <br> </kbd></a>&ensp;&ensp;
    <a href="https://(HEY_HyprArch Gallery)"><kbd> <br> Gallery <br> </kbd></a>&ensp;&ensp;
    <a href="https://t.me/Hey_HyprArch"><kbd> <br> Telegram <br> </kbd></a>&ensp;&ensp;
</div>

- **Work Well With New & Advanced Users**
  - 💫HEY_HyprArch is [ARCH + HYPRLAND].
  - Focus On User-friendly, Privacy & Security.
  - Best for General & Gaming Purposes!
  - Only Support in ARCH LINUX.
- **Publish in April 2026**
  - [Install](https://github.com/hey1me/HEY_HyprArch)


<h2 align="center">
    💌 SUPPORT 💌
</h2>

- Donate A 🌟 on my GitHub repos
- Subscribe My YouTube Channel 🎬 [YouTube](https://www.youtube.com/@hey1me)
- Join My Telegram Channel [Telegram](https://t.me/Hey_HyprArch)
- Check Out GumRoad [GumRoad](https://hey1me.gumroad.com/)
- You can also support by ☕ or PayPal 💕

[![Ko-Fi](https://img.shields.io/badge/Ko--fi-F16061?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/hey1me)

or

[![PayPal](https://img.shields.io/badge/PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white)](https://paypal.me/TengQing1016)
