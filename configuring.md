---
layout: page
title: Configuring
---

<sub>_See [quick steps](#quick-steps) below for just making changes quickly, or read this to get an understanding of how configuration works in Regolith._</sub>

Regolith Linux utilizes the [Xresource facility](https://en.wikipedia.org/wiki/X_resources#Location_and_use) to define and set [color](https://github.com/regolith-linux/regolith-styles/blob/master/Xresources/root#L3-L7), [typeface](https://github.com/regolith-linux/regolith-styles/blob/master/Xresources/root#L9-L13), and [backgrounds](https://github.com/regolith-linux/regolith-styles/blob/master/Xresources/root#L9-L13).  These resources live in your home directory, and are designed to be easy to understand, modify, and reset.  Assuming you're already in a Regolith session, let's have a look at your Xresources file.  Because you may already have Xresource definitions that we wouldn't want to overwrite, Regolith-specific Xresources live in `~/.Xresources-regolith`:
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

This file is loaded into the Xresource database [upon login](https://github.com/regolith-linux/regolith-scripts/blob/master/regolith-config-init.sh#L23-L33), and values are referenced by various programs, such as i3 and scripts, such as blocklets to load values rather than hardcode them directly.  This allows us to change a value in one place, say the primary font, and have that value propogate to all programs.  

However, you'll note that we don't have any actual typeface or color values in `~/.Xresources-regolith`.  There is a level of indirection that provides us the ability to swap out definition files without having to modify each value in place.  Specifically, we use the `#define` keyword to specify a literal value, and then map it to a specific application property in application-specific Xresource files such as `~/.Xresources.d/st-term`.  For example, the default color configuration, `.Xresources.d/color-solarized-dark` defines a key `color_red` and sets it to a specified RGB value.  Now if we look at `.Xresources.d/color-gruvbox`, we can see the same key, but set to a different color value.  Then, if we look at `~/.Xresources.d/i3-wm`, we can see that key mapped to specific UI elements, such as `i3-wm.client.urgent.color.background`.  In essense `.Xresources.d/color-solarized-dark` and `.Xresources.d/color-gruvbox` are two complimentary color theme definitions.  We can change all of them at once by toggling which resource file to load; by commenting and uncommenting files with the `!` character as needed.

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

### Refreshing the UI

Currently after modifying some values, such as Gnome settings like the background, the `regolith-config-reset.sh` script needs to be run before the changes are visible.  This is a temporary restriction that will be [addressed here](https://github.com/regolith-linux/regolith-scripts/issues/2).

Continuing with our example above, on next login, the color values specified in `color-mything` will be applied to all your programs automatically.  You can also reload the configuration with the `regolith-config-init.sh` script, which should be on your path.  Optionally you can back-up your existing configuration with the `regolith-config-reset.sh` script.

# [Quick Steps](#quick-steps)

## Change Color Theme

1. Edit `~/.Xresources-regolith`, add a `!` to the line `#include ".Xresources.d/color-solarized-dark"` and uncomment one of the other lines in the same section, say gruvbox by removing the `!` at the beginning of the line: `#include ".Xresources.d/color-gruvbox"`.
2. Run `regolith-config-reset.sh` and then `regolith-config-init.sh`.
3. Reload i3.

## Change Gnome Theme

1. Edit `~/.Xresources-regolith`, add a `!` to the line `#include ".Xresources.d/theme-regolith"` and uncomment one of the other lines in the same section, say Ubuntu Dark by removing the `!` at the beginning of the line: `#include ".Xresources.d/theme-ubuntu-dark"`.
2. Run `regolith-config-reset.sh` and then `regolith-config-init.sh`.

## Add a New Color Theme

1. Copy the new theme file into your `~/.Xresources.d` directory.  For example, if you have a color theme `color-sunday`, `cp color-sunday ~/.Xresources.d/`.
2. Reference your new color file in the Regolith Xresources file:
```
! -- Styles - Colors
!
! Uncomment one and only one of the following color definitions 
!#include ".Xresources.d/color-solarized-dark"
!#include ".Xresources.d/color-solarized-light"
!#include ".Xresources.d/color-gruvbox"
!#include ".Xresources.d/color-nord"
#include ".Xresources.d/color-sunday"
```
3. Run `regolith-config-reset.sh` and then `regolith-config-init.sh`.
4. Reload i3.

# [Migration Guide](#migration-guide)

Prior to August 2019, Regolith did not have a consistent way of updating theme information.  To update colors or typeface, several files with different syntax and rules had to be modified directly.  If you have done this, to use the Xresource system, you'll need to move your changes into Xresource files as described above.  Once you have this in place, here are a few scripts that will help you migrate.

Additionally, `i3blocks` was replaced with a fork that enables Xresources, called `i3xrocks`.  And `xgetres` has been replaced with `xrescat` for loading Xresource values into scripts.

### `regolith-config-reset.sh`

This program will backup your existing Regolith config data into your home directory.  It removes them from their original place so that Regolith knows that it can safely replace them next time you login.  You can safely delete the directory (`~/regolith-config-backup-<timestamp>`) if you don't have anything custom that you want to save and reintegrate.  If you do, after logging back in. diff the files in the backup directory with what you will have staged in ~/.config/i3-regolith`, `~/.config/i3xrocks`, and `~/.Xresources-regolith`.

### `regolith-config-init.sh`

This script gets called upon each login, but you can also call it from a shell if you prefer not to log out of your existing session.  Once the script is run, any updated Xresource values will be loaded and you can apply them by reloading i3.



