---
title: "Styles"
linkTitle: "Styles"
date: 2017-01-05
weight: 2
description: >
  Details about Regolith styles.
---

As stated in the [repo readme](https://github.com/regolith-linux/regolith-styles), Regolith styles are a convention by which a set of files which define key/value pairs are loaded into memory and can be queried by `xrdb` or `xrescat`.  Xresources employes the [C preprocessor](https://en.wikipedia.org/wiki/C_preprocessor) to allow for complex behaviors such as including more files, defining constants, and conditional expressions.  In Regolith, only two preprocessor directives are used: `include` and `define`.  `include` statements are used to reference other files.  Collections of files called `looks` were covered in the previous section of this guide.  `define` statements are a little more involved.

## Defines

To maximize the re-use of theme information in Regolith, Xresources are divided into two categories of files: definition files and application files.  The definition files make heavy use of the `define` directive.  They essentially bind an abstract key, such as "blue" or "terminal font" to a literal value, such as `#0000FF` or `Source Code Pro Medium`.  In making changes to files, it's expected that these defines will change.  The user may wish to specify a different icon set, or typeface, and would do so by modifying or creating a new definition file.  Once this file is created, it needs to be referenced by a top-level Xresource file in `~/Xresource-regolith`. 

## Application Xresource files

As mentioned previously, in `/etc/regolith/styles` lives a number of Xresources, including those for specific applications such as `st` or `i3-wm`.  Opening these files will show a mapping of the abstract keys provided by the defines files to application specific keys.  In this way, the general description of the look can be mapped to any UI component or application that can read from Xresources.