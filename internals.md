---
layout: default
---

# Internals

Regolith is comprised of existing open source projects and some minor custom configuration and package metadata.

| Package | Function | Regolith Customization |
|---------|----------|------------------------|
|[Adobe Source Code Pro](https://github.com/adobe-fonts/source-code-pro)|Primary Font|N/A|
|[Solarized Color Palette](https://ethanschoonover.com/solarized/)|Color Scheme|N/A|
|[Gnome-flashback](https://wiki.gnome.org/Projects/GnomeFlashback)|System Management|[package](https://github.com/regolith-linux/regolith-gnome-flashback)|
|[i3-wm](https://i3wm.org/)|Tiling Window Manager|[package](https://github.com/regolith-linux/regolith-i3)|
|[Rofi](https://github.com/davatorium/rofi)|Application Launcher and Window Switcher|[package](https://github.com/regolith-linux/regolith-rofi-config)|
|[Compton](https://github.com/chjj/compton)|Compositor|[package](https://github.com/regolith-linux/regolith-compton-config)|
|[Conky](https://github.com/brndnmtthws/conky)|Shortcuts on Desktop|[package](https://github.com/regolith-linux/regolith-conky-config)|
|[GDM3](https://wiki.debian.org/GDM)|Login Screen|[package](https://github.com/regolith-linux/regolith-gdm3-theme)|
|[Simple Terminal (st)](https://st.suckless.org/)|Terminal Emulator|[package](https://github.com/regolith-linux/regolith-st)|

# Distribution

Regolith is a set of Ubuntu packages distributed via two "Private Package Repositories" (PPA):

| Repository | URL | Purpose |
| [Regolith Stable](https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-stable) | https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-stable | Primary repository for Regolith packages |
| [Regolith Unstable](https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-unstable) | https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-unstable | Pre-release versions of Regolith packages. Not recommended for everyday use of Regolith. |

# Hacking

## Configuration

| Function | Component | Configuration File | Package |
|----------|-----------|--------------------|---------|
|Desktop Bar|i3-bar|`~/.config/i3-regolith/config`|regolith-i3|
|System Status Indicators|i3blocks|`/etc/i3blocks.conf`|regolith-i3blocks|
|Window Manager|i3-wm|`~/.config/i3-regolith/config`|regolith-i3|
|App Launcher|Rofi|`/etc/rofi.conf`|regolith-rofi-config|
|System Keybindings|i3-wm|`~/.config/i3-regolith/config`|regolith-i3|

## Packaging

All runtime aspects of Regolith Linux are expressed via debian packages.  These packages are available in source form on the [https://github.com/regolith-linux](Regolith Linux Github project).  Creating packages is not necessary to change the look and feel of Regolith, however there are advantages to packaging changes.  More easily sharing changes, ability to have a common configuration across machines, automatic updates, and a clean versioning strategy are all advantages to using a packaging system.
