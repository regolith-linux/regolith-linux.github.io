+++
title = "Regolith Linux"
linkTitle = "Regolith Linux"

+++
{{< blocks/cover image_anchor="top" height="full" >}}
{{< img regolith-title.png "Regolith Linux" >}}

<p class="lead m-5">Regolith is a modern desktop environment that saves you time by cutting out the clutter and ceremony that stand between you and your work. Built on top of Ubuntu and GNOME, Regolith stands on a well-supported and consistent foundation.</p>

<div class="row">
  <div class="col-sm-8">{{< img screenshot-intro.png "Regolith Linux" >}}</div>
  <div class="col-sm-4">
    <div class="mx-auto">
    <a class="btn btn-lg btn-primary mr-3 mb-4" href="{{< relref "/docs" >}}">
      Documentation <i class="fas fa-arrow-alt-circle-right ml-2"></i>
    </a>
    <a class="btn btn-lg btn-secondary mr-3 mb-4" href="https://github.com/google/docsy-example">
      Get Regolith <i class="fab fa-github ml-2 "></i>
    </a>
</div>
</div>
    <div class="mx-auto mt-5">
      {{< blocks/link-down color="info" >}}
  </div>
{{< /blocks/cover >}}

{{< blocks/section color="white" >}}
<div class="container">
  <div class="row">
    <div class="col my-auto">
      <p>Upon login, Regolith is relatively free of clutter.  A bar at the bottom provides important information such as the time and active workspace.</p>
    </div>
    <div class="col d-flex">
      <p>{{< screenshot screenshot-empty.png "Empty Desktop" >}}</p>
    </div>
    <br/>
    <div class="row">
      <div class="col">
        <p>{{< screenshot screenshot-terminal.png "Single Terminal" >}}</p>
      </div>
      <div class="col my-auto">
        <p>For those that work in the terminal, pressing <span class="text-nowrap"><span class="badge badge-warning">super</span> <span class="badge badge-warning">enter</span></span> is all it takes to get to business.</p>
      </div>
    </div>
    <br/><div class="row">
      <div class="col d-flex my-auto">
        <p>Need more terminals?  Toggle between horizontal and vertical layouts with <span class="text-nowrap"><span class="badge badge-warning">super</span> <span class="badge badge-warning">backspace</span></span>.</p>
      </div>
      <div class="col d-flex">
        <p>{{< screenshot screenshot-terminals.png "Terminals" >}}</p>
      </div>
    </div>
    <br/><div class="row">
      <div class="col d-flex">
        <p>{{< screenshot screenshot-rofi.png "Launch Apps" >}}</p>
      </div>
      <div class="col d-flex my-auto">
        <p>Launching apps is as simple as <span class="text-nowrap"><span class="badge badge-warning">super</span> <span class="badge badge-warning">space</span></span>, type a few letters of the app you're looking for and press <span class="badge badge-warning">enter</span> to launch it:</p>
      </div>
    </div>
    <br/><div class="row">
      <div class="col d-flex my-auto">
        <p>Gnome Flashback provides consistent and simple system management. Tweak your UI, auto mount your USB drives, connect to wireless networks.</p>
      </div>
      <div class="col d-flexr">
        <p>{{< screenshot screenshot-gnome.png "GNOME system admin" >}}</p>
      </div>
    </div>
    <br/><div class="row">
      <div class="col d-flex">
        <p>{{< screenshot screenshot-conky.png "Shortcuts" >}}</p>
      </div>
      <div class="col d-flex my-auto">
        <p>Toggle an overlay via <span class="text-nowrap"><span class="badge badge-warning">super</span> <span class="badge badge-warning">?</span></span> that presents the most important keybindings until they become muscle-memory.</p>
      </div>
    </div>
    <br/><div class="row">
      <div class="col d-flex my-auto">
        <p>Got a lot going on?  Quickly find the window you're looking for via <span class="text-nowrap"><span class="badge badge-warning">super</span> <span class="badge badge-warning">ctrl</span> <span class="badge badge-warning">space</span></span> or navigate over workspaces with <span class="text-nowrap"><span class="badge badge-warning">super</span> <span class="badge badge-warning">[0 - 19]</span></span>.</p>
      </div>
      <div class="col d-flex">
        <p>{{< screenshot screenshot-window.png "Shortcuts" >}}</p>
      </div>
    </div>
    <br/><div class="row">
      <div class="col d-flex">
        <p>{{< screenshot screenshot-develop.png "Window Management" >}}</p>
      </div>
      <div class="col d-flex my-auto">
        <p>Waste no space on frivolous UI and take advantage of every pixel without micro-managing your window layouts.</p>
      </div>
    </div>
  </div>
</div>
{{< /blocks/section >}}
{{< blocks/section color="dark">}}
### What Makes Regolith Different

- Provides GNOME's system management features with [i3](https://i3wm.org/)'s productive workflow.
- Enables new users a fast and fun way to try out a [tiling window manager](https://opensource.com/article/18/8/i3-tiling-window-manager).
- Supports [easy customization](https://github.com/regolith-linux/regolith-desktop/wiki/Customize) and [ricing](https://www.reddit.com/r/unixporn/) via a consistent [Xresource configuration](https://github.com/regolith-linux/regolith-styles/blob/master/Xresources/root).
- Relies on [Ubuntu's app store](https://snapcraft.io/store) and package repositories for a large, high quality selection of software.
- Delivers a desktop with small set of UI features that can be customized and expanded as needed.
- Ships with a toggle overlay of basic keybindings to navigate over windows, launch apps, and manage your system.
- Provides a [build script](https://github.com/regolith-linux/regolith-builder/blob/master/build.sh) and [package metadata](https://github.com/regolith-linux/regolith-builder/blob/master/package-model.json) to allow users to easily fork the desktop environment and distribution.

{{< /blocks/section >}}
{{< blocks/section >}}
### Get Regolith

Install or test drive Regolith from scratch with the [LiveCD Installer](https://sourceforge.net/projects/regolith-linux/), or if you already have an existing Ubuntu setup*, simply add it as another desktop session by installing the package `regolith-desktop` from the [Regolith PPA](https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-stable). See the [install page](https://github.com/regolith-linux/regolith-desktop/wiki/Install-Regolith) for more details.

<sub>*Ubuntu 18.04 and Ubuntu 19.04 bases available</sub>
{{< /blocks/section >}}
{{< blocks/section >}}
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
{{< /blocks/section >}}