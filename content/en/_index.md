+++
title = "Regolith Linux"
linkTitle = "Regolith Linux"

+++
{{< blocks/cover image_anchor="top" height="full" >}}
{{< img regolith-title.png "Regolith Linux" >}}

<p class="lead mt-5">Regolith is a unique desktop environment that ditches the cruft of Windows and Mac knockoffs to provide a productive and beautiful place to get work done. Built on top of Ubuntu and GNOME, Regolith stands on a stable, well-supported, and consistent foundation.</p>

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

{{< blocks/section color="dark" >}}
<div class="container">
  <div class="row">
    <div class="col d-flex justify-content-center">
      <p>Upon login, Regolith is relatively free of clutter.  A bar at the bottom provides important information such as the time and active workspace.</p>
    </div>
    <div class="col d-flex justify-content-center">
      <p>{{< screenshot screenshot-empty.png "Empty Desktop" >}}</p>
    </div>
    <br/><div class="row">
      <div class="col d-flex justify-content-center">
        <p>{{< screenshot screenshot-terminal.png "Single Terminal" >}}</p>
      </div>
      <div class="col d-flex justify-content-center">
        <p>For those that work in the terminal, pressing `super`-`enter` is all it takes to get to business:</p>
      </div>
    </div>
    <br/><div class="row">
      <div class="col d-flex justify-content-center">
        <p>Need more terminals?  Toggle between horizontal and vertical layouts with `<super>`-`<backspace>`:</p>
      </div>
      <div class="col d-flex justify-content-center">
        <p>{{< screenshot screenshot-terminals.png "Terminals" >}}</p>
      </div>
    </div>
    <br/><div class="row">
      <div class="col d-flex justify-content-center">
        <p>{{< screenshot screenshot-rofi.png "Launch Apps" >}}</p>
      </div>
      <div class="col d-flex justify-content-center">
        <p>Launching apps is as simple as `<super>`-`<space>`, type a few letters of the app you're looking for and press `<enter>` to launch it:</p>
      </div>
    </div>
    <br/><div class="row">
      <div class="col d-flex justify-content-center">
        <p>`gnome-flashback` provides consistent and simple system management.  Tweak your UI, auto mount your USB drives, connect to a wireless router.</p>
      </div>
      <div class="col d-flex justify-content-center">
        <p>{{< screenshot screenshot-gnome.png "GNOME system admin" >}}</p>
      </div>
    </div>
    <br/><div class="row">
      <div class="col d-flex justify-content-center">
        <p>{{< screenshot screenshot-conky.png "Shortcuts" >}}</p>
      </div>
      <div class="col d-flex justify-content-center">
        <p>Toggle an overlay via <super>-<?> that presents the most important keybindings until they become muscle-memory.</p>
      </div>
    </div>
    <br/><div class="row">
      <div class="col d-flex justify-content-center">
        <p>Big on multitasking?  Quickly find the window you're looking for via `<super>`-`<ctrl>`-`<space>`, or navigate over workspaces with `<super>`-`<number>`.</p>
      </div>
      <div class="col d-flex justify-content-center">
        <p>{{< screenshot screenshot-window.png "Shortcuts" >}}</p>
      </div>
    </div>
    <br/><div class="row">
      <div class="col d-flex justify-content-center">
        <p>{{< screenshot screenshot-develop.png "Window Management" >}}</p>
      </div>
      <div class="col d-flex justify-content-center">
        <p>Waste no space on frivolous UI and take advantage of every pixel without micro-managing your window layouts.</p>
      </div>
    </div>
  </div>
</div>
{{< /blocks/section >}}
{{< blocks/section >}}
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
### Next Steps

Have a look at the [Getting Started](https://github.com/regolith-linux/regolith-desktop/wiki/Getting-Started) guide to learn more about using Regolith Linux, see the [latest updates](/news.html), or check out the [configuration](https://github.com/regolith-linux/regolith-desktop/wiki/Customize) page and [list of HowTos](https://github.com/search?utf8=✓&q=org%3Aregolith-linux+HowTo+in%3Atitle&type=Wikis) to learn about how to tweak it to your liking. Also have a look at the [Keybindings](https://github.com/regolith-linux/regolith-desktop/wiki/Keybindings) to learn the quickest way around your new desktop environment.  Once you've gotten familiar with Regolith have a look at the [active RfCs](https://github.com/regolith-linux/regolith-desktop/issues?utf8=✓&q=is%3Aissue+is%3Aopen+"Request+for+Comment").
{{< /blocks/section >}}
{{< blocks/section >}}
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