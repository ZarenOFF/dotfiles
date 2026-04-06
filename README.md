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

## Windows Terminal

Config file: `wt/settings.json`

On Windows, copy the file instead of creating a symlink.
This file keeps only portable settings such as key bindings, theme, and profile defaults.
System profiles like WSL and PowerShell are intentionally not hardcoded, so Windows Terminal can generate them per machine.

Stable Microsoft Store installation:

```powershell
Copy-Item .\wt\settings.json "$env:LOCALAPPDATA\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json" -Force
```

Unpackaged installation:

```powershell
Copy-Item .\wt\settings.json "$env:LOCALAPPDATA\Microsoft\Windows Terminal\settings.json" -Force
```

You can open the active Windows Terminal settings file from the app via `Settings` or by holding `Shift` while opening `Settings` to edit the JSON file directly.
