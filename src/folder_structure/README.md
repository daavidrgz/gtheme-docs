# The folder structure

| **INFO:** After the installation process, gtheme files should be placed in `~/.config/gtheme`.|
| --- |
```bash
❯ tree ~/.config/gtheme
gtheme
├── global_config.json
├── user_settings.toml
├── desktops/
├── themes/
└── wallpapers/
```

Here we can see a `themes` and a `desktop` folder where all color schemes and dotfiles are stored, respectively. You may see also a `wallpapers` folder if you choose to download them.

In addition, we can find two more files:

- `global_config.json`, that is an internal gtheme configuration file and **should not be modified**.
- `user_settings.toml`, that is were all user preferences (font size, monitor, terminal, browser) are saved. To manage this file see `gtheme config help`

> To check more in depth the specification of the files that are stored in each of these folder go into their respective sections.