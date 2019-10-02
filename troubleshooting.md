---
layout: page
title: Troubleshooting
---

This page contains information that may help if you encounter an issue with Regolith Linux. If your problem isn't already here, you can join the [Slack channel](https://regolith-linux.herokuapp.com/) to ask, or kindly [file an issue](https://github.com/regolith-linux/regolith-desktop/issues) and describe your problem.

# Update

## [Regolith Uninstalled after Update](#uninstalled)

Some users have reported that `regolith-desktop` and other packages are removed when performing a `apt dist-upgrade`.  The root cause of [this issue](https://github.com/regolith-linux/regolith-desktop/issues/120) is unclear, however re-installing `regolith-desktop` via `apt install regolith-desktop` should suffice to resolve the issue.  Any configuration files in the user directory will not be impacted by this issue.

## [After Update see `Could not parse JSON` in bar](#outdated-xresources)

If you just updated your version of Regolith and you are seeing an error on your bottom bar (something like Could not parse JSON), it's most probably your `~/.Xresources-regolith` file that has incorrect/insufficient config in it. To fix it (and go back to stock config) you can delete or move that file somewhere else and log out and back in again (gnome-session-quit). If you want to pick a different theme or customize your Xresources, feel free to copy `/etc/regolith/styles/root` (the stock Xresources file) to `~/.Xresources-regolith` and customise it!

## [Lost Configuration Changes](#where-is-config)

If you've just updated Regolith and have lost any customizations to i3-wm, Rofi, i3bar, Conky, or i3blocks, this is due to a new versioning scheme.  Initially, config files were copied from a common location into your user directory upon new session creation.  However, some recent backwards-incompatable changes to support easier themeing were introduced.  To address this and to be more consistent with where Linux expects config files to be, they have moved to `/etc/regolith/`.  To make modifications, copy the file you wish to modify to your user directory first.  Here are the steps to copy default configurations to your user directory where you can make edits:

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

## [Screen locks twice when waking up from Suspend](#screen-lock)

This issue can occur if 'Blank Screen' and 'Automatic Suspend' set for the same amount of time.<br/>

For example, if Automatic Suspend and Blank Screen are both set for 15 minutes, after 15 minutes of Idle time the signal to suspend and blank the screen will be sent simultaneously.  The signal to suspend takes priority and is processed immediatley, the signal to Blank the screen is delayed. After waking the computer from suspend and typing the password to unlock, the signal to Blank the screen is processed.  This causes the user to have to press a key to wake the screen.  If 'Automatic Screen Lock' is set in the Privacy settings, it also causes the user to need to re-enter their password.
<br/>
To resolve this issue, change 'Blank Screen' and 'Automatic Suspend' to happen at different times.
<br/>
To find these settings press `⊞ Win` - `Space` and open Settings.  Click Power on the left-side. Change 'Blank Screen' as desired, for example 12 minutes.  Click 'Automatic Suspend' and change the Delay as desired, for example 15 minutes.