---
layout: default
---

# Regolith Linux

Regolith is a polished, productivity-focused Ubuntu-based Linux distribution. It brings together a trifecta of [Ubuntu](https://www.ubuntu.com/)'s ubiquity, [i3wm](https://i3wm.org/)'s efficient and productive interface, and Gnome's [system configuration](https://gitlab.gnome.org/GNOME/gnome-control-center) features.

## What it Looks Like

Regolith is visually spartan by design.  It's meant to stay out of your way to prevent distraction.

TBD: Screenshots

## How to Get Regolith Linux

Regolith can be installed in two ways.  If you already have an existing Ubuntu setup, Regolith can simply be added as another desktop session by installing the metapackage `regolith-desktop` from the Regolith PPA.  If you'd like to start from scratch, download the Regolith Linux ISO and use the Ubuntu install wizard as you would a stock Ubuntu install.  Both approaches are equivelent, except that the LiveCD install does not contain the default Ubuntu UI.

### LiveCD Installer

The LiveCD can be downloaded here.  Write the file to a usb drive as you would any other Linux install image, and boot the drive in the PC that you wish to install to.  It works exactly as the stock Ubuntu installer.

### Ubuntu Metapackage PPA

From your existing Ubuntu 18.04 system, perform the following installation steps: 

1. Open a terminal, and enter: `sudo add-apt-repository -y ppa://kgilmer/regolith-stable`
2. After the sync completes, enter: `sudo apt install regolith-desktop`
3. Some packages will be installed.  When this completes, reboot.
4. At the login screen, select the "gear" icon and select `Regolith` from the list, and then login.

#### Uninstalling Regolith

To remove the Regolith Desktop from your existing Ubuntu system, first remove the package: `sudo apt remove regolith-desktop`.  Then remove the package archive reference: `sudo add-apt-repository --remove ppa://kgilmer/regolith-stable`.  After a reboot your system should be back to it's previous state.

#### Removing the Default Ubuntu Login Session

This step is entirely optional.  To remove the default "Ubuntu" login session, execute the following command in a terminal: `sudo apt remove ubuntu-session`.  This step can be reversed by reinstalling the same package.

## Menu

[Getting Started]({% link getting_started.md %})
[Internals]({% link internals.md %})
[Motivations]({% link motivations.md %})
[User Guide]({% link user_guide.md %})
[Resources]({% link resources.md %})
