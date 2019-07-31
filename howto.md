---
layout: page
title: How To
lang: en
---

This page contains instructions on how to make commonly requested changes.

## [Change the default meta keybinding](#key-binding)
1. Open `~/.config/i3-regolith/config-4.16-1ubuntu18ppa10` in your editor of choice.
2. The first non-comment line should read `set $mod Mod4
`.
3. Replace `Mod4` with [one of these options](https://i3wm.org/docs/userguide.html#keybindings).
4. Reload i3 with `⊞ Win`-`shift`-`r`.

<sub>If you would like this to be easier to change, please vote for [this issue](https://github.com/regolith-linux/regolith-desktop/issues/16)</sub>

## [Add or change i3 Keybindings](#change-keybinging)
1. Consult the [i3 User's Guide](https://i3wm.org/docs/userguide.html) to find out which feature you'd like to add or change.
2. Open `~/.config/i3-regolith/config-4.16-1ubuntu18ppa10` in your editor of choice.
3. The lines which start with `bindsym` map keys to actions.  `$mod` means the modifier key, which by default is `⊞ Win`.  For example `bindsym $mod+Return exec /usr/bin/st` will cause i3 to run `/usr/bin/st` when `⊞ Win` and `Return` are pressed at the same time.
4. Update an existing line or add a new one based on your needs.  For example, to cause i3 to use tabbed layout mode, when `⊞ Win` and `t` are pressed, add this to the config file: `bindsym $mod+t workspace_layout tabbed`
5. After making the change, save the file and reload i3 with `⊞ Win` + `Shift` + `r`.

## [Change the default terminal from st to gnome-terminal](#default-term)

1. Install gnome-terminal (or whatever terminal you prefer): `sudo apt install gnome-terminal`. (NOTE: this is not necessary if you already have your terminal installed.)
2. Remap the i3-wm config to launch `gnome-terminal` instead of `st` by editing `~/.config/i3-regolith/config-4.16-1ubuntu18ppa10` and changing the following line:
From: `bindsym $mod+Return exec st`
To: `bindsym $mod+Return exec gnome-terminal`
3. Save file and reload i3 with `⊞ Win`-`shift`-`r`
4. (Optional) Update your system to default to your terminal of choice by running `sudo update-alternatives --config x-terminal-emulator` (See [this page](https://askubuntu.com/questions/578293/is-it-possible-to-remove-the-default-terminal-and-replace-it-with-some-other-ter) for more details)

## [Restore the Regolith default i3-wm configuration file](#default-i3-config)
1. Delete or copy to another location the file `~/.config/i3-regolith/config-4.16-1ubuntu18ppa10`
2. Log out and log back in.  A fresh default copy will be installed at `~/.config/i3-regolith/config-4.16-1ubuntu18ppa10`.

## [Hide the bar until `⊞ Win` is pressed](#hide-bar)

1. Open `~/.config/i3-regolith/config-4.16-1ubuntu18ppa10` in your editor of choice.
2. After the line `bar {`, add the following entry: `mode hide`. (See [here](https://i3wm.org/docs/userguide.html#_configuring_i3bar) for details)
3. Reload i3 with `⊞ Win`-`shift`-`r`.

<sub>If you would like this to be easier to change, please vote for [this issue](https://github.com/regolith-linux/regolith-desktop/issues/16)</sub>

## [Add Stock Ubuntu Session to Login](#stock-ubuntu)

If Regolith is installed from the LiveCD installer, the stock Ubuntu session is removed due to the finicky way that users must specify sessions in the login screen. Users may wish to add this session back in to access some UI features that Regolith removes.  NOTE: This howto does not apply to users installing Regolith on an existing Ubuntu system.

1. In a terminal, install the Ubuntu session: `sudo apt install ubuntu-session`
2. Reboot and when when presented with the login screen, select "Ubuntu" from the "gear" drop-down menu.

## [Use i3 and Gnome without Regolith](#i3-gnome-no-regolith)

If you'd like to get all the usability features of gnome integration, but prefer to keep your own i3 setup, perform the following steps from a terminal:
```
$ sudo apt install i3 gnome-flashback build-essential 
$ git clone https://github.com/deuill/i3-gnome-flashback
$ cd i3-gnome-flashback
$ sudo make install
$ /sbin/reboot
```

After rebooting you should have an `i3-gnome` session to select from the login window "gear" menu.

## [Change the window highlight color](#window-highlight-color)

If the shading between active and inactive windows is too subtle for your tastes, [here is a tip](https://github.com/regolith-linux/regolith-desktop/issues/42#issuecomment-503789313) on how to update the i3 config for a stronger border.

Open the i3 configuration file (`~/.config/i3-regolith/config-4.16-1ubuntu18ppa10`) in a text editor, look for existing text as below and update the values according to taste.  For example:
```
new_window pixel 4
new_float pixel 4
client.focused          #002b36 $blue #fdf6e3 #268bd2
```

Another approach is to make inactive windows darker.  This can be achieved by editing the compton configuration in the file `/etc/xdg/compton.conf` and adjusting the value of `inactive-dim`.  You'll need to `sudo` to edit the file and reload i3 to see the change.

## [View and modify the Regolith i3 Config](#i3-config)
The i3 config file that Regolith uses is not easy to find.  This is because the final file is the result of the application of several patches against the default i3 config file.  To generate this file we need to use the `quilt` tool with the `regolith-i3` package.

### Setup
```
$ sudo apt install quilt
$ export QUILT_PATCHES=debian/patches  # See https://wiki.debian.org/UsingQuilt for details
$ export QUILT_REFRESH_ARGS="-p ab --no-timestamps --no-index"
```

### Extraction
```
$ git clone https://github.com/regolith-linux/regolith-i3.git  # Clone Regolith's version of i3
...
$ quilt push -a 
Applying patch debian/patches/remove_i3_xsession.patch
patching file Makefile.am
...
$ less etc/config  # Here is what ends up in Regolith for i3 config.
```

### Modification
First we need to create a new patch to hold our changes:
```
$ quilt new my-regolith-change.patch # tell quilt to create a new patch
$ quilt add etc/config # tell quilt which file changes belong in your patch
$ your-editor-of-choice etc/config  #make your changes
$ quilt refresh  # this updates the patch with the delta of your change vs what was there before.
$ quilt pop -a  # roll the patches back up and leave the files as they were
```

### Verification
You should be able to see your changes in your new patch file in `debian/patches/your-patch-name.patch`.  Have a look at the changes to make sure they are what you intended.  If good, you're ready to submit a PR or push the changes to your own fork.  But, if you intend to publish your own version, use `dch` to add a change log entry and bump the version number.

## [Enable an Icon Tray in the Bar](#i3-tray)
Enabling the task/icon tray in the bar requires a single change to your i3 config file, located at `~/.config/i3-regolith/config-4.16-1ubuntu18ppa10`.  Find the line with `tray_output none` and replace it with `tray_output primary`.  After logging back in or [reloading i3](https://regolith-linux.org/keybindings.html), the tray is active.  To verify it's working, run `nm-applet` from a terminal and notice the icon appears in the tray.  With the tray enabled, you'll then need to run applet programs of your choosing to show up in the tray.  This can be done via the i3 `exec` command.  See the [i3-wm User Guide](https://i3wm.org/docs/userguide.html#_tray_output) for more information.