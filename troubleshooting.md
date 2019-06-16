---
layout: page
title: Troubleshooting
---

This page contains information that may help if you encounter an issue with Regolith Linux. If your problem isn't already here, kindly [file an issue](https://github.com/regolith-linux/regolith-desktop/issues) and describe your problem.

# Installation

## PPA

### [Package Conflicts](#package-conflict)
Regolith is installed using Debian packages. By design, a package will fail to install if by installing it would overwrite existing files on your system.  So, if you have already installed (either via package or compiled from sources) i3-wm, rofi, gnome-flashback, or compton, you will not be able to install Regolith without moving or removing them.  To remove them, run `sudo make uninstall` from the source directory, or use `sudo apt remove <package>` for non-Regolith debian packages.  Once removed try installing `regolith-desktop` again.

# Usage

## [Keybinding to toggle horizontal/vertical window layout doesn't work.](#layout-keybinding)

The keybinding `⊞ Win`-`backspace` toggles the layout mode for the current workspace, and will change the layout for the __next__ window opened on that workspace.  Toggling the layout by itself will not change anything on screen, but will effect how the next window is added to the workspace.
