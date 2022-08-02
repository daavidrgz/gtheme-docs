# PostScript specification

[Dunst extra example](https://github.com/daavidrgz/gtheme-desktops/blob/main/simple/gtheme/post-scripts/dunst.sh):

```bash
#!/bin/bash

pkill dunst &>/dev/null
exit 0
```

PostScripts are scripts that are executed after a pattern is filled. Some applications don't support hot-reload, so them must have to be reloaded. PostScripts allow to automatize those reloads every time a theme is applied, so the user doesn't have to restart it manually.

| **WARNING:** The names of the script files should match the pattern names. |
| --- |

They recive as first parameter the **`output-file` path specified in the pattern**, but
not all applications need this path in order to restart correctly.

There is a **special script** called `desktop-exit.sh` that is executed every time you change from one desktop to another one. It let us be agnostic of the current Window Manager that is being used and feel a better experience when switching from one desktop to another.