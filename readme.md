[![preview image](https://github.com/Zxce3/next-theme/blob/main/preview.png)](https://www.deviantart.com/sdbinwiiexe/art/rEFInd-Next-Theme-407754566)
## rEFInd Next theme

[rEFInd](http://www.rodsbooks.com/refind/) is a simplistic boot manager for UEFI
based systems. This is a clean and minimal theme for it.

I Just re-upload from
![rEFInd Next](http://sdbinwiiexe.deviantart.com/)

### Usage

To use this theme you'll want to clone it into the same directory as your rEFInd
efi executable (usually `/boot/EFI/refind/`). Then you will want to add the following line to the end of your `refind.conf`:
	include next-theme/theme.conf


To set the appropriate background image, edit the “theme.conf” file in TextEdit and change the banner line to direct to whichever image file corresponds to your mac’s native resolution.
E.g. If your native resolution is 1440x900, you’d change the line to the following:
	banner next-theme/background_900.png

To make an icon appear when loading using graphical boot, open boot_bg.png file in your image editor of choice, and just copy the operating system’s os_ icon over top of the background.  Then save the new image using the boot_ prefix.  A few examples have been included (windows, linux, ubuntu, linux mint, unknown)

To set the icons for your entries you will want to add the `icon` configuration
to each menuentry which points to the icon under `next-theme/icons` that you
would like to use for that entry.

Here's an example configuration:

```shell
menuentry "Arch Linux" {
	icon /EFI/refind/next-theme/icons/os_arch.png
	loader vmlinuz-linux
	initrd initramfs-linux.img
	options "ro root=UUID=dfb2919d-ff78-48db-a8a7-23f7542c343a loglevel=3"
}

menuentry "Windows" {
	icon /EFI/refind/next-theme/icons/os_win.png
	loader /EFI/Microsoft/Boot/bootmgfw.efi
}

menuentry "OSX" {
	icon /EFI/refind/next-theme/icons/os_mac.png
	loader /EFI/Apple/Boot/bootmgfw.efi
}
```

Entries that are autodetected should also show the proper icons.

# Description
This description from devian art pages

As I plan on setting up a triple boot on my computer once the new versions of Windows, OS X, and Linux become released, I decided an update to my rEFIt/rEFInd boot screen was in order. This theme is inspired by both iOS 7 and Windows 8 interfaces.

rEFIt's development has been halted for a while now; a maintained for of it called rEFInd is available as a suggested replacement.

I created the theme using current themes/guides as a base, but have not thoroughly tested it. If there are any issues, please let me know and I'll see what I can do. Instructions for how to set up the theme are in the package, as well as instructions for how to set up OS-specific icon profiles (useful for linux distros).

The theme contains icons for the following operating systems:
 - macOS (OS X)
 - Windows 7 and older
 - Windows 8 and newer
 - Chrome OS
 - FreeBSD
 - Arch Linux
 - Android
 - Antergos
 - CentOS
 - Debian
 - Deepin
 - Elementary OS
 - Fedora
 - Kali Linux
 - Linux Mint
 - Mageia
 - Manjaro
 - Mandriva
 - NetBoot/iPXE
 - OpenSUSE
 - PC Linux OS
 - Puppy Linux
 - Red Hat
 - Sabayon
 - Slackware
 - Solus
 - Steam OS
 - Ubuntu Flavours
     - Ubuntu
     - Xubuntu
     - Lubuntu
     - Kubuntu
     - Edubuntu
     - Ubuntu Studio
     - Ubuntu Mate
     - Ubuntu Budgie
 - Zorin
 - General Linux Distributions (Generic Tux)
 - Legacy Operating Systems (Generic Icon)
 - General Other/Unknown

# Change Log

## February 10, 2018
 - Added Netboot (both tool and os icons)

## August 7, 2017
 - Added Ubuntu Flavours
	- Xubuntu
	- Lubuntu
	- Kubuntu
	- Edubuntu
	- Ubuntu Studio
	- Ubuntu Mate
	- Ubuntu Budgie
- Added Antergos
- Added CentOS
- Added Deepin
- Added Zorin
- Added Solus

## June 23, 2017

- Added new Elementary os and boot icons
- Renamed previous thin elementary icons to elementary_alt

## April 4, 2015

- Added Android icon (os_android.png) for Android_x86 users

## February 10, 2015

- Copied os_win.png to os_win8.png for compatibility with rEFInd 0.8.6

## October 22, 2014:

- Changed Kali icon to a thicker, more basic variation of the logo
- Added alternate (traditional) Linux Mint logo

## May 26, 2014:

- Linux OS/boot icons changed to a tux variation
- Shell tool icon added
- Renamed backtrack icons to kali

## December 25, 2013:

- Windows and Linux Mint icons have been downscaled slightly to be more visually appealing.
- Several boot icons have been included for graphical boot (notes have been added to the readme file for how to create additional boot icons).
- Added resolution-scaled backgrounds.  Simply designate the background corresponding to your mac's native resolution (as discussed in the readme file).
