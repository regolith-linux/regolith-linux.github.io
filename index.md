---
layout: default
title: 
lang: en
---
Regolith Linux is a distro for people that prefer a spartan interface with polished and consistent system management. It brings together a trifecta of [Ubuntu](https://www.ubuntu.com/)'s ubiquity, [i3-wm](https://i3wm.org/)'s efficient and productive interface, and Gnome's [system configuration](https://gitlab.gnome.org/GNOME/gnome-control-center) features.

## What it Looks Like

<a href="/assets/screenshot-empty.png"><img class="screenshot" alt="Empty Desktop" src="/assets/screenshot-empty.png"/></a>

Regolith is visually spartan by design.  It's meant to stay out of your way to prevent distraction.  There are no icons, docks, panels, menus, widgets, or advertisements taking up screen space.  A small bar at the bottom of the screen shows valuable persistent information such as workspaces and volatile system status.

<a href="/assets/screenshot-apps.png"><img class="screenshot" alt="Tiled Windows" src="/assets/screenshot-apps.png"/></a>

Despite its minimal visual design, Regolith Linux provides modern system and file management features such as external monitor and storage management, wifi and bluetooth configuration, as well as language and privacy settings.

<a href="/assets/screenshot-rofi.png"><img class="screenshot" alt="Launch Apps" src="/assets/screenshot-rofi.png"/></a>

Quickly browse, search, and launch apps from the app launcher.  This modal menu can also be used to find and select windows across all of your workspaces.

<a href="/assets/screenshot-term.png"><img class="screenshot" alt="View Terminals" src="/assets/screenshot-term.png"/></a>

Because Regolith utilizes i3-wm for window management, you get more out of every pixel on your screen. Use more of it for what you care about, rather than sharing it with advertisements or features rarely used.

<a href="/assets/screenshot-nord.png"><img class="screenshot" alt="Nord" src="/assets/screenshot-nord.png"/></a>

Regolith is built to be customized.  Color, font, and theme information is defined in a single location: Xresources.  Change a color definition in one file, and have it be updated across all of your programs.  Here is Regolith with a user-contributed [Nord color scheme](https://github.com/arcticicestudio/nord) and the [Nordic GTK theme](https://github.com/EliverLara/Nordic).

## How to Get Regolith Linux

Regolith can be installed in two ways:  If you already have an existing Ubuntu setup, Regolith can simply be added as another desktop session by installing the package `regolith-desktop` from the [Regolith PPA](https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-stable).  If you'd like to start from scratch, download the Regolith Linux ISO and simply install Regolith [as you would stock Ubuntu](https://tutorials.ubuntu.com/tutorial/tutorial-create-a-usb-stick-on-ubuntu#0).  Both approaches are equivalent, except that the LiveCD does not contain the default Ubuntu UI.

### Option 1: LiveCD Installer

The Ubuntu-based LiveCD can be downloaded [from Source Forge](https://sourceforge.net/projects/regolith-linux/).  [Release 1](https://sourceforge.net/projects/regolith-linux/files/regolith-linux-r1/) is based on Ubuntu 18.04 and [release 1.1](https://sourceforge.net/projects/regolith-linux/files/regolith-linux-r1.1/) is based on Ubuntu 19.04, but either can be used to update to the latest updates.  [Write the file to a usb drive](https://tutorials.ubuntu.com/tutorial/tutorial-create-a-usb-stick-on-ubuntu#0) as you would any other Linux install image, and boot the drive in the PC that you wish to install to.  It works exactly as the [stock Ubuntu installer](https://tutorials.ubuntu.com/tutorial/tutorial-install-ubuntu-desktop#0).

### Option 2: Regolith Ubuntu PPA

From your existing Ubuntu 18.04 (Bionic), 18.10 (Cosmic), or 19.04 (Disco) system, perform the following installation steps: 

1. Open a terminal, and enter: <br/>`sudo add-apt-repository -y ppa:kgilmer/regolith-stable`
2. After the sync completes, enter: <br/>`sudo apt install regolith-desktop`
3. Some packages will be installed.  When this completes, reboot.
4. At the login screen, select the "gear" icon and select `Regolith` from the list, and then login.

<sub>If you encounter errors during step 2, please refer to the [troubleshooting page]({% link troubleshooting.md %}) for help.</sub>

#### Uninstalling Regolith

To remove the Regolith Desktop from your existing Ubuntu system, first remove the package: `sudo apt remove regolith-desktop`.  Then remove the package archive reference: `sudo add-apt-repository --remove ppa:kgilmer/regolith-stable`.  After a reboot your system should be back to it's previous state.

## Next Steps

Have a look at the [Getting Started]({% link getting_started.md %}) guide to learn more about using Regolith Linux, see the [latest updates]({% link news.md %}), or check out the [configuration]({% link configuring.md %}) page to learn about how to tweak it to your liking.  
