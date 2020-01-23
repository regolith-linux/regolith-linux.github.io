---
title: "Config Files"
linkTitle: "Config Files"
date: 2017-01-05
weight: 2
description: >
  General information about the config files that Regolith uses.
---

| **Component** | **Default Config** | **User Config** | **Notes** |
|------------|--------|--------|--------|-------------|
| i3-gaps | `/etc/regolith/i3/config` | `~/.config/regolith/i3/config` | In Regolith versions prior to 1.2 this file was in another directory.  |
| Xresources | `/etc/regolith/styles/root` | `~/.Xresources-regolith` | `~/.Xresources` is also loaded but intended for properties that may also be required in other desktop sessions. |
| Rofi | `/etc/regolith/styles/cahuella/rofi.rasi` | Defined in the `theme` style file. | This can also be overridden directly in the i3 file if preferred.
| Bar Workspace Labels | `/etc/regolith/styles/i3-wm` | User defined | |
| Bar status indicators | `/etc/regolith/i3xrocks/config` | User defined (i3 config) | |


