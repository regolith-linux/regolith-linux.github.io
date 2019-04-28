---
layout: page
title: How To
lang: cn
---

这个页面提供比较常见的自定义指导。

## [更改默认的元键绑定](#key-binding)。
1. 用任何文本编辑器打开`~/.config/i3-regolith/config`。   
2. 第一个没有被注释语句应该是`set $mod Mod4`。   
3. 把`Mod4` 换成 [选项中一个](https://i3wm.org/docs/userguide.html#keybindings)。   
4. 重置i3: `⊞ Win`-`shift`-`r`。   

<sub>如果你希望更简单的做以上的更改，请投票 [this issue](https://github.com/regolith-linux/regolith-desktop/issues/16)</sub>

## [把默认的 ST 终端更换成 gnome-termial 终端](#default-term)

1. 安装 gnome-terminal (或者任何一个你喜爱的终端): `sudo apt install gnome-terminal`. (如果你已经安装了此终端，这一步可以省略)
2. 重新映射 i3wm 的配置。 编辑`~/.config/i3-regolith/config`， 更改下列语句:
更改前: `bindsym $mod+Return exec st`
更改后: `bindsym $mod+Return exec gnome-terminal`
3. Save file and reload i3 with `⊞ Win`-`shift`-`r`
4. (可选)  更改操作系统的默认终端 `sudo update-alternatives --config x-terminal-emulator` (参见 [此页面](https://askubuntu.com/questions/578293/is-it-possible-to-remove-the-default-terminal-and-replace-it-with-some-other-ter))  

## [恢复Regolith 默认的 i3wm 的配置文件](#default-i3-config)
1. 删除或者移动该文件到其它地方  `~/.config/i3-regolith/config`  
2. 录出然后录入。 一个新的默认的 `~/.config/i3-regolith/config` 将会被自动创建。

## [隐藏状态条直到敲击 `⊞ Win` 键](#hide-bar)
1. 用任何文本编辑器打开`~/.config/i3-regolith/config`。  
2. 在这一行语句 `bar {`后，加以下语句： `mode hide`. (参见 [这里](https://i3wm.org/docs/userguide.html#_configuring_i3bar))
3. 重置 i3 ： `⊞ Win`-`shift`-`r`。

<sub>如果你希望更简单的做以上的更改，请投票 [this issue](https://github.com/regolith-linux/regolith-desktop/issues/16)</sub>