---
layout: page
title: Contribute
lang: en
---

Ways to contribute to Regolith Linux:

## Join our Slack channel

There is a link in the menu on the left of this website.

## Install the regolith-unstable PPA

A lot of development is done in the unstable PPA and then tested before pushed to production in the stable PPA. The following steps are how the unstable PPA is added:

From your existing Ubuntu 18.04 (Bionic) or 19.04 (Disco) system, perform the following installation steps: 

1. Open a terminal, and enter: <br/>`sudo add-apt-repository -y ppa:kgilmer/regolith-unstable`
2. After the sync completes, enter: <br/>`sudo apt install regolith-desktop`
3. The following command will need to be ran <br/>`sudo apt update && sudo apt upgrade && sudo apt full-upgrade`
4. Some packages will be upgraded.  When this completes, reboot.

## Code and Documenation

As an open source project, Regolith Linux is open to anyone to extend, fork, or modify as they see fit.  People are welcome to join as contributors to the project if interested. Please file an issue describing the change you'd like to be made to Regolith before doing the work however, so we do not waste your time. Also take a look at [the roadmap](https://regolith-linux.org/news.html#roadmap) and [list of issues looking for help](https://github.com/regolith-linux/regolith-desktop/labels/help%20wanted) to see what is actively being developed and future plans.
