---
layout: page
title: Install
lang: de
---

Regolith can be installed in two ways:  If you already have an existing Ubuntu setup, Regolith can simply be added as another desktop session by installing the package `regolith-desktop` from the [Regolith PPA](https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-stable).  If you'd like to start from scratch, download the Regolith Linux ISO and simply install Regolith [as you would stock Ubuntu](https://tutorials.ubuntu.com/tutorial/tutorial-create-a-usb-stick-on-ubuntu#0).  Both approaches are equivalent, except that the LiveCD does not contain the default Ubuntu UI, but also some branding such as login screen changes not present in the PPA release.

Another option if you'd like to learn more about Regolith without installing it; the ISO, when booted from USB, can boot into a live environment.  This can be achieved by selecting "Try Regolith" from the boot menu when booting from the 1.2 Release ISO.

### Option 1: LiveCD Installer

The Ubuntu-based LiveCD can be downloaded [from Source Forge](https://sourceforge.net/projects/regolith-linux/).  [Release 1](https://sourceforge.net/projects/regolith-linux/files/regolith-linux-r1/) is based on Ubuntu 18.04 and [release 1.2](https://sourceforge.net/projects/regolith-linux/files/regolith-linux-r1.2/) is based on Ubuntu 19.04, but either can be used to update to the latest updates.  [Write the file to a usb drive](https://tutorials.ubuntu.com/tutorial/tutorial-create-a-usb-stick-on-ubuntu#0) as you would any other Linux install image, and boot the drive in the PC that you wish to install to.  It works exactly as the [stock Ubuntu installer](https://tutorials.ubuntu.com/tutorial/tutorial-install-ubuntu-desktop#0).

### Option 2: Regolith Ubuntu PPA

From your existing Ubuntu 18.04 (Bionic) or 19.04 (Disco) system, perform the following installation steps: 

1. Open a terminal, and enter: <br/>`sudo add-apt-repository -y ppa:kgilmer/regolith-stable`
2. After the sync completes, enter: <br/>`sudo apt install regolith-desktop`
3. Some packages will be installed.  When this completes, reboot.
4. At the login screen, select the "gear" (⚙️) icon and select `Regolith` from the list, and then login.

<sub>If you encounter errors, please refer to the [troubleshooting page]({% link troubleshooting.md %}) for help.</sub>

## Uninstallation of `regolith-desktop`

If Regolith is not for you, simply follow these steps to remove it from your system:

1. Log out of the Regolith session and into the default Ubuntu session.
2. Open a terminal and run: <br/>`sudo apt remove regolith-desktop regolith-st && sudo apt autoremove` 
3. Now remove the PPA:  <br/>`sudo add-apt-repository --remove ppa:kgilmer/regolith-stable`
4. To restore your GNOME settings, run: <br/>`source ~/.regolith-gnome-backup`
5. You can safely delete `~/.config/regolith`.
