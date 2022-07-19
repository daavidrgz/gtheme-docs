# Pattern specification

## File structure

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

All properties are accessed with the pattern `<[some-property]>`. Those propertis will be replaced with the value of the applied theme OR the user\_settings file!!.

Mandatory property `output-file`!! That line will be removed in the generated file.

`theme-name` property is optional.

If the property is defined in the theme that you want to apply, you can reference it in the patterns. It means that you can create custom properties if you want (keep in mind that the rest of the themes should also need to have this custom property setted in order to work properly).

Optional propertyes. Syntax: `<[some-property|default-value]>` Talk about them.

## Modules and submodules

If you have a program that is composed of several config files, you also need several pattern files. To manage this situation, we got the pattern modules.

Inside the `patterns` folder, you can create another folder, which name will be the one of the module. Then, you can create any number of pattern files inside that folder, and all will be processed. Those files can have any name you want¿
