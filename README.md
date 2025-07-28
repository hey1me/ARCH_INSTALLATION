
## ARCH Installation GUIDE


![Logo](https://cdn0.iconfinder.com/data/icons/flat-round-system/512/archlinux-512.png)

### Visit ARCH OFFICIAL Download WebPage:
[ARCH_DOWNLOAD](https://geo.mirror.pkgbuild.com/iso/latest/)

Choose & Click The ISO File Format Name Like THIS:

[archlinux-yyyy.mm.dd-x86_64.iso]


#### Wait For The Installation Done — this may take a minute.


## After Download

Visit: 
[HOW_TO_CREATE_BOOTABLE_USB_FOR_ARCH_IN_WINDOWS](https://youtu.be/yYyh3PrIB7w?si=f7Ibs79C9I4M3u0P)

Watch Until 5:07 ONLY

## After Followed the Steps

### GUIDE:
Run:
`fdisk -l`

`fdisk /dev/sdX` (replace /dev/sdX by the partition you want to install ARCH)

#### # Delete If You Want to Clear The Chosen Partition:

`d` for delete partition, follow the instructions to delete partition.

Example: If want to delete 2 partitions, then two times of `d`.


#### # Create 3 Partitions:

`n`
Press Enter to 'Last Sector', Type: +1G, Press Enter Again.

`n`
Press Enter to 'Last Sector', Type: +6G, Press Enter Again.

`n`
Press Enter 3 times.


#### # Make Partition Bootable Flag:

`a` Type: 1, Press Enter.

#### # Change Type of Partitions:

`t` Type: 1, Press Enter, Type: ef, Press Enter.

`t` Type: 2, Press Enter, Type: 82, Press Enter.

#### # Save Changes:

`w`

### Format Partitions:

Run:

`mkfs.ext4 /dev/sdX3`

`mkfs.fat -F 32 /dev/sdX1`

`mkswap /dev/sdX2`

### Mount Partitions:

`mount /dev/sdX3 /mnt`

`swapon /dev/sdX2`

`mount --mkdir /dev/sdX1 /mnt/boot`


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
- Search: git
- Press 'Enter' for Select

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

#### Refer to [Install_HEY_Hypr_Arch](https://github.com/hey1me/HEY_Hypr_Arch) to Install HEY_Hypr_Arch Linux.