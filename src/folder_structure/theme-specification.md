# Theme specification

Example using [Dracula](https://github.com/daavidrgz/gtheme-themes/blob/main/themes/Dracula.toml) theme.

```toml
name = 'Dracula'

[extras]
intellij-idea = ['Dracula Colorful']
vscode = ['Dracula']
wallpaper = ['~/.config/gtheme/wallpapers/Dracula/arch-linux-light.png']

[colors]
background = '1e1f28'
black = '000000'
black-hg = '545454'
blue = 'bd92f8'
blue-hg = 'bd92f8'
cursor = 'bbbbbb'
cyan = '8ae9fc'
cyan-hg = '8ae9fc'
foreground = 'f8f8f2'
green = '50fa7b'
green-hg = '50fa7b'
magenta = 'ff78c5'
magenta-hg = 'ff78c5'
red = 'ff5555'
red-hg = 'ff5454'
selection-background = '44475a'
selection-foreground = '1e1f28'
white = 'bbbbbb'
white-hg = 'ffffff'
yellow = 'f0fa8b'
yellow-hg = 'f0fa8b'
```

You can easily create a new theme skeleton running `gtheme theme new-skeleton <THEME_NAME>`

## Extras

In the extras section, there are specified all the arguments that are necessary to apply the theme in other applications.

The elements of the array will be passed to the extra's post-script in the same order. To see more information about this check out the [PostScript specification](file-specifications/postscript-specification.md).

You can also add any application you want, but obviously implementing a script that handles those arguments. This script must be stored into the `extras/` folder of a desktop.

| **WARNING:** The names of the extra's script and the application specified in the extras section of a theme must be the same! |
| --- |

## Colors

In the theme specification, you must use **valid hex colors only**. It is important no not prefix the hex color with `#`.

If the property is defined in the theme that you want to apply, you can reference it in the patterns. It means that you can create custom properties on theme's colors definition keep in mind that the rest of the themes should also need to have this custom property set in order to be consistent). We **encourage to not use custom color properties** on theme files, since we don't find this neccesary at all, and it will ruin the standarization we're trying to accomplish.

However, if you need to use more than 16 colors in your theme, creating new color properties
is the only way.

