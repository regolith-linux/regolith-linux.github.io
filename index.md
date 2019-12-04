---
layout: default
title: 
lang: en
---
Regolith is a unique desktop environment that ditches the cruft of Windows and Mac knockoffs to provide a productive and beautiful place to get work done. Built on top of Ubuntu and GNOME, Regolith stands on a stable, well-supported, and consistent foundation.

<a href="/assets/screenshot-intro.png"><img class="screenshot" alt="Intro Screenshot" src="/assets/screenshot-intro.png"/></a>

<details>

  <summary>Visual Tour of Regolith...</summary>
  
<br/>Upon login, Regolith is relatively free of clutter.  A bar at the bottom provides important information such as the time and active workspace.

<a href="/assets/screenshot-empty.png"><img class="screenshot" alt="Empty Screenshot" src="/assets/screenshot-empty.png"/></a><br/>

For those that do most of their work in the terminal, pressing `<super>`-`<enter>` is all it takes to get to business:

<a href="/assets/screenshot-terminal.png"><img class="screenshot" alt="Terminal Screenshot" src="/assets/screenshot-terminal.png"/></a><br/>

Need more terminals?  Toggle between horizontal and vertical layouts with `<super>`-`<backspace>`:

<a href="/assets/screenshot-terminals.png"><img class="screenshot" alt="Terminals Screenshot" src="/assets/screenshot-terminals.png"/></a><br/>

Launching apps is as simple as `<super>`-`<space>`, type a few letters of the app you're looking for and press `<enter>` to launch it:

<a href="/assets/screenshot-rofi.png"><img class="screenshot" alt="Rofi Screenshot" src="/assets/screenshot-rofi.png"/></a><br/>

`gnome-flashback` provides consistent and simple system management.  Tweak your UI, auto mount your USB drives, connect to a wireless router:

<a href="/assets/screenshot-gnome.png"><img class="screenshot" alt="Gnome Screenshot" src="/assets/screenshot-gnome.png"/></a><br/>

Toggle an overlay via `<super>`-`<?>` that presents the most important keybindings until they become muscle-memory:

<a href="/assets/screenshot-conky.png"><img class="screenshot" alt="Conky Screenshot" src="/assets/screenshot-conky.png"/></a><br/>

Big on multitasking?  Quickly find the window you're looking for via `<super>`-`<ctrl>`-`<space>`, or navigate over workspaces with `<super>`-`<number>`:

<a href="/assets/screenshot-window.png"><img class="screenshot" alt="Conky Screenshot" src="/assets/screenshot-window.png"/></a><br/>

Waste no space on frivolous UI and take advantage of every pixel without micro-managing your window layouts:

<a href="/assets/screenshot-develop.png"><img class="screenshot" alt="Dev Screenshot" src="/assets/screenshot-develop.png"/></a><br/>

</details>

### What Makes Regolith Different

