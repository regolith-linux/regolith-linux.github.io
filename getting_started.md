---
layout: page
title: Getting Started
---

## Regolith Interface Tour

### Desktop Bar

The only UI widget persistently on screen.  This shows your workspace state as well as some system information such as CPU load and the date.

### Windows

Essentially as is in other graphical windowing environments such as Mac OS X or Windows, but without titles or decorations. Their size and position are generally managed via the keyboard, although you can use a mouse of you prefer.  More details below about window management.

### Workspaces

A workspace is simply a computer screen's worth of windows.  By default Regolith provides 10 workspaces to manage your work in.

### Launcher

A full-screen dialog that allows you to launch programs or select windows.

### Notifications 

A transient window at the top right of the screen shows notifications from applications.

### Keybinding Helper

Upon first login, a cheat-sheet of keybindings is launched on the right side of the screen.  Subsequent logins do not show the shortcuts, but they can be viewed on the desktop with the `⊞ Win`-`?` key sequence.

## Launching Programs

In Regolith Linux, applications are launched via the `⊞ Win`-`space` sequence.  A full screen dialog is presented.  Begin typing the app or command and the list will filter as you type.  Launch the app by selecting it and pressing `enter`.

The terminal application is special in Regolith as it can be launched with `⊞ Win`-`enter`.

### Terminal Commands

To page up past the top of the screen to see the buffered text, use `shift`-`page up`.  To adjust the font size in the active terminal, use `shift`-`ctrl`-`page up` `shift`-`ctrl`-`page down`.  To cycle between light and dark Solarized themes, press `F6`.

## Workspaces

Stacks of overlapping windows is something Regolith avoids.  In tiling window systems, it is common to arrange windows into groupings of workspaces.  These can be thought of as virtual screens. These workspaces are used to group and organize work, depending on how you prefer it.  Perhaps by program, task, or mood ~ it's up to you!  In traditional window systems, you would search out the window you need from the stack, or use a dock application.  In Regolith, you navigate to the workspace that contains the window, or use  `⊞ Win`-`w` to explicitly select the window from the dialog.

The currently active workspace and all workspaces that you have open will be visibile as a series of indexed colored boxes at the lower left part of the screen.  The active workspace will be highlighted.  To switch to a specific workspace, enter  `⊞ Win`-`<workspace number>`.  For example, to move to workspace 3, enter  `⊞ Win`-`3`.  Relative navigation can be performed with  `⊞ Win`-`tab` (next) and  `⊞ Win`-`shift`-`tab` (previous).

## Managing Windows

As you launch more applications in a given workspace, the window manager will re-arrange the existing windows such that all windows are visible without overlap, also known as 'tiled'.  The window manager has a strategy for determining the size and position relative to the other active windows.  Vertical and horizontal orientation can be configured with  `⊞ Win`-`h` for a horizontal layout, and  `⊞ Win`-`v` can be used for vertical layouts.  Flipping between horizontal and vertial layouts on a screen is a simple way of getting the basic layout you may desire.  From there resizing and moving windows may be needed for an exact layout.  To adjust the distance between windows on the active workspace, use `⊞ Win`-`-` and `⊞ Win`-`+`.

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
