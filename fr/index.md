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
- Supporte [la personnalisation](/configure.html) et le [« ricing »](https://www.reddit.com/r/unixporn/) grâce à une [configuration Xresource](https://github.com/regolith-linux/regolith-styles/blob/master/Xresources/root).
- Se base sur [l'app store Ubuntu](https://snapcraft.io/store) et ses dépôts pour offrir une large gamme de logiciels et d'applications.
- Offre un bureau avec un petit nombre de fonctionnalités qui peuvent être personnalisées et étoffées si nécessaire.
- Affiche, au premier démarrage, une sélection de raccourcis clavier pour naviguer entre les fenêtres, lancer des applications et gérer votre système.
- Fournit un [script de build](https://github.com/regolith-linux/regolith-desktop/blob/master/build.sh) et les [métadonnées des paquets](https://github.com/regolith-linux/regolith-desktop/blob/master/package-model.json) afin de permettre aux utilisateurs de forker l'environnement de bureau et la distribution.

### Obtenir Regolith

Testez et installez Regolith directement avec le [LiveCD](https://sourceforge.net/projects/regolith-linux/), ou, si votre ordinateur tourne déjà sous Ubuntu*, en ajoutant simplement une nouvelle session en installant le paquet `regolith-desktop` depuis le [PPA Regolith](https://launchpad.net/~kgilmer/+archive/ubuntu/regolith-stable). Voir la [page d'installation](https://github.com/regolith-linux/regolith-desktop/wiki/Install-Regolith) pour plus de précisions.

<sub>*Disponible pour Ubuntu 18.04 LTS et Ubuntu 19.04</sub>

### Prochaines étapes

Jetez un œil sur notre [guide de démarrage](/getting_started.html) pour obtenir plus d'informations sur Regolith Linx, consultez les [dernières nouvelles](/news.html), ou bien lisez notre [guide de configuration](/configure.html) pour apprendre à personnaliser votre bureau selon vos goûts. Les [raccourcis clavier](/keybindings.html) sont la manière la plus rapide d'être productif dans ce nouvel environnement.

### Credits

Regolith est avant tout une sélection d'outils existants et non une création à partir de rien. Voici une liste de quelques personnes et projets qui ont créé les outils sur lesquels Regolith se construit.


|---------|----------|
| [Michael Stapelberg](https://i3wm.org) et [Ingo Bürk](https://github.com/Airblader/i3) | Desktop UI
| [Dave Davenport](https://github.com/davatorium/rofi) | Desktop UI
| [yshui](https://github.com/yshui/compton) | Desktop UI
| [Alberts Muktupāvels](https://wiki.gnome.org/Projects/GnomeFlashback) | Desktop UI
| [Vivien Didelot](https://github.com/vivien/i3blocks) | Desktop UI
| [Arctic Ice Studio](https://github.com/arcticicestudio) et [Ethan Schoonover](https://ethanschoonover.com/solarized/) | Colors
| [Eliver Lara](https://github.com/EliverLara/Nordic) | Theme
| [Sam Hewitt](https://snwh.org/paper) | Icons
| [suckless.org](https://st.suckless.org) | Terminal
| [Lucas Bellator](https://unsplash.com/photos/C0OD8OM-oM0) and [Luca Bravo](https://unsplash.com/photos/xnqVGsbXgV4) | Wallpaper
| [PJ Singh](https://launchpad.net/cubic) | Infrastructure
| [Canonical](https://canonical.com) and [GitHub](https://github.com) | Infrastructure
