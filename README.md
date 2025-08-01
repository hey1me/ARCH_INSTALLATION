
## ARCH Installation GUIDE


![Logo](https://cdn0.iconfinder.com/data/icons/flat-round-system/512/archlinux-512.png)


### Index

- [Arch ISO File Download](https://github.com/hey1me/ARCH_INSTALLATION/blob/main/README.md#visit-arch-official-download-webpage)
- [After Download & How to Boot into Arch Live ISO](https://github.com/hey1me/ARCH_INSTALLATION/blob/main/README.md#after-download)
- [Choose And Create Partition For Arch](https://github.com/hey1me/ARCH_INSTALLATION/blob/main/README.md#after-followed-the-steps)
- [Format Partition of Arch Linux](https://github.com/hey1me/ARCH_INSTALLATION/blob/main/README.md#format-partitions)
- [Mount The Partition](https://github.com/hey1me/ARCH_INSTALLATION/blob/main/README.md#mount-partitions)
- [Enter User-Friendly ArchInstall](https://github.com/hey1me/ARCH_INSTALLATION/blob/main/README.md#enter-arch-installation)
- [Guide For ArchInstall](https://github.com/hey1me/ARCH_INSTALLATION/blob/main/README.md#guide-1)
- [Install HEY_Hypr_Arch For Your Arch Linux](https://github.com/hey1me/ARCH_INSTALLATION/blob/main/README.md#after-installed)


### Visit ARCH OFFICIAL Download WebPage:
[ARCH_DOWNLOAD](https://geo.mirror.pkgbuild.com/iso/latest/)

Choose & Click The ISO File Format Name Like THIS:

[archlinux-yyyy.mm.dd-x86_64.iso]


#### Wait For The Installation Done — this may take a minute.


## After Download

Visit: 
[HOW_TO_CREATE_BOOTABLE_USB_FOR_ARCH_IN_WINDOWS_And_Boot into Arch LiveISO](https://youtu.be/yYyh3PrIB7w?si=f7Ibs79C9I4M3u0P)

Watch Until 5:07 ONLY

## After Followed the Steps

### GUIDE:
Run:
`fdisk -l`

`cfdisk [the partition]` (Example: `cfdisk /dev/sda` )

#### # Delete If You Want to Clear The Chosen Partition:

Use [Delete] Button.

(Double Check If you has choose correct partition For install Arch Linux)


#### # Create 3 Partitions:

Use [New] Button to Create:

- 1G  [first partition]

- 6G (You can Choose 1-6 by yourself, if you know what is this for)   [second partition]

- (the rest of space)   [third partition]


#### # Make Partition Bootable Flag:

Use [Bootable] Button to Flag First Partition [1G]


#### # Change Type of Partitions:

Use [Type] to Make:

- [first partition] 'ef' Code    (first partition)

- [second partition] '82' Code    (second partition)

- [third partition] '83' Code     (third partition)


#### # Save Changes:

Use [Write] Button, Type: yes, Press 'Enter'


### Format Partitions:

Run:

`mkfs.ext4 [third partition]`

`mkfs.fat -F 32 [first partition]`

`mkswap [second partition]`


### Mount Partitions:

`mount [third partition] /mnt`

`swapon [second partition]`

`mount --mkdir [first partition] /mnt/boot`


## Enter Arch Installation:

`archinstall`

### Guide:

- Modify Options From Up to Down

##### Mirror: Choose Your Country. 
- IF Don't Have Your Country, Choose Nearby Country.

##### Disk Configuration:
- Choose Pre-Mounted Configuration
- Type: /mnt

##### Root Password:
- Set Your Own.

##### User Account:
- Follow instructions to add A User
- 'Yes' to Add To Sudoers File/List.

##### Profile:
- Choose: Minimal

##### Audio:
- Choose: Pipewire

##### Additional Packages:
- (For Enter Search)Type: /
- Search: curl
- Press 'Tab' (Select)
- Search: git
- Press 'Enter' (Select and Exit)

##### Network Configuration:
- Select: Use NetworkManager

##### Timezone:
- (For Enter Search)Type: /
- Search: [Your TimeZone]
- Press 'Enter' for Select

## !!! Last !!!

#### Go to 'Install', Press Enter.

#### Select 'Yes', Press Enter Again.

### 
- Wait For Finish Installation.

## After Installed

### Select 'Reboot System'

#### Now, You can Unplug Your Flash Drive.

#### And, Your will Enter to Login Page.

### After Login:

#### Refer to [Install_HEY_Hypr_Arch](https://github.com/hey1me/HEY_HyprArch) to Install HEY_Hypr_Arch Linux. (Developing, Estimated will be published in March 2026)

#### Thanks For Supporting My Projects. Follow to Avoid Miss Out More Projects.
