---
---
# 

## General Layout

Bar

Windows

Workspaces

Launcher

Notifications

Keybinding Helper

## Launching Programs

In Regolith Linux, applications are launched via the `⊞ Win`-`space` sequence.  A full screen dialog is presented.  Begin typing the app or command and the list will filter as you type.  Launch the app by selecting it and pressing `enter`.

The terminal application is special in Regolith as it can be launched with `⊞ Win`-`enter`.

## Workspaces

Stacks of overlapping windows is something Regolith avoids.  In tiling window systems, it is common to arrange windows into groupings of workspaces.  These can be thought of as virtual screens. These workspaces are used to group and organize work, depending on how you prefer it.  Perhaps by program, task, or mood ~ it's up to you!  In traditional window systems, you would search out the window you need from the stack, or use a dock application.  In Regolith, you navigate to the workspace that contains the window, or use  `⊞ Win`-`w` to explicitly select the window from the dialog.

The currently active workspace and all workspaces that you have open will be visibile as a series of indexed colored boxes at the lower left part of the screen.  The active workspace will be highlighted.  To switch to a specific workspace, enter  `⊞ Win`-`<workspace number>`.  For example, to move to workspace 3, enter  `⊞ Win`-`3`.  Relative navigation can be performed with  `⊞ Win`-`tab` (next) and  `⊞ Win`-`shift`-`tab` (previous).

## Managing Windows

As you launch more applications in a given workspace, the window manager will re-arrange the existing windows such that all windows are visible without overlap, also known as 'tiled'.  The window manager has a strategy for determining the size and position relative to the other active windows.  Vertical and horizontal orientation can be configured with  `⊞ Win`-`h` for a horizontal layout, and  `⊞ Win`-`v` can be used for vertical layouts.  Flipping between horizontal and vertial layouts on a screen is a simple way of getting the basic layout you may desire.  From thre resizing and moving windows may be needed for an exact layout.

### Resizing Windows

`⊞ Win`-`r` will cause Regolith to enter window size mode.  You'll note a text message on the bar, "resize" when this mode is active.  After pressing `⊞ Win`-`r` use the arrow keys to change the size of the active window.  Press `enter` or `escape` to exit resize mode.

### Moving Windows

`⊞ Win`-`shift`-`<arrow key>` is used to move the active window on the screen relative to other windows on the same screen.  `⊞ Win`-`shift`-`<workspace number>` is used to move windows among workspaces.

## System Status

On the right side of the bar are a few system statistics that are periodically updated.  From left to right; first is system load, then battery status, (if a battery is detected on the system) followed by the date and time.

## System Configuration and Management

The Setting app can be launched via `⊞ Win`-`space` and then typing "settings".  This application is the UI for configuring the computer.  Connecting to wifi access points, configuring monitors, configuring power saving policy, and similar tasks can be achieved from this application.

## Logging In and Out

When logging in, if Regolith was installed via the PPA rather than the LiveCD, upon the first login after installation you must specify the Regolith session at the login screen.  This is done by clicking the small gear icon near the login button and selecting "Regolith".  This step isn't required when using Regolith from the LiveCD as the default Ubuntu session has been removed.  To log out, `⊞ Win`-`shift`-`e` will cause you to immediately log out of your session.  `⊞ Win`-`escape` will lock the screen.  `⊞ Win`-`shift`-`s` will cause the system to enter sleep mode.
