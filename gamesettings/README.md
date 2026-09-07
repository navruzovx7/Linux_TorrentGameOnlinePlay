# CachyOS + Hyprland Gaming Setup

This file shows only the essentials. No unnecessary details.

## 1) Install basic packages

```bash
sudo pacman -Syu
sudo pacman -S steam gamemode mangohud gamescope protonup-qt wine winetricks vulkan-tools lib32-vulkan-tools xdg-desktop-portal-hyprland
```

If you use NVIDIA:

```bash
sudo pacman -S nvidia-dkms nvidia-utils lib32-nvidia-utils
```

## 2) Minimum Hyprland gaming config

Write this to `~/.config/hypr/hyprland.conf`:

```ini
monitor=,preferred,auto,1

env = SDL_VIDEODRIVER,wayland
env = MOZ_ENABLE_WAYLAND,1
env = MANGOHUD,1

decoration {
    blur {
        enabled = false
    }
}

animations {
    enabled = false
}

misc {
    vfr = true
    disable_hyprland_logo = true
}

bind = SUPER, Q, killactive
bind = SUPER, RETURN, exec, kitty
bind = SUPER, D, exec, wofi --show drun

windowrulev2 = noblur,class:^(steam_app_.*)$
windowrulev2 = noanim,class:^(steam_app_.*)$
```

That's enough. Turning off blur and animations makes games smoother.

## 3) Gamemode config

Write this to `~/.config/gamemode.ini`:

```ini
[general]
softrealtime = on
inhibit_screensaver = 1
allow_gpu = 1

[cpu]
governor = performance

[gpu]
apply_gpu_optimisations = 1
gpu = auto
```

## 4) Steam launch option

Steam > Game > Properties > Launch Options

Add:

```bash
gamemoderun %command%
```

To see FPS with MangoHud:

```bash
MANGOHUD=1 gamemoderun %command%
```

## 5) Proton / Steam requirement

In Steam:
- Settings > Compatibility
- Install Proton GE

This generally improves compatibility/stability.

## 6) Short summary

Top 3 things:
- install and use `gamemode`
- disable blur/animations in `hyprland.conf`
- add `gamemoderun %command%` to Steam launch options

These three are enough for most games.
