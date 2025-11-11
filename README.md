# Hyprland + Waybar

A minimal, dark-themed configuration for Hyprland and Waybar.

![Screenshot](docs/screenshots/desktop.png)

## Structure
```
~/.config/
├─ hypr/
│  ├─ hyprland.conf
│  ├─ hyprlock.conf
│  └─ hyprpaper.conf
└─ waybar/
   ├─ config
   └─ style.css
```

## Requirements
- hyprland, waybar, hyprpaper, hyprlock
- Nerd Font (recommended)
- Optional (if used by your Waybar modules): pamixer or pactl, brightnessctl, playerctl, wl-clipboard, grim, slurp, nmcli (NetworkManager), upower

Example (Arch):
```sh
sudo pacman -S hyprland waybar hyprpaper hyprlock ttf-nerd-fonts-symbols wl-clipboard grim slurp brightnessctl playerctl
```

## Setup
Copy:
```sh
SOURCE="/path/to/repo/.config"
rsync -av "$SOURCE/hypr" "$SOURCE/waybar" ~/.config/
```
Or symlink:
```sh
ln -sfn "$SOURCE/hypr" ~/.config/hypr
ln -sfn "$SOURCE/waybar" ~/.config/waybar
```

## Run
```sh
hyprctl reload
waybar &
hyprpaper &
```

Autostart (in hypr/hyprland.conf):
```ini
exec-once = hyprpaper
exec-once = waybar
```

## Usage / Keybinds
- See and edit keybinds in: hypr/hyprland.conf
- Adjust Waybar modules/styles in: waybar/config and waybar/style.css

## Git
```sh
git add hypr/ waybar/ README.md && git commit -m "Add Hyprland + Waybar configs and README"
```
