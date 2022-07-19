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

As we can see, we are executing the script using `bash`, but you can use any other language.

Another important thing resides the third line, where we are getting the VSCode theme name from the arguments passed to the script. That name is the one that is stored in the _extras_ section of each color theme.
