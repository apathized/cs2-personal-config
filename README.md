# cs2-personal-config

Kept losing my setup when tinkering with Linux; had Claude throw this together so I don't have to keep going back and fixing it.

Current Setup: CachyOS + Hyprland, AMD GPU (Mesa), G Pro 2 mouse @ 800 DPI. GPro Wireless Headset

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
| `-novid` | Skip intro video. |
| `-nojoy` | Disable controller support.|

## Video settings

| Setting | Value |
|---|---|
| Resolution | 1440x1080 |
| Aspect ratio | 4:3 |
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
| High Dynamic Range | Quality |
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
