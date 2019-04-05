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

Regolith is distributed via a view "Private Package Repositories" (PPA):

| Repository | URL | Purpose |
| [Regolith Stable](https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-stable) | https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-stable | Primary repository for Regolith packages |
| [Regolith Unstable](https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-unstable) | https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-unstable | Pre-release versions of Regolith packages. Not recommended for everyday use of Regolith. |


