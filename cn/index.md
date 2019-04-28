---
layout: default
title: 
lang: cn
---

Regolith 是一个精心设计， 以提高使用者工作效率为核心理念的基于Ubuntu 的 Linux Distribution。 它整合了ubuntu的广泛性，[i3wm](https://i3wm.org/)
的高效的用户界面， 以及 Gnome [系统设置](https://gitlab.gnome.org/GNOME/gnome-control-center)的功能。

## 它看起来是这样的

<a href="/assets/screenshot-empty.png"><img class="screenshot" alt="Empty Desktop" src="/assets/screenshot-empty.png"/></a>

Regolith 看起来非常简洁。 这么做是为了减少“杂音”，防止使用者的注意力被分散。 它没有任何图标， 任务栏， 版块， 菜单， 或者， 广告 等占用屏幕空间的杂物。 
一个很小的状态条显示必要的信息， 比如说工作区和系统状态。

<a href="/assets/screenshot-apps.png"><img class="screenshot" alt="Tiled Windows" src="/assets/screenshot-apps.png"/></a>

尽管Regolith的界面很简洁， 它提供了流行的系统和文件管理功能，比如说外接显示器和存储管理， WIFI 和蓝牙设置， 以及语言和隐私设置。

<a href="/assets/screenshot-rofi.png"><img class="screenshot" alt="Launch Apps" src="/assets/screenshot-rofi.png"/></a>

快捷的通过App Launcher 浏览， 查找， 和启动应用程序。 这个对话框也可以用来查找和选择所有工作区的应用程序窗口。

<a href="/assets/screenshot-term.png"><img class="screenshot" alt="View Terminals" src="/assets/screenshot-term.png"/></a>

由于Regolith 利用 i3wm 来做窗口管理， 屏幕里每一个像素都没有浪费。 

## 如何获取Regolith Linux

Regolith 可以用以下两种方式获取：  
如果你已经有了Ubuntu， 可以通过 [Regolith PPA](https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-stable) 来安装 `regolith-desktop`。  
如果你想从头安装， 可以通过下载 Regolith Linux ISO 镜像， 然后可以像安装Ubuntu 一样来安装Regolith。  
两种方法的效果都是一样的。 唯一的不同就是LiveCD ISO方式没有默认的Ubuntu的界面选项。

### Option 1: LiveCD 安装方式

LiveCD ISO 镜像可以在 [from Source Forge](https://sourceforge.net/projects/regolith-linux/) 下载。 你可以用安装其它Linux Distribution 的方式来安装。

### Option 2: Regolith Ubuntu PPA

在你正在使用的 Ubuntu 18.04 里， 完成以下步骤：  
1. 打开终端， 输入 `sudo add-apt-repository -y ppa://kgilmer/regolith-stable`
2. 安装Regolith 桌面环境： `sudo apt install regolith-desktop`
3. 一些程序包会安装。 完成后重启电脑。
4. 在录入界面，点选工具图标，选择Regolith，然后录入。

<sub>如果你在第二步出现报错, 请参详 [常见问题]({% link cn/troubleshooting.md %})</sub>

#### Uninstalling Regolith

首先，删除package： `sudo apt remove regolith-desktop`。 然后， 删除 package archive reference： `sudo add-apt-repository --remove ppa://kgilmer/regolith-stable`。
最后重启系统。

## Next Steps

请阅读[入门]({% link cn/getting_started.md %}) 来了解关于Regolith的更多功能。 如果你想了解Regolith是如何构建的， 也可以参详[内部构成]({% link cn/internals.md %}) 页面。
