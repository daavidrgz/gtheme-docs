# Desktop specification

As mentioned before, the desktop structure is the following:

```bash
❯ tree simple -L 1 -a
simple
├── desktop_config.json
├── desktop_info.toml
├── .config/
└── gtheme/
```

You can easily create a new desktop skeleton running `gtheme desktop new-skeleton <DESKTOP_NAME>`

## Gtheme folder

### Extras

Here are located all extra scripts that are executed after applying a theme. See [Extra Specification](folder_structure/extra_especification.md)

### Patterns

Here are located all patterns. It is a complex file, see [Pattern Specification](folder_structure/pattern-specification.md)

### Post-Scripts

Here are stored all script that are executed after a pattern is filled. They can be used to force a reload to show the color change. See [PostScript Specification](folder_structure/postscript_specification.md)

**PostScripts are optional**, not all patterns need to have a PostScript associated.


## .config folder

Here are stored all desktop configuration files that goes under `$HOME/.config`. Some of them can have a pattern, so it is not needed to store patterns here, but is recommended to keep a filled pattern here, in case of something brokes, the system could be recovered easily by the user.
