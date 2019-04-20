---
layout: page
title: Troubleshooting
---

This page contains information that may help if you encounter an issue with Regolith Linux. If your problem isn't already here, kindly [file an issue](https://github.com/regolith-linux/regolith-desktop/issues) and describe your problem.

# Installation

## PPA

Regolith is installed using Debian packages. By design, a package will fail to install if by installing it would overwrite existing files on your system.  So, if you have already installed (either via package or compiled from sources) i3wm, rofi, gnome-flashback, or compton, you will not be able to install Regolith without moving or removing them.  To remove them, run `sudo make uninstall` from the source directory, or use `sudo apt remove <package>` for non-Regolith debian packages.  Once removed try installing `regolith-desktop` again.
