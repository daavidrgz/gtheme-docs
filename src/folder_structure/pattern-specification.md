# Pattern specification

Patterns files must be located on `{/path/to/desktop}/gtheme/patterns` and there must not be more than one pattern with the same name.

| **WARNING:** If patterns only differ on the extension, they have effectively the same name.|
| --- |

Example using the [Alacritty](https://github.com/daavidrgz/gtheme-desktops/blob/main/simple/gtheme/patterns/alacritty.pattern) config file:

```yml
<[output-file]>=~/.config/alacritty/alacritty.yml
# <[theme-name]>

font:
  normal:
    family: <[default-font|DejaVuSansMono Nerd Font]>
  bold:
    family: <[default-font|DejaVuSansMono Nerd Font]>
  italic:
    family: <[default-font|DejaVuSansMono Nerd Font]>
  size: <[default-font-size|12]>

colors:
  cursor:
    text: '0x<[foreground]>'
    cursor: '0x<[cursor]>'
  primary:
    background: '0x<[background]>'
    foreground: '0x<[foreground]>
...
```

## Properties

All properties are accessed with the pattern `<[some-property]>`. Those properties will be replaced with the value of the associated key on a theme or the `user_settings` file.

You can also **specify a default value for some properties** with `<[some-property|default-value]>`. This can be used to prevent crashes when that property is not present in the `user_settings` file.

In addition, there are **two special properties**:

* `<[output-file]>=/path/to/write`: This is a **mandatory** property that it's necessary in order to know where to place the filled pattern. It has to be in **its own line, with nothing else**.

| **INFO:** As opposed to other properties, `output-file` will not be filled on the generated output and the line were it was located will be deleted.|
| --- |

* `<[theme-name]>`: Unlike the previous property, this one is **optional.** It simply uses the key `name` on the theme file to fill the property.

## Modules and sub-modules

If you have a program that is composed of **several config files**, you will also need **several pattern files**. To manage this situation, you can use the **pattern modules.**

Inside of `patterns/` folder, you can create **another folder** that:

* It's name will be the one of the module.
* It can contain any number of patterns (or patterns modules) inside that will be consider sub-modules.
* When filling a pattern module, all of its sub-modules will be filled too.
* Enabling or disabling a module, also enables or disables all of its sub-modules.
* Submodules can be a module itself. This means that submodules are recursive.

| **WARNING:** Pattern sub-modules must follow the restrictions of regular pattern files. |
| --- |
## Pattern inversion

Some themes could have a wallpaper with color tones that conflict with text foreground color and makes reading text harder. In order to fix that, you can **invert a pattern**.&#x20;

Inverting a pattern means that `foreground` color will be switched with `background` color, and the same happens with its `selection-` variants.&#x20;

Check `gtheme pattern invert --help`.

## Tips

If you're planning to create (or port existing dotfiles) patterns, we encourage you to check already existing patterns. You can found some on the [community desktops repository](git@github.com:daavidrgz/gtheme-desktops.git)
