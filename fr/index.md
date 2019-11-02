---
layout: default
title: 
lang: fr
---
Regolith est un environnement de bureau qui s'écarte complètement des interfaces Mac ou Windows afin de fournir un bureau à la fois beau et efficace. Basé sur Ubuntu et GNOME, Regolith s'appuie sur des fondations solides.

<a href="/assets/screenshot-intro.png"><img class="screenshot" alt="Intro Screenshot" src="/assets/screenshot-intro.png"/></a>

[Visual tour of Regolith](/visual-tour.html)

### En quoi Regolith est-il différent ?

- Fournit les fonctionnalités système de GNOME avec un workflow [i3](https://i3wm.org/).
- Permet aux nouveaux utilisateurs de tester rapidement un [tiling window manager](https://opensource.com/article/18/8/i3-tiling-window-manager).
- Supporte [la personnalisation](https://github.com/regolith-linux/regolith-desktop/wiki/Customize) et le [« ricing »](https://www.reddit.com/r/unixporn/) grâce à une [configuration Xresource](https://github.com/regolith-linux/regolith-styles/blob/master/Xresources/root).
- Se base sur [l'app store Ubuntu](https://snapcraft.io/store) et ses dépôts pour offrir une large gamme de logiciels et d'applications.
- Offre un bureau avec un petit nombre de fonctionnalités qui peuvent être personnalisées et étoffées si nécessaire.
- Affiche, au premier démarrage, une sélection de raccourcis clavier pour naviguer entre les fenêtres, lancer des applications et gérer votre système.
- Fournit un [script de build](https://github.com/regolith-linux/regolith-desktop/blob/master/build.sh) et les [métadonnées des paquets](https://github.com/regolith-linux/regolith-desktop/blob/master/package-model.json) afin de permettre aux utilisateurs de forker l'environnement de bureau et la distribution.

### Obtenir Regolith

Testez et installez Regolith directement avec le [LiveCD](https://sourceforge.net/projects/regolith-linux/), ou, si votre ordinateur tourne déjà sous Ubuntu*, en ajoutant simplement une nouvelle session en installant le paquet `regolith-desktop` depuis le [PPA Regolith](https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-stable). Voir la [page d'installation](https://github.com/regolith-linux/regolith-desktop/wiki/Install-Regolith) pour plus de précisions.

<sub>*Disponible pour Ubuntu 18.04 LTS et Ubuntu 19.04</sub>

### Prochaines étapes

Jetez un œil sur notre [guide de démarrage](https://github.com/regolith-linux/regolith-desktop/wiki/Getting-Started) pour obtenir plus d'informations sur Regolith Linx, consultez les [dernières nouvelles](/news.html), ou bien lisez notre [guide de configuration](https://github.com/regolith-linux/regolith-desktop/wiki/Customize) pour apprendre à personnaliser votre bureau selon vos goûts. Les [raccourcis clavier](https://github.com/regolith-linux/regolith-desktop/wiki/Keybindings) sont la manière la plus rapide d'être productif dans ce nouvel environnement.

### Credits

Regolith est avant tout une sélection d'outils existants et non une création à partir de rien. Voici une liste de quelques personnes et projets qui ont créé les outils sur lesquels Regolith se construit.

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
