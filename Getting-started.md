# Applying your first desktop
> IMPORTANT: Through this process, you will end up overwriting your current configuration files under `~/.config` with the desktop specific ones.
>
> Please, backup your files before continuing.

## Desktop resources
To see information about all available desktops and **detailed installation instructions** go to [Gtheme-Desktops →](https://github.com/daavidrgz/gtheme-desktops).

In this example, we are going to install the [Simple desktop→](https://github.com/daavidrgz/gtheme-desktops/tree/main/simple).
In that link you can find all desktop dependencies and a *copy and paste* experience for those who are using **Arch Linux**.

## Apply the desktop

After the dependency installation process, it's time to apply the desktop using gtheme. There are two approaches:

* Using the **CLI**: 

```bash
gtheme desktop apply simple
```

* Using the **TUI**:

Run `gtheme` without arguments, move to *simple* desktop and press `enter`.

> IMPORTANT: Please, if your are installing your first desktop, you **need to reboot** your computer after applying it.

Moreover, keep in mind that you must select the Desktop Environment (in our case is bspwm) in your Display Manager (a.k.a. login screen).

# Applying your first theme

At this point, you should have installed a desktop (otherwise it will presumably not work).

As well as before, there are two different methods to apply a theme:

* Using the **CLI**:

```bash
gtheme theme apply {theme}
```

* Using the **TUI**:

Run `gtheme` and press `tab` to switch to the *fav-themes/themes view*. Press `right` or `d` to select the right panel and press `enter` to apply a theme.

Some applications **should now restart** and apply the selected theme's colors. Nevertheless, there are some apps that either do not support *hot reload color change* 
or **need a manual restart**.
