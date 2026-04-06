# dotfiles

Personal repository for environment configuration files.

## Structure

Configurations are grouped by tool in separate directories.

## Installation

Clone the repository and enter the project directory:

```bash
git clone https://github.com/ZarenOFF/dotfiles.git
cd dotfiles
```

## Tmux

Config file: `tmux/.tmux.conf`

Create a symlink from inside the cloned repository:

```bash
ln -sfn "$(pwd)/tmux/.tmux.conf" ~/.tmux.conf
```

Reload the config in an existing `tmux` session:

```bash
tmux source-file ~/.tmux.conf
```
