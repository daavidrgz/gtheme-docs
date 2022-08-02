# Getting started

## Applying your first desktop


| **WARNING:** Through this process, you will end up overwriting your current configuration files under `~/.config` with the desktop specific ones. Please, backup your files before continuing! |
| --- |

### Desktop resources

To see information about all available desktops and **detailed installation instructions** go to [Gtheme-Desktops](https://github.com/daavidrgz/gtheme-desktops).

In this example, we are going to install the [Simple](https://github.com/daavidrgz/gtheme-desktops/tree/bec9b141809b97d0b8ab52ec0b521dd17a4e2463/simple) desktop. In that link you can find all desktop dependencies and a copy and paste experience for those who are using Arch Linux.

### Apply the desktop

After the dependency installation process, it's time to apply the desktop by using gtheme. There are two approaches:

* Using the CLI **->** Run `gtheme desktop apply simple`
* Using the TUI **->** Run `gtheme` without arguments, move to _simple_ desktop and press `enter`


| **WARNING:** If your are installing your first desktop, you will need to reboot your computer after applying it. |
| --- |

\

| **INFO:** Keep in mind that you must select the Desktop Environment (in our example is bspwm) in your Display Manager (a.k.a. login screen). |
| --- |

## Applying your first theme

At this point, **you should have a desktop installed** (otherwise it will presumably not work).

As we mentioned before, there are two different methods for applying a theme:

* Using the CLI **->** Run `gtheme theme apply {theme}`
* Using the TUI **->** Run `gtheme` and press `tab` to switch to the _fav-themes/themes_ view. Search for the theme you want to apply and hit `enter`


| **INFO:** Some applications should now restart and apply the selected theme's colors. Nevertheless, there are some apps that either do not support _hot reload color change_ or need a manual restart (this is the main reason pattern postcripts exists) |
| --- |
