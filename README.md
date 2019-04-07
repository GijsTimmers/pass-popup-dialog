# pass-popup-dialog
A small script to have a pass dialog pop up, for fast copy-pasting of passwords

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
        urxvt m+sb -geometry 60x20 -e /path/to/pass_dialog && notify-send "Copied password to clipboard."

2. Make sure `sxhkd` is running and the set binding is not used by any other program.

## Notes
You could change `bash` for `sh` but you will miss out on tab completion.
