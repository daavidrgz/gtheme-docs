# General usage

As well as we had seen in the previous section, you can interact with gtheme via two different approaches:

### **Command Line Interface (CLI)**

You can see gtheme's help with `gtheme --help` and `gtheme <subcommand> --help`

Here are some examples:

* `gtheme desktop list`: will show all desktops you've installed.
* `gtheme theme list`: will show all themes installed.
* `gtheme desktop set-default-theme <theme> -d <desktop>`: will set a default theme for the specified desktop.
* `gtheme desktop apply <desktop>`: will apply the specified desktop and copy desktop's dotfiles to your `~/.config` folder.
* `gtheme theme apply <theme>`: will apply the specified theme for the current desktop.

### **Text User Interface (T**UI)

* If you prefer a Text UI rather than a CLI, execute `gtheme` without any arguments.
* In order to see Text UI help and all included functionalities, press `h`.
* To navigate between _desktops/patterns_ view to _fav-themes/themes_ **** view, press `tab`.
