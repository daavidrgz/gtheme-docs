# PostScript specification

{% code title="vscode.sh" %}
```bash
#!/bin/bash

VSCODETHEME="$1"
VSCODE_SETTINGS_FILE="$HOME/.config/Code/User/settings.json"

[[ ! -e $VSCODE_SETTINGS_FILE || -z "$VSCODETHEME" ]] && exit 1

sed -i "s|\"workbench.colorTheme\": \".*\"|\"workbench.colorTheme\": \"$VSCODETHEME\"|" $VSCODE_SETTINGS_FILE
```
{% endcode %}

As we can see, we are executing the script using `bash`, but you can use any other scripting language.

Another important thing resides the third line, where we are getting the VSCode theme name from the arguments passed to the script. That name is the one that is stored in the _extras_ section of each color theme.

Postscripts argument are specific of each theme, since it is the only way to have themes synchronized with another parts of our system. VScode is a good example, but a similar thing happens to the wallpaper. 

This issue is handled via **extras**. For example, if you have a postcript that changes vscode theme according to a gtheme theme, you should have a `extras/vscode.sh` file, that executes every time you apply a desktop. That script can receive theme-specific arguments, and you can specify them on the **extras section** of theme files.

Extras are managed on a similar way to postscripts. They are executed every time you apply a theme, and you can also enable/disable them.