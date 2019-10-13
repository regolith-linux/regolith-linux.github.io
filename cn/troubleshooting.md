---
layout: page
title: 常见问题解决
lang: cn
---

这个页面会帮助你解决你在使用Regolith Linux中遇到的常见问题。 如果你的问题不在这里， 请 [提交一个 Issue](https://github.com/regolith-linux/regolith-desktop/issues) 并且描述你的问题。

# 安装

## PPA

### [程序包冲突 Package Conflicts](#package-conflict)
Regolith 是以Debian程序包来安装的。 根据设计， 一个程序包会安装失败如果安装包的过程会覆盖系统中已有的文件。
所以， 如果你已经安装了i3-wm, rofi, gnome-flashback, or compton， 你将无法成功安装Regolith， 除非你移除他们。
移除他们可以用以下方法： 在源代码目录运行 `sudo make uninstall` 或者 用 `sudo apt remove <package>` 来移除非Regolith的Debian的程序包。
移除成功后，重新尝试安装 `regolith-desktop` 即可。
