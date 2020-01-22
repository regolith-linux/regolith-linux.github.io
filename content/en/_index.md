+++
title = "Regolith Linux"
linkTitle = "Regolith Linux"

+++
{{< blocks/cover image_anchor="top" height="full" >}}
{{< img regolith-title.png "Regolith Linux" >}}

<p class="lead m-5">Regolith is a modern desktop environment that saves you time by reducing the clutter and ceremony that stand between you and your work. Built on top of Ubuntu and GNOME, Regolith stands on a well-supported and consistent foundation.</p>

<div class="row">
  <div class="col-sm-8">{{< img screenshot-intro.png "Regolith Linux" >}}</div>
  <div class="col-sm-4">
    <div class="mx-auto">
    <a class="btn btn-lg btn-secondary mr-3 mb-4" href="https://github.com/google/docsy-example">
      Get Regolith <i class="fas fa-cloud-download-alt ml-2 "></i>
    </a>
    <a class="btn btn-lg btn-primary mr-3 mb-4" href="{{< relref "/docs" >}}">
      Documentation <i class="fas fa-book-reader ml-2"></i>
    </a>
</div>
</div>
    <div class="mx-auto mt-5">
      {{< blocks/link-down color="white" >}}
  </div>
{{< /blocks/cover >}}

{{< blocks/section color="white" >}}
<div class="container">
  <div class="row pb-5">
    <div class="col my-auto border rounded p-3">
      <p>Upon login, Regolith is relatively free of clutter.  A collapsible bar at the bottom provides important information such as the time and active workspace.</p>
    </div>
    <div class="col d-flex">
      <p>{{< screenshot screenshot-empty.png "Empty Desktop" >}}</p>
    </div>    
    <div class="row pb-5 pt-5">
      <div class="col">
        <p>{{< screenshot screenshot-terminal.png "Single Terminal" >}}</p>
      </div>
      <div class="col my-auto border rounded p-3">
        <p>For those that work in the terminal, pressing <span class="text-nowrap"><span class="badge badge-warning">super</span> <span class="badge badge-warning">enter</span></span> is all it takes to get to business.</p>
      </div>
    </div>
    <div class="row pb-5">
      <div class="col d-flex my-auto border rounded p-3">
        <p>Need more terminals?  Toggle between horizontal and vertical layouts with <span class="text-nowrap"><span class="badge badge-warning">super</span> <span class="badge badge-warning">backspace</span></span>.</p>
      </div>
      <div class="col d-flex">
        <p>{{< screenshot screenshot-terminals.png "Terminals" >}}</p>
      </div>
    </div>
    <div class="row pb-5">
      <div class="col d-flex">
        <p>{{< screenshot screenshot-rofi.png "Launch Apps" >}}</p>
      </div>
      <div class="col d-flex my-auto border rounded p-3">
        <p>Launching apps is as simple as <span class="text-nowrap"><span class="badge badge-warning">super</span> <span class="badge badge-warning">space</span></span>, type a few letters of the app you're looking for and press <span class="badge badge-warning">enter</span> to launch it:</p>
      </div>
    </div>
    <div class="row pb-5">
      <div class="col d-flex my-auto border rounded p-3">
        <p>Gnome Flashback provides consistent and simple system management. Tweak your UI, auto mount your USB drives, connect to wireless networks.</p>
      </div>
      <div class="col d-flexr">
        <p>{{< screenshot screenshot-gnome.png "GNOME system admin" >}}</p>
      </div>
    </div>
    <div class="row pb-5">
      <div class="col d-flex">
        <p>{{< screenshot screenshot-conky.png "Shortcuts" >}}</p>
      </div>
      <div class="col d-flex my-auto border rounded p-3">
        <p>Toggle an overlay via <span class="text-nowrap"><span class="badge badge-warning">super</span> <span class="badge badge-warning">?</span></span> that presents the most important keybindings until they become muscle-memory.</p>
      </div>
    </div>
    <div class="row pb-5">
      <div class="col d-flex my-auto border rounded p-3">
        <p>Got a lot going on?  Quickly find the window you're looking for via <span class="text-nowrap"><span class="badge badge-warning">super</span> <span class="badge badge-warning">ctrl</span> <span class="badge badge-warning">space</span></span> or navigate over workspaces with <span class="text-nowrap"><span class="badge badge-warning">super</span> <span class="badge badge-warning">[0 - 19]</span></span>.</p>
      </div>
      <div class="col d-flex">
        <p>{{< screenshot screenshot-window.png "Shortcuts" >}}</p>
      </div>
    </div>
    <div class="row">
      <div class="col d-flex">
        <p>{{< screenshot screenshot-develop.png "Window Management" >}}</p>
      </div>
      <div class="col d-flex my-auto border rounded p-3">
        <p>Waste no space on frivolous UI and take advantage of every pixel without micro-managing your window layouts.</p>
      </div>
    </div>
  </div>
