---
layout: page
title: How To
lang: en
---

This page contains instructions on how to make commonly requested changes.

## [Change the default meta keybinding](#key-binding)
1. Open `~/.config/i3-regolith/config` in your editor of choice.
2. The first non-comment line should read `set $mod Mod4
`.
3. Replace `Mod4` with [one of these options](https://i3wm.org/docs/userguide.html#keybindings).
4. Reload i3 with `⊞ Win`-`shift`-`r`.

<sub>If you would like this to be easier to change, please vote for [this issue](https://github.com/regolith-linux/regolith-desktop/issues/16)</sub>

## [Change the default terminal from st to gnome-terminal](#default-term)

1. Install gnome-terminal (or whatever terminal you prefer): `sudo apt install gnome-terminal`. (NOTE: this is not necessary if you already have your terminal installed.)
2. Remap the i3-wm config to launch `gnome-terminal` instead of `st` by editing `~/.config/i3-regolith/config` and changing the following line:
From: `bindsym $mod+Return exec st`
To: `bindsym $mod+Return exec gnome-terminal`
3. Save file and reload i3 with `⊞ Win`-`shift`-`r`
4. (Optional) Update your system to default to your terminal of choice by running `sudo update-alternatives --config x-terminal-emulator` (See [this page](https://askubuntu.com/questions/578293/is-it-possible-to-remove-the-default-terminal-and-replace-it-with-some-other-ter) for more details)

## [Restore the Regolith default i3-wm configuration file](#default-i3-config)
1. Delete or copy to another location the file `~/.config/i3-regolith/config`
2. Log out and log back in.  A fresh default copy will be installed at `~/.config/i3-regolith/config`.

## [Hide the bar until `⊞ Win` is pressed](#hide-bar)

1. Open `~/.config/i3-regolith/config` in your editor of choice.
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
