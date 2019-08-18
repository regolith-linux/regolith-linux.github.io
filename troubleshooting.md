---
layout: page
title: Troubleshooting
---

This page contains information that may help if you encounter an issue with Regolith Linux. If your problem isn't already here, you can join the [Slack channel](https://regolith-linux.herokuapp.com/) to ask, or kindly [file an issue](https://github.com/regolith-linux/regolith-desktop/issues) and describe your problem.

# Update

## [Lost Configuration Changes](#where-is-config)

If you've just updated Regolith and have lost any customizations to i3-wm, Rofi, i3bar, Conky, or i3blocks, this is due to a new versioning scheme.  Initially, config files were copied from a common location into your user directory upon new session creation.  However, some recent backwards-incompatable changes to support easier theming were introduced.  In order to be more consistent with where Linux expects config files to be, they have moved to `/etc/regolith/`.  To make modifications, copy the file you wish to modify to your user directory first.  Here are the steps to copy default configurations to your user directory where you can make edits:

### i3 Config
```
$ mkdir -p ~/.config/regolith/i3
$ cp /etc/regolith/i3/config ~/.config/regolith/i3/config
```
Now you can edit `~/.config/regolith/i3/config` and reload i3 to see your changes.

### Xresources
```
$ cp /etc/regolith/styles/root ~/.Xresources-regolith
```
Now you can edit `~/.Xresources-regolith`.  To see your changes, log back in to your session.

### i3xrocks (i3blocks)
Edit your i3 configuration file, changing this line:
```
  status_command i3xrocks -c /etc/regolith/i3xrocks/config
```

To:
```
  status_command i3xrocks -c ~/.config/regolith/i3xrocks/config
```

And now copy the file there:
```
$ mkdir -p ~/.config/regolith/i3xrocks
$ cp /etc/regolith/i3xrocks/config ~/.config/regolith/i3xrocks/
```
Now edit `~/.config/regolith/i3xrocks/config` and reload i3 to see your changes.

# Installation

## PPA

### [Package Conflicts](#package-conflict)
Regolith is installed using Debian packages. By design, a package will fail to install if by installing it would overwrite existing files on your system.  So, if you have already installed (either via package or compiled from sources) i3-wm, rofi, gnome-flashback, or compton, you will not be able to install Regolith without moving or removing them.  To remove them, run `sudo make uninstall` from the source directory, or use `sudo apt remove <package>` for non-Regolith debian packages.  Once removed try installing `regolith-desktop` again.

### [add-apt-repository command not found](#add-apt-repoistory)
If `add-apt-repository` is not installed, you may have to install `software-properties-common`. See [this stack overflow page](https://askubuntu.com/questions/493460/how-to-install-add-apt-repository-using-the-terminal) for more detail.

# Usage

## [Keybinding to toggle horizontal/vertical window layout doesn't work.](#layout-keybinding)

The keybinding `⊞ Win`-`backspace` toggles the layout mode for the current workspace, and will change the layout for the __next__ window opened on that workspace.  Toggling the layout by itself will not change anything on screen, but will effect how the next window is added to the workspace.
