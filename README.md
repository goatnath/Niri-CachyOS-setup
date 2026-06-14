# Niri + DankMaterialShell on CachyOS

My personal Wayland desktop setup using the Niri scrollable tiling compositor and DankMaterialShell on CachyOS.

## What's included

| Folder | Config |
|--------|--------|
| `niri/` | Window manager config + keybinds, animations, layout, rules, input, display, autostart |
| `dms/` | DankMaterialShell settings + amoledBlack and dankViolet themes |
| `alacritty/` | Terminal config + DMS colour theme |

## Requirements

Install dependencies:

```bash
sudo pacman -S niri stow alacritty dms-shell
```

## Installation

Clone the repo and symlink the configs:

```bash
git clone https://github.com/goatnath/Niri-CachyOS-setup.git ~/dotfiles
cd ~/dotfiles
stow niri dms alacritty
```

Start Niri.

## After first launch

**Wallpaper** — open DMS control centre → Wallpaper and set your own image. DMS manages the wallpaper from there.

**Monitor setup** — if your display isn't configured correctly, edit `~/.config/niri/cfg/display.kdl` and fill in your output name and resolution. Run `niri msg outputs` to get the correct output name.

## Keybinds

| Key | Action |
|-----|--------|
| `Mod+Return` | Open Alacritty |
| `Mod+Space` | Toggle DMS launcher |
| `Mod+Z` | Open Zen Browser |
| `Mod+Q` | Close window |
| `Mod+F` | Fullscreen |
| `Mod+T` | Toggle floating |
| `Mod+L` | Lock screen |
| `Mod+O` | Toggle overview |
| `Mod+Shift+R` | Screen recording (wf-recorder) |
| `Mod+Arrow keys` | Focus window |
| `Mod+Shift+Arrow keys` | Move window |
| `Print` | Screenshot |
| `Mod+Print` | Full screenshot |

## Additional Packages

You can install the packages configured recently in the keybinds using your package manager and AUR helper:

```bash
# Screen recording tools (pacman)
sudo pacman -S wf-recorder slurp

# Browser (AUR)
yay -S zen-browser-bin
```
