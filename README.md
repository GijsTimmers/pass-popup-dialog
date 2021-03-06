[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

# pass-popup-dialog
A small script to have a `pass` dialog pop up, for fast copy-pasting of passwords.

## Dependencies
* `pass`
* `expect`
* `sxhkd`
* `bash`
* `bash-completion`
* any terminal emulator, I'm using `urxvt` here.

Optional:
* `notify-osd`

## Usage:
1. Set `sxhkd` binding: add this to your `sxhkdrc` file:

        ctrl + alt + p
            urxvt +sb -geometry 60x20 -e /path/to/pass_dialog && notify-send "Copied password to clipboard."

2. Make sure `sxhkd` is running and the set binding is not used by any other program.

## Notes
* You could change `bash` for `sh` but you will miss out on tab completion.
* Combining this with [`pam-gnupg`](https://github.com/cruegge/pam-gnupg) makes everything even faster. 
