---
layout: page
title: Internals
lang: it
---

Regolith is comprised of existing open source projects and some minor custom configuration and package metadata. The following table lists the primary components that make up Regolith Linux:

| Package | Function | Regolith Customization |
|---------|----------|------------------------|
|[Gnome-flashback](https://wiki.gnome.org/Projects/GnomeFlashback)|System Management|[package](https://github.com/regolith-linux/regolith-gnome-flashback)|
|[i3-wm](https://i3wm.org/)|Tiling Window Manager|[package](https://github.com/regolith-linux/regolith-i3)|
|[i3-gaps](https://github.com/Airblader/i3)|Nice additions to i3-wm|See i3-wm|
|[Rofi](https://github.com/davatorium/rofi)|Application Launcher and Window Switcher|[package](https://github.com/regolith-linux/regolith-rofi-config)|
|[Compton](https://github.com/chjj/compton)|Compositor|[package](https://github.com/regolith-linux/regolith-compton-config)|
|[Conky](https://github.com/brndnmtthws/conky)|Shortcuts on Desktop|[package](https://github.com/regolith-linux/regolith-conky-config)|
|[GDM3](https://wiki.debian.org/GDM)|Login Screen|[package](https://github.com/regolith-linux/regolith-gdm3-theme)|
|[Simple Terminal (st)](https://st.suckless.org/)|Terminal Emulator|[package](https://github.com/regolith-linux/regolith-st)|
|[i3-gnome-flashback](https://github.com/deuill/i3-gnome-flashback)|i3/gnome integration|[repo](https://github.com/deuill/i3-gnome-flashback)|
|[Adobe Source Code Pro](https://github.com/adobe-fonts/source-code-pro)|Primary Font|N/A|
|[Solarized Color Palette](https://ethanschoonover.com/solarized/)|Color Scheme|N/A|
|[Psiu Puxa Wallpapers](http://wallpaper-site.webflow.io/)|Desktop Backgrounds|N/A|

# Distribution

Regolith is a set of Ubuntu packages distributed via two "Private Package Repositories" (PPA):

| Repository | URL | Purpose |
| [Regolith Stable](https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-stable) | https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-stable | Primary repository for Regolith packages |
| [Regolith Unstable](https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-unstable) | https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-unstable | Pre-release versions of Regolith packages. Not recommended for everyday use of Regolith. |

# Hacking

## Configuration

Colors and fonts can be changed in Regolith by updating your Xresource values.  The primary Xresources file that Regolith uses is `/etc/regolith/styles/root`.  To customize them, copy that file to `~/.Xresources-regolith`.  After logging back in your new settings should take effect.

### Colors

Color values can be selected by toggling the `#includes` in your Regolith Xresources file.  Lines in Xresources are commented if `!` is the first character of the line.


## Package Changes

| Function | Component | Configuration File | Package |
|----------|-----------|--------------------|---------|
|Desktop Bar|i3-bar|`~/.config/regolith/i3/config`|regolith-i3|
|System Status Indicators|i3xrocks|`~/.config/regolith/i3xrocks/config`|regolith-i3xrocks|
|Window Manager|i3-wm|`~/.config/regolith/i3/config`|regolith-i3|
|App Launcher|Rofi|`/etc/rofi.conf`|regolith-rofi-config|
|System Keybindings|i3-wm|`~/.config/regolith/i3/config`|regolith-i3|
|Keybinding Guide|Conky|`/etc/xdg/conky/config`|regolith-conky-config|

## Packaging

All deployable aspects of Regolith Linux are expressed via debian packages.  These packages are available in source form on the [Regolith Linux Github project](https://github.com/regolith-linux).  Creating packages is not necessary to change the look and feel of Regolith, however there are advantages to packaging changes.  More easily sharing changes, ability to have a common configuration across machines, automatic updates, and a clean versioning strategy are all advantages to using a packaging system.
