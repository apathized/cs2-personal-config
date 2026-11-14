# cs2-personal-config

My Counter-Strike 2 setup: `autoexec.cfg` plus the settings that can't live in a cfg (launch options, video settings).

Setup: CachyOS + Hyprland, AMD GPU (Mesa), G Pro 2 mouse @ 800 DPI.

## Install

1. Clone into the CS2 cfg folder (or copy `autoexec.cfg` there):
   ```
   ~/.local/share/Steam/steamapps/common/Counter-Strike Global Offensive/game/csgo/cfg/
   ```
2. Set the launch options below.
3. Set the video settings below in game (Settings > Video). CS2 stores these in `cs2_video.txt`, not in cfgs.

## Launch options

Steam > CS2 > Properties > Launch Options:

```
ENABLE_LAYER_MESA_ANTI_LAG=1 %command% +exec autoexec -fullscreen -novid -nojoy
```

| Option | What it does |
|---|---|
| `ENABLE_LAYER_MESA_ANTI_LAG=1` | AMD + Mesa anti-lag Vulkan layer. Env var, so it has to go **before** `%command%` |
| `+exec autoexec` | Runs `autoexec.cfg` on launch |
| `-fullscreen` | Exclusive fullscreen, overrides the in-game borderless setting |
| `-novid` | Skip intro video (no-op in CS2, harmless) |
| `-nojoy` | Disable controller support (no-op in CS2, harmless) |

## Video settings

| Setting | Value |
|---|---|
| Resolution | 1440x1080 |
| Aspect ratio | 4:3 |
| Display mode | Fullscreen windowed (overridden to fullscreen by `-fullscreen`) |
| Refresh rate | Monitor max |
| Brightness (gamma) | 2.02 (set in autoexec) |
| Boost Player Contrast | Enabled |
| Wait for VSync | Disabled |
| Multisampling Anti-Aliasing | 8x MSAA |
| Global Shadow Quality | High |
| Dynamic Shadows | All |
| Model / Texture Detail | Low |
| Texture Filtering Mode | Bilinear |
| Shader Detail | Low |
| Particle Detail | Low |
| Ambient Occlusion | Disabled |
| High Dynamic Range | Performance |
| FidelityFX Super Resolution | Disabled |
| Low Latency (Reflex/Anti-Lag) | Enabled |

## Mouse

| Setting | Value |
|---|---|
| DPI | 800 |
| Sensitivity | 0.8 |
| eDPI | 640 |
| Zoom sensitivity ratio | 1 |
| Acceleration | Off (`accel_profile = flat` in Hyprland) |

Everything else (crosshair, viewmodel, HUD, radar, binds, audio, network, practice aliases) is in [`autoexec.cfg`](autoexec.cfg).
