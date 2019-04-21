---
layout: page
title: How To
---

This page contains instructions on how to make commonly requested changes.

## Change the default meta keybinding
1. Open `~/.config/i3-regolith/config` in your editor of choice.
2. The first non-comment line should read `set $mod Mod4
`.
3. Replace `Mod4` with [one of these options](https://i3wm.org/docs/userguide.html#keybindings).
4. Reload i3 with `⊞ Win`-`shift`-`r`.

## Change the default terminal from st to gnome-terminal

1. Install gnome-terminal (or whatever terminal you prefer): `sudo apt install gnome-terminal`. (NOTE: this is not necessary if you already have your terminal installed.)
2. Remap the i3wm config to launch `gnome-terminal` instead of `st` by editing `~/.config/i3-regolith/config` and changing the following line:
From: `bindsym $mod+Return exec st`
To: `bindsym $mod+Return exec gnome-terminal`
3. Save file and reload i3 with `⊞ Win`-`shift`-`r`
4. (Optional) Update your system to default to your terminal of choice by running `sudo update-alternatives --config x-terminal-emulator` (See [this page](https://askubuntu.com/questions/578293/is-it-possible-to-remove-the-default-terminal-and-replace-it-with-some-other-ter) for more details)

## Restore the default i3wm configuration file
1. Delete or copy to another location the file `~/.config/i3-regolith/config`
2. Log out and log back in.  A fresh default copy will be installed at `~/.config/i3-regolith/config`.
