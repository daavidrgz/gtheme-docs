After the installation process, gtheme files should be placed in `~/.config/gtheme`, where you can see a `themes` and a `desktop` folder
where all color schemes and dotfiles are stored, respectively. You may see also a `wallpapers` folder if you
choose to download them.

```bash
❯ tree gtheme
gtheme
├── global_config.json
├── user_settings.toml
├── desktops/
├── themes/
└── wallpapers/
```

In addition, here we can find two more files:
* A `global_config.json`, that is an internal gtheme configuration file and **should not be modified**.
* A `user_settings.toml`, that is were all user preferences (font size, terminal, browser) are saved. This can be directly modified
but is not recommended as it exists a command in order to do that.

### Desktops
Inside a `desktop` folder, you'll find many different things:

```bash
❯ tree simple -L 1 -a
simple
├── desktop_config.json
├── desktop_info.toml
├── README.md
├── .config/
├── fonts/
├── gtheme/
└── screenshots/
```

We can see two files:
* A `desktop_config.json`, that is a file managed by gtheme and **should not be modified**.
* A `desktop_info.toml`, which contains a simple description of the desktop.

Furthermore, we can find more folders that are more in depth explained in the [Desktop Specification](github) section.

### Themes
In this folder reside all saved color themes.

```bash
❯ tree themes
themes
├── 3024-Day.json
├── 3024-Light.json
├── 3024-Night.json
...
├── XTerm.json
├── Yousai.json
└── Zenburn.json
```

### Wallpapers
This folder contains all the wallpapers that some theme use as default. You can add or remove what you want and reorganize them aa you want.
