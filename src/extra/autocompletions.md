# Autocompletions

As a (kinda ugly) patch, in order to make the autocompletions update every time a desktop or a theme is added/removed, we are constantly regenerating them. This causes that we must have write access in the directory where we are saving those autocompletion scripts.

The steps that you have to follow depend on the shell you are currently using.

## Zsh

If you are using [zsh](https://www.zsh.org/), you need to add the following line to your `.zshrc`:

```
fpath=($HOME/.gtheme/completions $fpath)
```

Important: This line should be placed **BEFORE** the call to `compinit`, usually something like this:

```
autoload -Uz compinit && compinit
```

If you don't have this line, add it **AFTER** the fpath export.

## Bash

If you are using [bash](https://www.gnu.org/software/bash/), you only need to add this to your `.bashrc`:

```bash
[ -r /home/{your-user}/.gtheme/completions/gtheme.bash ] && source /home/{your-user}/.gtheme/completions/gtheme.bash
```

## Fish

If you are using [fish](https://github.com/fish-shell/fish-shell), it already includes an user level write access directory to store the completion scripts, so you don't need to do anything.
