# Pattern specification

## File structure

Patterns files must be located on `{/path/to/desktop}/gtheme/patterns` and there
must not be more than one pattern with the same name (if patterns only differ on the extension, they have effectively the same name)

Example using the alacritty config file:

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

All properties are accessed with the pattern `<[some-property]>`. Those properties will be replaced with the value of the **associated key on applied theme OR the `user\_settings` file**.

There is a **special mandatory property** called `output-file`, it is necessary in order to know **where to write the filled pattern**. Its syntax is `<[output-file]>=/path/to/write` and it has to be on its **own line**, without anything else on that line. As opposed to other properties, this one will not be filled on the generated output and the line were it was located will be deleted. 

There is also another **special property** called `theme-name`, but this one is **optional**. It uses the key `name` on the theme file to fill the property. This is necessary if you want to keep track of which theme you've applied on a filled pattern. 

If the property is defined in the theme that you want to apply, you can reference it in the patterns. It means that you can create custom properties if you want (keep in mind that the rest of the themes should also need to have this custom property setted in order to be consistent). We **encourage to not use custom color properties** on theme files, since we don't find this neccessary at all.

There can be **user-defined optional properties** (i.e, it won't show any warning if the property is not setted while filling the pattern). Therefore, the property should have a default value to use when no value for that key is found. Its syntax is `<[some-property|default-value]>`.

## Modules and submodules

If you have a program that is composed of **several config files**, you also need **several pattern files**. To manage this situation, we got the **pattern modules**.

Inside of `patterns` folder, you can create another folder, which its name will be the one of the module. Then, you can create any number of pattern files inside that folder and will be considered **submodules** of the root module. When filling a pattern module, all of its submodules will be filled too.

The pattern module **must follow the limitations of regular pattern files** (i.e, there mustn't be more than one with the same name), but submodules can have any name you want, since we dont need its name to manage it. Enabling/Disabling a module, also enables/disables all of its submodules.

## Pattern invertion

Some themes could have a wallpaper with color tones that conflict with text foreground color and that makes reading text harder (for example, having dark text with a dark wallpaper), in order to fix that, you can **invert a pattern**. Inverting a pattern means that `foreground` color **will be switched** with `background` color, and the same happens with its `selection-` variants. For example, if you can't read clearly your polybar text, you should consider to invert polybar pattern and then re-apply the theme.
Check `gtheme pattern invert --help` to know how to invert patterns.

## Tips

If you're planning to create (or port existing dotfiles) patterns, we encourage you to check already existing patterns. You can found some on community desktops([gtheme-desktops](git@github.com:daavidrgz/gtheme-desktops.git))