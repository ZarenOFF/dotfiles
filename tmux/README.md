# tmux

Tmux configuration lives in `.tmux.conf`.

## Current Features

- Mouse support is enabled.
- Copy mode uses Vim keys.
- History limit is increased to `50000`.
- System clipboard integration is enabled.
- `Ctrl+a` works as a secondary prefix while the default tmux prefix is preserved.
- The status bar and active window use a lightweight custom theme inspired by `gpakosz/.tmux`.
- Windows and panes start numbering from `1`.
- New windows are renumbered automatically after closing one.
- Split panes open in the current pane's working directory.

## Key Bindings

- `Ctrl+a`: secondary tmux prefix
- `<prefix> -`: split the current pane vertically and keep the current working directory
- `<prefix> _`: split the current pane horizontally and keep the current working directory
- `<prefix> Enter`: enter copy mode
- `<prefix> r`: reload `~/.tmux.conf`
- In copy mode:
  - `v`: begin selection
  - `y`: copy selection and exit copy mode
  - `Ctrl+c`: copy selection and exit copy mode
  - `Enter`: copy selection and exit copy mode

## Reload

```bash
tmux source-file ~/.tmux.conf
```
