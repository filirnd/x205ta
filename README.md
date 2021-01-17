# Asus x205ta resources

[TOC]



## What is this ?

This resources help to install linux (in this case Xubuntu) on Asus x205ta and (if you want) installing i3 windows manager with my personal desktop style.
I choose xubuntu becouse is very lite, as opposed to ubuntu that is to heavy for this machine.
I using i3 as windows manager because is more easy and distraction free to have only 1/2 full screen windows with a 11.6 display.
Base Xfce is also good choose.


## Linux (Xubuntu) installation guide 

Installing a Linux distro on this netbook is not really easy, because normal distros missing a 32bit file (bootia32.efi) that this netbook need for starting a live usb distro.

This is the steps for installing xubuntu:

1. Download xubuntu (or other distro you like to install ) from his  repository (https://xubuntu.org/download/). I chose an LTS release.

2. Create a bootable USB with Rufus (or other software). I'm using Rufus (on windows) because i can choosing some boot settings. Parameters for creation must be the follow:

   - Partition Scheme: **GPT**
   - Target System: **UEFI(non CSM)**
   - Other parameters can remain as default

3. After USB creation you must copy the bootia32.efi file in "EFI/BOOT" directory. For Ubuntu (and derivates) you can download file from this repo resources ([bootia32.efi](https://github.com/filirnd/x205ta/blob/master/resources/bootia32.efi)). 
   For other distros you can simple search relative bootia32.efi file with a google search.

4. Insert the USB live on x205ta and power on the pc. Press many times F2 key as long as BIOS screen start. Then go to "Save & Exit" tab and choose your usb from "Boot Override" list. Press ENTER key and your distro will start.

5. Choose "Try Xubuntu" from boot menu. When you enter in live xubuntu start GPARTED and follow this steps:

   - Create new partition table in GPT and apply
   - Create efi partition (fat32) with a dimension of 550 MB (or similar) and apply
   - Set boot flag on this partition and apply

   After you apply all steps you can close GPARTED and click on "Install Xubuntu" on desktop.

6. You can now personalize your installation but you need to follow this steps for good installation:

   - Enable WiFi for install all software and drivers during the installation
   - Configuring partitions in manually mode. Select the efi partition that was created from GPARTED and edit "using as" setting as "UEFI system partition".
     Next you can create root partition or other partition scheme as you like
   - Before click the "INSTALL" button and starting the installation be sure to have selected entire disk as grub installation.



With Xubuntu 20.04 i don't have drivers issues (like wifi, touchpad) and function keyboards (like light or sound settings) works well.



This part of guide is an English translation of this Italian guide (https://forum.ubuntu-it.org/viewtopic.php?f=43&t=644049)





## Personal dotfiles

### TODO

.config


## Installed sw

### TODO



- i3: `sudo apt-get install i3`
- telegram (snap) : 
	`sudo snap install telegram-desktop`
- micro <file editor> (snap) : 
	`sudo snap install micro --classic`



