# Extra specification

[VSCode extra example](https://github.com/daavidrgz/gtheme-desktops/blob/main/simple/gtheme/extras/vscode.sh):

```bash
#!/bin/bash

VSCODETHEME="$1"
VSCODE_SETTINGS_FILE="$HOME/.config/Code/User/settings.json"

[[ ! -e $VSCODE_SETTINGS_FILE || -z "$VSCODETHEME" ]] && exit 1

sed -i "s|\"workbench.colorTheme\": \".*\"|\"workbench.colorTheme\": \"$VSCODETHEME\"|" $VSCODE_SETTINGS_FILE
```

As we can see, we are executing the script using `bash`, but you can use any other scripting language.

Another important thing resides the third line, where we are getting the VSCode theme name from the arguments passed to the script. That name is the one that is stored in the _extras_ section of each color theme.

Extras argument are specific of each theme, since it is the only way to have themes synchronized with another parts of our system. VScode is a good example, but a similar thing happens to the wallpaper. 

This issue is handled via **extras**. For example, if you have a postcript that changes **vscode theme** according to a **gtheme theme**, you should have a `extras/vscode.sh` script, that executes every time you apply a theme. That script can receive **theme-specific arguments**, and you can specify them on the **extras section** of theme files and the name of the extra script **must match** the one that appers in that file.

Extras are managed on a similar way to postscripts. They are executed every time you apply a theme, and you can also enable/disable them.


| **INFO:** Dont forget to give extras execution permissions. |
| --- |