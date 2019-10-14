---
layout: page
title: How To
lang: sv
---

This page contains instructions on how to make commonly requested changes.

## [Stage your own version of the i3 configuration file](#user-i3-config)
1. Copy the default Regolith i3 config file into your user directory:
```
$ mkdir -p ~/.config/regolith/i3
$ cp /etc/regolith/i3/config ~/.config/regolith/i3/config
```
2. Log out and back in. You can verify by running `i3 --moreversion` and noting the config file that is printed as a result.

## [Change the default meta keybinding](#key-binding)

1. [Stage your own i3 config file](#user-i3-config), then open `~/.config/regolith/i3/config` in your editor of choice.
2. The first non-comment line should read `set $mod Mod4
`.
3. Replace `Mod4` with [one of these options](https://i3wm.org/docs/userguide.html#keybindings).
4. Reload i3 with `⊞ Win`-`shift`-`r`.

<sub>If you would like this to be easier to change, please vote for [this issue](https://github.com/regolith-linux/regolith-desktop/issues/16)</sub>

## [Add or change i3 Keybindings](#change-keybinging)
1. Consult the [i3 User's Guide](https://i3wm.org/docs/userguide.html) to find out which feature you'd like to add or change.
2. [Stage your own i3 config file](#user-i3-config), then open `~/.config/regolith/i3/config` in your editor of choice.
3. The lines which start with `bindsym` map keys to actions.  `$mod` means the modifier key, which by default is `⊞ Win`.  For example `bindsym $mod+Return exec /usr/bin/st` will cause i3 to run `/usr/bin/st` when `⊞ Win` and `Return` are pressed at the same time.
4. Update an existing line or add a new one based on your needs.  For example, to cause i3 to use tabbed layout mode, when `⊞ Win` and `t` are pressed, add this to the config file: `bindsym $mod+t workspace_layout tabbed`
5. After making the change, save the file and reload i3 with `⊞ Win` + `Shift` + `r`.

## [Change the default terminal from st to gnome-terminal](#default-term)

1. Install gnome-terminal (or whatever terminal you prefer): `sudo apt install gnome-terminal` and [Stage your own i3 config file](#user-i3-config).
2. Remap the i3-wm config to launch `gnome-terminal` instead of `st` by editing `~/.config/regolith/i3/config` and changing the following line:
From: `bindsym $mod+Return exec st`
To: `bindsym $mod+Return exec gnome-terminal`
3. Save file and reload i3 with `⊞ Win`-`shift`-`r`
4. (Optional) Update your system to default to your terminal of choice by running `sudo update-alternatives --config x-terminal-emulator` (See [this page](https://askubuntu.com/questions/578293/is-it-possible-to-remove-the-default-terminal-and-replace-it-with-some-other-ter) for more details)

## [Restore the Regolith default i3-wm configuration file](#default-i3-config)
1. Delete or copy to another location the file `~/.config/regolith/i3/config`
2. Log out and log back in, the default in `/etc/regolith/i3/config` will be used.  You can verify by running `i3 --moreversion` and noting the config file that is printed as a result.

## [Hide the bar until `⊞ Win` is pressed](#hide-bar)

1. [Stage your own i3 config file](#user-i3-config) and open `~/.config/regolith/i3/config` in your editor of choice.
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

After rebooting you should have an `i3-gnome` session to select from the login window "gear" (⚙️) menu.

## [Disable Compton](#disable-compton)

1. [Stage your own i3 config file](#user-i3-config) and open `~/.config/regolith/i3/config` in your editor of choice.
2. Find the line which launches compton, looking something like `exec --no-startup-id compton -f --config $compton_config`.  Comment out or remove the line.
3. Log out and back in to the Regolith session.  You can verify compton is not running via <br/> `$ ps aux | grep compton`

## [Enable an Icon Tray in the Bar](#i3-tray)
Enabling the task/icon tray in the bar requires a single change to your i3 config file, located at `~/.config/regolith/i3/config`.  Find the line with `tray_output none` and replace it with `tray_output primary`.  After logging back in or [reloading i3](https://regolith-linux.org/keybindings.html), the tray is active.  To verify it's working, run `nm-applet` from a terminal and notice the icon appears in the tray.  With the tray enabled, you'll then need to run applet programs of your choosing to show up in the tray.  This can be done via the i3 `exec` command.  See the [i3-wm User Guide](https://i3wm.org/docs/userguide.html#_tray_output) for more information.

## [Create your own version of Regolith from source](#create-regolith-fork)

A primary goal of Regolith is to enable more people to create their own unique desktop experience.  What is installed to get the Regolith environment is simply a series of Debian packages for Ubuntu provided in a set of [Private Package Repositories](https://help.launchpad.net/Packaging/PPA?action=show&redirect=PPA) (PPA).  In `regolith-desktop` there is a shell script `build.sh` that will produce packages and publish them to a PPA. The script simply automates the task of checking out, building, and publishing packages as [described here](http://packaging.ubuntu.com/html/packaging-new-software.html). Anyone can fork any of the Regolith repos, make changes, and use the script to produce their own variant of Regolith.  The following steps assume you're building Regolith in a Ubuntu 18.04+ system.

1. [Create an Ubuntu PPA](https://askubuntu.com/a/71516).
1. Install and configure your system to build Debian packages.<br/>`sudo apt install build-essential debhelper dh-make devscripts git gnupg quilt`
2. Check out the `regolith-desktop` package.<br/>`git clone https://github.com/regolith-linux/regolith-desktop.git && cd regolith-desktop`
3. Take a look at `package-model.json`, it defines where the packages should be built from. To customize Regolith, you'll need to update one or more of these repos to point to your own fork (depending on what you want to change).  For this exercise we will use the package model as-is.
4. Run the build script.<br/>`./build.sh package-model.json ppa:<your Launchpad.net username>/<your PPA name> /tmp/regolith-build`
5. After some time, the script will complete.  Refresh the PPA web page and you'll see many packages have been uploaded into your PPA. Check the package details via the PPA Web UI and you may see that some packages are still in the process of building.  You'll need to wait until this process completes before being able to test them.
6. You'll notice most or all of the packages are built for a specific version of Ubuntu, such as `disco`.  Depending on which Ubuntu version you wish to target, you may want to **copy packages** using the PPA web UI.  Your PPA must provide all packages for the version of Ubuntu you wish to support.
7. Once you have the packages for the version of Ubuntu you wish to target, add your PPA to a test system to verify it works.<br/>`sudo add-apt-repository ppa:<your Launchpad.net username>/<your PPA name>`
8. Now install Regolith desktop from your PPA.<br/>`sudo apt install regolith-desktop`
9. You may notice that some packages are missing and the installation cannot proceed.  This is because some packages that Regolith depends on are provided by others.  There are two ways of resolving this: Either copy the missing packages into your PPA (via the PPA Web UI), or add the other PPAs into your system.  At the time of writing this, the only required PPA is `snwh/ppa` which hosts icons.  To add this PPA run:<br/>`sudo add-apt-repository -u ppa:snwh/ppa`.  
9. Now try and install `regolith-desktop` again.  This time it should complete successfully.  Reboot and login with the Regolith session to complete the test.

### Next Steps

Now that you've built your own Regolith, fork the repositories that you want to change, update the `package-model.json` to refer to your forks, and run the build script when you're ready to test your changes.
