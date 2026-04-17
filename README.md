# tmux-navigate

Intelligently navigate tmux panes and Vim splits using the same keys.
This also supports SSH tunnels where Vim is running on a remote host.

  | inside Vim? | is Zoomed? | Action taken by key binding |
  | ----------- | ---------- | --------------------------- |
  | No          | Yes        | Focus directional tmux pane |
  | No          | Yes        | Unzoom pane, focus directional tmux pane |
  | Yes         | No         | Seamlessly focus Vim / tmux |
  | Yes         | Yes        | Focus directional Vim split |


## Installation

1. Install the [TPM] framework for tmux.

[TPM]: https://github.com/tmux-plugins/tpm

2. Add this line to your `~/.tmux.conf`:
```sh
set -g @plugin '44maru/tmux-navigate'
```

3. Configure your navigation shortcuts:
```sh
# if you're using QWERTY layout
set -g @navigate-left  '-n M-h'
set -g @navigate-down  '-n M-j'
set -g @navigate-up    '-n M-k'
set -g @navigate-right '-n M-l'
set -g @navigate-back  '-n M-\'

# if you're using DVORAK layout
set -g @navigate-back  '-n M-d'
set -g @navigate-left  '-n M-h'
set -g @navigate-up    '-n M-t'
set -g @navigate-down  '-n M-n'
set -g @navigate-right '-n M-s'
```

4. Reload your tmux configuration file.

5. Type <kbd>prefix</kbd>+<kbd>I</kbd>.
   (This makes TPM install the plugin.)

### Vim integration

> Option 1: use your favorite Vim plugin manager
```vim
Plug '44maru/tmux-navigate'
```

> Option 2: symlink from your tmux plugins clone
```sh
mkdir -p ~/.vim/plugin/
ln -s ~/.tmux/plugins/tmux-navigate/plugin/tmux-navigate.vim ~/.vim/plugin/
```

## License

This project inherits the same license as the original project.

See the LICENSE file for details.

https://github.com/sunaku


