---
layout: page
title: Getting Started
lang: en
---

## Key Bindings

Regolith is designed for keyboard interaction.  The first time you log into a Regolith session, you'll see a listing of the most useful key bindings on the right-hand side of the screen.  This helper will not appear by default on subsequent logins, but you can view them at any time with the `⊞ Win`-`?` sequence while on an empty workspace.  A full list of keybindings is [available here]({% link keybindings.md %}).

## Launching Programs

In Regolith Linux, applications are launched via the `⊞ Win`-`space` sequence.  A full screen dialog is presented.  Begin typing the app or command and the list will filter as you type.  Launch the app by selecting it and pressing `enter`.

The terminal, browser, and settings applications are special because they can be directly launched from a keybinding as well as from the application launcher.

| Application | Key Binding |
|-------------|-------------|
|Terminal|`⊞ Win`-`enter`|
|Browser|`⊞ Win`-`shift`-`enter`|
|Configure Bluetooth|`⊞ Win`-`b`|
|Configure Displays|`⊞ Win`-`d`|
|Configure Network|`⊞ Win`-`n`|
|Configure Power|`⊞ Win`-`p`|
|Configure Sound|`⊞ Win`-`s`|
|Configure Wifi|`⊞ Win`-`w`|

### Installing Software

Running the `software` from app launcher will load the Ubuntu app store.  The terminal can also be used to install software, for example `sudo apt install vim` will install the vim editor.

### Terminal Commands

To page up past the top of the screen to see the buffered text, use `shift`-`page up`.  To adjust the font size in the active terminal, use `shift`-`ctrl`-`page up` `shift`-`ctrl`-`page down`.  To cycle between light and dark Solarized themes, press `F6`.

## Workspaces

Stacks of overlapping windows is something Regolith avoids.  In tiling window systems, it is common to arrange windows into groupings of workspaces.  These can be thought of as virtual screens. These workspaces are used to group and organize work, depending on how you prefer it.  Perhaps by program, task, or mood ~ it's up to you!  In traditional window systems, you would search out the window you need from the stack, or use a dock application.  In Regolith, you navigate to the workspace that contains the window, or use  `⊞ Win`-`w` to explicitly select the window from the dialog.

The currently active workspace and all workspaces that you have open will be visible as a series of indexed colored boxes at the lower left part of the screen.  The active workspace will be highlighted.  To switch to a specific workspace, enter  `⊞ Win`-`<workspace number>`.  For example, to move to workspace 3, enter  `⊞ Win`-`3`.  Relative navigation can be performed with  `⊞ Win`-`tab` (next) and  `⊞ Win`-`shift`-`tab` (previous).

## Managing Windows

As you launch more applications in a given workspace, the window manager will re-arrange the existing windows such that all windows are visible without overlap, also known as 'tiled'.  The window manager has a strategy for determining the size and position relative to the other active windows.  Layout mode can be toggled between horizontal and vertical modes with `⊞ Win`-`backspace`.  Flipping between horizontal and vertical layouts before launching new windows is a simple way of building the window layout you desire.  Resizing and moving windows can also be needed for an exact layout.  See below for resize mode.  To adjust the distance between windows (gaps) on the active workspace, use `⊞ Win`-`-` and `⊞ Win`-`+`.

### Resizing Windows

`⊞ Win`-`r` will cause Regolith to enter window size mode.  You'll note a text message on the bar, "resize" when this mode is active.  After pressing `⊞ Win`-`r` use the arrow keys to change the size of the active window.  Press `enter` or `escape` to exit resize mode.

### Moving Windows

`⊞ Win`-`shift`-`<arrow key>` is used to move the active window on the screen relative to other windows on the same screen.  `⊞ Win`-`shift`-`<workspace number>` is used to move windows among workspaces.

## System Status

On the right side of the bar are a few system statistics that are periodically updated.  From left to right; first is system load, then battery status, (if a battery is detected on the system) followed by the date and time.

## System Configuration and Management

The Setting app can be launched via `⊞ Win`-`c` (or `⊞ Win`-`space` and then typing "settings" to launch the control pannel by name).  This application is the UI for configuring the computer.  Connecting to wifi access points, configuring monitors, configuring power saving policy, and similar tasks can be achieved from this application.

## Logging In and Out

When logging in, if Regolith was installed via the PPA rather than the LiveCD, upon the first login after installation you must specify the Regolith session at the login screen.  This is done by clicking the small gear icon near the login button and selecting "Regolith".  This step isn't required when using Regolith from the LiveCD as the default Ubuntu session has been removed.  To log out, `⊞ Win`-`shift`-`e` will cause you to immediately log out of your session.  `⊞ Win`-`escape` will lock the screen.  `⊞ Win`-`shift`-`s` will cause the system to enter sleep mode.

## Regolith Interface Tour

### Desktop Bar

The only UI widget persistently on screen.  This shows your workspace state as well as some system information such as CPU load and the date.

### Windows

Essentially as is in other graphical windowing environments such as Mac OS X or Windows, but without titles or decorations. Their size and position are generally managed via the keyboard,
although you can use a mouse of you prefer.  More details below about window management.

### Workspaces

A workspace is simply a computer screen's worth of windows.  By default Regolith provides 10 workspaces to manage your work in.

### Launcher

A full-screen dialog that allows you to launch programs or select windows.

### Notifications

A transient window at the top right of the screen shows notifications from applications.

### Keybinding Helper

Upon first login, a cheat-sheet of keybindings is launched on the right side of the screen.  Subsequent logins do not show the shortcuts, but they can be viewed on the desktop with the `⊞
Win`-`?` key sequence.

## Digging Deeper

i3-wm provides an excellent [user manual](https://i3wm.org/docs/userguide.html) for those wishing to customize their keybindings or other window behavior.  Additionally the [i3-wm FAQ page on Reddit](https://www.reddit.com/r/i3wm/) is a great resource for asking questions and searching for answers.