</div>
{{< /blocks/section >}}
{{< blocks/section color="orange">}}
### <i class="fas fa-info-circle pr-3"></i>What Makes Regolith Different
- Delivers a desktop with a functional yet minimal user interface that can be customized and expanded as needed.
- Provides GNOME's system management features with <a class="text-light bg-dark" href="https://i3wm.org/">i3-wm</a>'s productive workflow.
- Enables new users a fast and fun way to try out a <a class="text-light bg-dark" href="https://opensource.com/article/18/8/i3-tiling-window-manager">tiling window manager</a>.
- Supports <a class="text-light bg-dark" href="https://github.com/regolith-linux/regolith-desktop/wiki/Customize">easy customization</a> and <a class="text-light bg-dark" href="https://www.reddit.com/r/unixporn">ricing</a> via a consistent <a class="text-light bg-dark" href="https://github.com/regolith-linux/regolith-styles/blob/master/Xresources/root">Xresource configuration</a>.
- Relies on <a class="text-light bg-dark" href="https://snapcraft.io/store">Ubuntu's app store</a> and <a class="text-light bg-dark" href="https://packages.ubuntu.com/">package repositories</a> for a large, high quality selection of software.
- Built to be taken apart. Swap in your own UI components easily.
- Ships with a toggle overlay of basic keybindings to make getting started easier.
- Provides a <a class="text-light bg-dark" href="https://github.com/regolith-linux/regolith-builder/blob/master/build.sh">build script</a> and <a class="text-light bg-dark" href="https://github.com/regolith-linux/regolith-builder/blob/master/package-model.json">package metadata</a> to allow users to easily fork the desktop environment and distribution. 
{{< /blocks/section >}}
{{< blocks/section color="white">}}
### <i class="fas fa-user-friends pr-3"></i>Credits
<div class="container-fluid">
  <div class="row pl-0 align-items-center">
    <div class="col-5 col-md-0">
      Regolith is more curation than creation.  Here are some of the notable people and entities that produced unaffiliated work independently from which Regolith is based.
    </div>
    <div class="col-6">
      <div class="container">
        <div class="row">
          <div class="col-lg"><a href="https://i3wm.org">Michael Stapelberg</a> and <a href="https://github.com/Airblader/i3">Ingo Bürk</a></div>
          <div class="col-sm">Desktop UI</div>
        </div>
        <div class="row">
          <div class="col-lg"><a href="https://github.com/davatorium/rofi">Dave Davenport</a></div>
          <div class="col-sm">Desktop UI</div>
        </div>
        <div class="row">
          <div class="col-lg"><a href="https://github.com/yshui/compton">yshui</a></div>
          <div class="col-sm">Desktop UI</div>
        </div>
        <div class="row">
          <div class="col-lg"><a href="https://wiki.gnome.org/Projects/GnomeFlashback">Alberts Muktupāvels</a></div>
          <div class="col-sm">Desktop UI</div>
        </div>
        <div class="row">
          <div class="col-lg"><a href="https://github.com/jcstr">Jesús Castro</a> and <a href="https://github.com/deuill">Alex Palaistras</a></div>
          <div class="col-sm">Desktop UI</div>
        </div>
        <div class="row">
          <div class="col-lg"><a href="https://github.com/vivien/i3blocks">Vivien Didelot</a></div>
          <div class="col-sm">Desktop UI</div>
        </div>
        <div class="row">
          <div class="col-lg"><a href="https://github.com/arcticicestudio">Arctic Ice Studio</a> and <a href="https://ethanschoonover.com/solarized/">Ethan Schoonover</a></div>
          <div class="col-sm">Colors</div>
        </div>
        <div class="row">
          <div class="col-lg"><a href="http://www.alastairreynolds.com/">Alastair Reynolds</a></div>
          <div class="col-sm">Proper Nouns</div>
        </div>
        <div class="row">
          <div class="col-lg"><a href="https://github.com/EliverLara/Nordic">Eliver Lara</a></div>
          <div class="col-sm">Theme</div>
        </div>
        <div class="row">
          <div class="col-lg"><a href="https://snwh.org/paper">Sam Hewitt</a></div>
          <div class="col-sm">Icons</div>
        </div>
        <div class="row">
          <div class="col-lg"><a href="https://st.suckless.org">suckless.org</a></div>
          <div class="col-sm">Terminal</div>
        </div>
        <div class="row">
          <div class="col-lg"><a href="http://wallpaper-site.webflow.io/">Psiu Puxa</a>,<a href="https://unsplash.com/photos/C0OD8OM-oM0">Lucas Bellator</a>, and <a href="https://unsplash.com/photos/xnqVGsbXgV4">Luca Bravo</a></div>
          <div class="col-sm">Artwork</div>
        </div>
        <div class="row">
          <div class="col-lg"><a href="https://launchpad.net/cubic">PJ Singh</a></div>
          <div class="col-sm">Infrastructure</div>
        </div>
        <div class="row">
          <div class="col-lg"><a href="https://canonical.com">Canonical</a> and <a href="https://github.com">GitHub</a></div>
          <div class="col-sm">Infrastructure</div>
        </div>
      </div>
    </div>
  </div>
</div>

{{< /blocks/section >}}