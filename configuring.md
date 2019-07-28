---
layout: page
title: Configuring
---

Regolith Linux utilizes the Xresource facility to define and set color, typeface, and backgrounds.  These resources live in your home directory, and are designed to be easy to understand and modify.  Assuming you're already in a Regolith session, let's have a look at your Xresources file.  Because you may already have Xresource definitions that we wouldn't want to overwrite, Regolith-specific Xresources live in `~/.Xresources-regolith`:
```
! -- Styles - Colors
!
! Uncomment one and only one of the following color definitions 
#include ".Xresources.d/color-solarized-dark"
!#include ".Xresources.d/color-solarized-light"
!#include ".Xresources.d/color-gruvbox"
!#include ".Xresources.d/color-nord"

! -- Styles - Fonts
!
! Uncomment one and only one of the following font definitions 
#include ".Xresources.d/typeface-sourcecodepro"
!#include ".Xresources.d/typeface-sourcecodepro"

! -- Styles - Theme
!
! Uncomment one and only one of the following font definitions
#include ".Xresources.d/theme-regolith"
!#include ".Xresources.d/theme-ubuntu-dark"

! -- Applications
!
#include ".Xresources.d/st-term"
#include ".Xresources.d/i3-wm"
#include ".Xresources.d/i3xrocks"
#include ".Xresources.d/rofi"
#include ".Xresources.d/gnome"

! -- Policy
! Set this to false for Regolith to never update files on start
regolith.policy.update: true
```

This file is loaded into the Xresource database upon login, and values are referenced by various programs, such as i3 and scripts, such as blocklets to load values rather then hardcode them directly.  This allows us to change a value in one place, say the primary font size, and have that value propogate to all programs that may display something with the primary font.  

However, you'll note that we don't have any actual typeface or color values here.  There is a level of inderection that provides us the ability to swap out defention files without having to modify each value in place.  For example, the default color configuration, `.Xresources.d/color-solarized-dark` defines a key `color_red` and sets it to a specified RGB value.  Now if we look at `.Xresources.d/color-gruvbox`, we can see the same key, but set to a different color value.  In essense `.Xresources.d/color-solarized-dark` and `.Xresources.d/color-gruvbox` are two complimentary color theme settings, and we can change all of them at once by toggling which resource file to load, by commenting and uncommenting files with the `!` character as needed.

As an example, if I want to set my colors to Solarized Light, I would make the folowing change to the file above:
```
! Uncomment one and only one of the following color definitions 
!#include ".Xresources.d/color-solarized-dark"
#include ".Xresources.d/color-solarized-light"
!#include ".Xresources.d/color-gruvbox"
!#include ".Xresources.d/color-nord"
```

I've simply commented the line that specifies Solarized Dark, meaning the resources will not be loaded, and replaced them with Solarized Light.  Because both files define the same keys with different values, this is the only change I need to make to change the color selection.

This same pattern applies to fonts (Xresources that are prefixed with `typeface-`) and GTK themes (Xresources that are prefixed with `theme-`).

In a similar matter, it is straightforward to add new settings without modifying existing definitions.  For example, to create a new color scheme, simply copy an existing definition:
```
cp ~/.Xresources.d/color-solarized-dark ~/.Xresources.d/color-mything
```

Now edit `~/.Xresources.d/color-mything` and change the color definitions however you like.  To add them to the Xresources, change the root file to include your new file:
```
! Uncomment one and only one of the following color definitions 
!#include ".Xresources.d/color-solarized-dark"
!#include ".Xresources.d/color-solarized-light"
!#include ".Xresources.d/color-gruvbox"
!#include ".Xresources.d/color-nord"
#include ".Xresources.d/color-mything"
```

On next login, the color values specified in `color-mything` will be applied to all your programs automatically.

## [Migration Guide](#migration-guide)

Prior to August 2019, Regolith did not have a consistent way of updating theme information.  To update colors or typeface, several files with different syntax and rules had to be modified directly.  If you have done this, to use the Xresource system, you'll need to move your changes into Xresource files as described above.  Once you have this in place, here are a few scripts that will help you migrate.

### `regolith-config-reset.sh`

This program will backup your existing Regolith config data into your home directory.  It removes them from their original place so that Regolith knows that it can safely replace them next time you login.  You can safely delete the directory (`~/regolith-config-backup-<timestamp>`) if you don't have anything custom that you want to save and reintegrate.  If you do, after logging back in. diff the files in the backup directory with what you will have staged in ~/.config/i3-regolith`, `~/.config/i3xrocks`, and `~/.Xresources-regolith`.

### `regolith-config-init.sh`

This script gets called upon each login, but you can also call it from a shell if you prefer not to log out of your existing session.  Once the script is run, any updated Xresource values will be loaded and you can apply them by reloading i3.



