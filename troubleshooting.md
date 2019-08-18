---
layout: page
title: Troubleshooting
---

This page contains information that may help if you encounter an issue with Regolith Linux. If your problem isn't already here, you can join the [Slack channel](https://regolith-linux.herokuapp.com/) to ask, or kindly [file an issue](https://github.com/regolith-linux/regolith-desktop/issues) and describe your problem.

# Update

## Lost Configuration Changes

If you've just updated Regolith and have lost any customizations to i3-wm, Rofi, i3bar, Conky, or i3blocks, this is due to a new versioning scheme.  Initially, config files were copied from a common location into your user directory upon new session creation.  However, some recent backwards-incompatable changes to support easier theming were introduced.  In order to prevent bugs of running the old configuration files, but not delete users custom files, the i3 configuration file is referenced by the package version.  So, what was `~/.config/i3-regolith/config` is now `~/config/i3-regolith/config-4.16-1ubuntu18ppa10`.  Additionally, the i3blocks (forked to i3xrocks) now lives in `~/.config/i3xrocks/i3xrocks.conf`.  To restore your configuration, simply add your changes into these new files.  Breaking changes are expected infrequently, and will be announced beforehand via the [Regolith Linux Announcements mailing list](https://www.freelists.org/list/regolith-linux).  If your customizations involve color, typeface, or gtk theme, have a look at the new [Xresources-based customization documentation](https://regolith-linux.org/configuring.html) before merging your changes.

# Installation

## PPA

### [Package Conflicts](#package-conflict)
Regolith is installed using Debian packages. By design, a package will fail to install if by installing it would overwrite existing files on your system.  So, if you have already installed (either via package or compiled from sources) i3-wm, rofi, gnome-flashback, or compton, you will not be able to install Regolith without moving or removing them.  To remove them, run `sudo make uninstall` from the source directory, or use `sudo apt remove <package>` for non-Regolith debian packages.  Once removed try installing `regolith-desktop` again.

### [add-apt-repository command not found](#add-apt-repoistory)
If `add-apt-repository` is not installed, you may have to install `software-properties-common`. See [this stack overflow page](https://askubuntu.com/questions/493460/how-to-install-add-apt-repository-using-the-terminal) for more detail.

# Usage

## [Keybinding to toggle horizontal/vertical window layout doesn't work.](#layout-keybinding)

The keybinding `⊞ Win`-`backspace` toggles the layout mode for the current workspace, and will change the layout for the __next__ window opened on that workspace.  Toggling the layout by itself will not change anything on screen, but will effect how the next window is added to the workspace.
