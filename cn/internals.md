---
layout: page
title: 内部构成
lang: cn
---

Regolith 是由一些开源项目/软件， 一些自定义设置和 Package 元数据构成。 以下表格列举了主要组件:
Regolith Linux:  

| Package | 功能 | Regolith 自定义 |
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

Regolith是一系列由 "Private Package Repositories" (PPA) 分布的 Ubuntu packages:

| Repository | URL | Purpose |
| [Regolith Stable](https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-stable) | https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-stable | Primary repository for Regolith packages |
| [Regolith Unstable](https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-unstable) | https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-unstable | Pre-release versions of Regolith packages. Not recommended for everyday use of Regolith. |

# Hacking

## 设置

| 功能 | 组件 | 设置文件 | Package |
|----------|-----------|--------------------|---------|
|状态条|i3-bar|`~/.config/i3-regolith/config-4.16-1ubuntu18ppa10`|regolith-i3|
|系统状态提示|i3blocks|`/etc/i3blocks.conf`|regolith-i3blocks|
|窗口管理|i3-wm|`~/.config/i3-regolith/config-4.16-1ubuntu18ppa10`|regolith-i3|
|App Launcher|Rofi|`/etc/rofi.conf`|regolith-rofi-config|
|系统快捷键绑定|i3-wm|`~/.config/i3-regolith/config-4.16-1ubuntu18ppa10`|regolith-i3|

## 打包

Regolith Linux 所有可布署的组件都是由debian packages 来描述的。 这些 packages 都在 [Regolith Linux Github project](https://github.com/regolith-linux) 以源码的形式存在。
创建 packages 对更改Regolith的外观来说是不必要的。 但是创建Packages有一些好处。
比如说更容易分享更改，在不同的机器上使用同一种设置，自动更新，以及更好的版本控制。