- Provides GNOME's system management features with [i3](https://i3wm.org/)'s productive workflow.
- Enables new users a fast and fun way to try out a [tiling window manager](https://opensource.com/article/18/8/i3-tiling-window-manager).
- Supports [easy customization](https://github.com/regolith-linux/regolith-desktop/wiki/Customize) and [ricing](https://www.reddit.com/r/unixporn/) via a consistent [Xresource configuration](https://github.com/regolith-linux/regolith-styles/blob/master/Xresources/root).
- Relies on [Ubuntu's app store](https://snapcraft.io/store) and package repositories for a large, high quality selection of software.
- Delivers a desktop with small set of UI features that can be customized and expanded as needed.
- Ships with a toggle overlay of basic keybindings to navigate over windows, launch apps, and manage your system.
- Provides a [build script](https://github.com/regolith-linux/regolith-builder/blob/master/build.sh) and [package metadata](https://github.com/regolith-linux/regolith-builder/blob/master/package-model.json) to allow users to easily fork the desktop environment and distribution.

### Get Regolith

Install or test drive Regolith from scratch with the [LiveCD Installer](https://sourceforge.net/projects/regolith-linux/), or if you already have an existing Ubuntu setup*, simply add it as another desktop session by installing the package `regolith-desktop` from the [Regolith PPA](https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-stable). See the [install page](https://github.com/regolith-linux/regolith-desktop/wiki/Install-Regolith) for more details.

<sub>*Ubuntu 18.04 and Ubuntu 19.04 bases available</sub>

### Next Steps

Have a look at the [Getting Started](https://github.com/regolith-linux/regolith-desktop/wiki/Getting-Started) guide to learn more about using Regolith Linux, see the [latest updates](/news.html), or check out the [configuration](https://github.com/regolith-linux/regolith-desktop/wiki/Customize) page and [list of HowTos](https://github.com/search?utf8=✓&q=org%3Aregolith-linux+HowTo+in%3Atitle&type=Wikis) to learn about how to tweak it to your liking. Also have a look at the [Keybindings](https://github.com/regolith-linux/regolith-desktop/wiki/Keybindings) to learn the quickest way around your new desktop environment.  Once you've gotten familiar with Regolith have a look at the [active RfCs](https://github.com/regolith-linux/regolith-desktop/issues?utf8=✓&q=is%3Aissue+is%3Aopen+"Request+for+Comment").

### Contact

<table>
  <tr>
    <td>Bug Reports</td>
    <td><a href="https://github.com/regolith-linux/regolith-desktop/issues">Github Issues</a></td>
  </tr>
  <tr>
    <td>Feature Requests</td>
    <td><a href="https://github.com/regolith-linux/regolith-desktop/issues">Github Issues</a></td>  </tr>
  <tr>
    <td>Chat</td>
    <td><a href="https://regolith-linux.herokuapp.com">Slack Channel</a></td>  </tr>
  <tr>
    <td>Change Annoucements</td>
    <td><a href="https://www.freelists.org/list/regolith-linux">Mailing List</a></td>  </tr>
</table>

### Credits

Regolith is more curation than creation.  Here are some of the notable people and entities that produced unaffiliated work **independently** from which Regolith is based.

<table>
  <tbody>
    <tr>
      <td><a href="https://i3wm.org">Michael Stapelberg</a> and <a href="https://github.com/Airblader/i3">Ingo Bürk</a></td>
      <td>Desktop UI</td>
    </tr>
    <tr>
      <td><a href="https://github.com/davatorium/rofi">Dave Davenport</a></td>
      <td>Desktop UI</td>
    </tr>
    <tr>
      <td><a href="https://github.com/yshui/compton">yshui</a></td>
      <td>Desktop UI</td>
    </tr>
    <tr>
      <td><a href="https://wiki.gnome.org/Projects/GnomeFlashback">Alberts Muktupāvels</a></td>
      <td>Desktop UI</td>
    </tr>
    <tr>
      <td><a href="https://github.com/jcstr">Jesús Castro</a> and <a href="https://github.com/deuill">Alex Palaistras</a></td>
      <td>Desktop UI</td>
    </tr>
    <tr>
      <td><a href="https://github.com/vivien/i3blocks">Vivien Didelot</a></td>
      <td>Desktop UI</td>
    </tr>
    <tr>
      <td><a href="https://github.com/arcticicestudio">Arctic Ice Studio</a> and <a href="https://ethanschoonover.com/solarized/">Ethan Schoonover</a></td>
      <td>Colors</td>
    </tr>
    <tr>
      <td><a href="https://github.com/EliverLara/Nordic">Eliver Lara</a></td>
      <td>Theme</td>
    </tr>
    <tr>
      <td><a href="https://snwh.org/paper">Sam Hewitt</a></td>
      <td>Icons</td>
    </tr>
    <tr>
      <td><a href="https://st.suckless.org">suckless.org</a></td>
      <td>Terminal</td>
    </tr>
    <tr>
      <td><a href="https://unsplash.com/photos/C0OD8OM-oM0">Lucas Bellator</a> and <a href="https://unsplash.com/photos/xnqVGsbXgV4">Luca Bravo</a></td>
      <td>Wallpaper</td>
    </tr>
    <tr>
      <td><a href="https://launchpad.net/cubic">PJ Singh</a></td>
      <td>Infrastructure</td>
    </tr>
    <tr>
      <td><a href="https://canonical.com">Canonical</a> and <a href="https://github.com">GitHub</a></td>
      <td>Infrastructure</td>
    </tr>
  </tbody>
</table>
