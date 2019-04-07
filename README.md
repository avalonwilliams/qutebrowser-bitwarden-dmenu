# [THIS PROJECT HAS BEEN MIGRATED TO GITLAB](https://gitlab.com/AGitBoy/qutebrowser-bitwarden-dmenu)

# Qutebrowser Bitwarden Userscript
Autofills webpage login from your bitwarden account information, selected from a dmenu menu.
This branch has settings for users using rofi as a drop in replacement for dmenu

## Requirements
* [bitwarden-dmenu](https://github.com/andykais/bitwarden-dmenu)
* [bw](https://github.com/bitwarden/cli)
* dmenu
* qutebrowser (obviously)
* Standard UNIX utilities (sh, awk, sed, tr, etc...)
* xdotool

## Install
Make the userscripts directory if it doesn't exist:
```
mkdir -P ~/.local/share/qutebrowser/userscripts
```

Copy the userscript to the userscript directory
```
cp bw-dmenu-fill ~/.local/share/qutebrowser/userscripts
```

Add a keybinding, for example, in my `~/.config/qutebrowser/config.py`, I have the script bound to `zl`:
```
config.bind('zl', 'spawn --userscript bw-dmenu-fill')
```
