[Implicit Lazy Writer] Installation Guide of Microsoft Surface Pro 3 with Ubuntu 16.04 (amd64)
===========================================

#### Table of contents
1. [Specification & Essential Config](#specification)
2. [Peripheral Requirement](#peripheral-requirements)


------------------------------------

## Specification

Microsoft Surface Pro 3 **(Core i7, 512GB SSD, 8GB of Ram)** with Windows 10 installed

> - Secure boot = **[enabled]**
> - Bitlocker = **[disabled]**

## Peripheral Requirements

Mandatory

>  1. 8GB USB at least

Optional

>  1. USB Keyboard
>  2. USB 3 Hub
>  3. Ethernet Adapter

## Software Requirements

 1. Download Unetbootin for windows https://unetbootin.github.io/
 2. Download Ubuntu 16.04 LTS https://www.ubuntu.com/download/desktop


## Installation step

 1. Shrink the space for at least +50gb **(Do not format it first)**
 2. Burn the **Ubuntu iso** through **unetbootin** to your **USB**
 3. Click it http://lmgtfy.com/?q=Disable+bitlocker+in+windows+10
 4. Reboot, press and hold **Volume Down ** then **Power button** just once
 5. You are supposed to see GRUB bootloader, choose **Without installing** so u can make use of onscreen keyboard and so on
 6. Use your **Common sense** to do it manually, not recommended step.
 7. You are supposed to be in partitioning step after clicking few *next* installation button by touching your finger to the screen
 8. Uncheck **third party installation**, it gonna make the process longer, we can do this later.
 8. Partitioning set after you are in Live Ubuntu USB
	 7. Split
	 8. and
	 8. Format as :
	 8. **Filesystem** Linux Swap (**Recommended size:** 1:1 to your RAM, if you have 8GB of ram make it 8GB).
	 9. **Filesystem:** ext4 **Mount:** / **My Size: 20-30GB**
	 10. **Filesystem:** ext4 **Mount:** /home **My Size: 50-70GB**
	 11. **Filesystem:** ext4 **Mount:**/boot **My Size: 900mb**
 9. Use **Common Sense** again until you finish the installation
 10. Reboot

What to do next ? (TypeCover support)
--
 1. Find **system settings** by your finger, on top right of the screen
 2. **Universal Access** > **Typings** > Turn on **On screen keyboard**
 3. Find **Terminal** and Open it
 4. Type as listed below as the terminal opened

> sudo add-apt-repository ppa:tigerite/kernel

> sudo apt-get update

> sudo apt-get upgrade

> sudo apt-get install linux-surface

> sudo apt-get dist-upgrade

> reboot

---

## Starter-kit packages

 - sudo apt-get install terminator
 - sudo apt-get install i3
 - sudo apt-get install i3blocks
 - sudo apt-get install zsh

## i3 Window Manager Essential
 - sudo apt-get install scrot (Screenshot with i3)
 - sudo apt-get install pavucontrol (Volume control)
 - sudo apt-get install feh (Image Viewer)

## Configuration, Shell and else
 - [oh-my-zsh!](https://github.com/robbyrussell/oh-my-zsh)

## Development-kit packages
 - [Node Version Manager](https://github.com/creationix/nvm)( Node Essential )
 - [Ruby Version Manager](https://rvm.io/) ( Ruby Essential )
 - [GitKraken](https://www.gitkraken.com/) ( Pretty good for staging a hunk, clean commit but resource intensive for SP3 )
 - sudo apt-get install git
 - sudo apt-get install ubuntu-make

## Ruby Development with i3wm
**(Not yet)**

## Known Problems
 - Chrome Screen flickering  ( Fixed by installing Microsoft HD5000 driver with little bit of hax )
 - Atom Screen flickering ( Fixed by installing Microsoft HD5000 driver with little bit of hax )
 - WiFi/Ethernet connection eventually broke (Fixed by installing driver)
 > git clone git://git.marvell.com/mwifiex-firmware.git

 > mkdir -p /lib/firmware/mrvl/

 > cp mwifiex-firmware/mrvl/* /lib/firmware/mrvl/

 > reboot

 - Sound stuttering (only with i3 Windows Manager)
