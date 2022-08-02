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

### Gtheme folder

#### Extras

Here are located all scripts that are executed after applying a theme and the extra is actived. If you need parameters, the name should match the one that appears in the theme toml (extras secion). They are bash scripts, completely unrestricted (the user who will execut them won't be root)

See examples [vscode extra script](github/)

Dont forget to give themes execution permissions.

#### Patterns

Complex file, link to [Pattern Specification](Desktop-specification.md)

#### Post-Scripts

Here are saved all script that are executed after the pattern was filled. They can be used to force a reload to show the color change.

The names of the script files should match the pattern names!!

They recive as first parameter the output-file path specified in the pattern.

There is a special script called `desktop-exit.sh` that is executed every time you change from one desktop to another one. It let us be agnostic of the current Window Manager that is being used and experiment a better experience when switching desktops.

### .config folder

Here are stored all desktop configuration files. Some of them can have a pattern, but is recommended to mantain them.
