# Orbit Studio v0

A restrained cinematic theme tested on a TCL G13 running Google TV 14. The observatory wallpaper keeps its natural color and contrast; app-colored halos stay around the selected tile. The glass dock, compact controls, animated focus, and scrolling use existing launcher options.

![Real TV screenshot](screenshot.jpg)

## Assets

- [wallpaper.jpg](wallpaper.jpg): the native 1280 x 720 deployment image, about 155 KiB.
- [artwork-master.png](artwork-master.png): the original generated artwork at 1672 x 941, retained for future crops and exports. The theme tool does not upload this master.
- [screenshot.jpg](screenshot.jpg): a real 1280 x 720 TV capture, with personal details absent from the header.
- [config.json](config.json): the six-app dock, app-colored selection, animation, and layout settings.

The wallpaper was generated for this theme; no third-party artwork is included. It is distributed with the repository's MIT license.

## Use

```powershell
.\tools\theme.ps1 -TvHost '192.168.1.50' .\themes\orbit-studio
```

Replace the example address with your TV address. Undo the theme with `tools\theme.ps1 -TvHost <tv ip> -Reset`.

This version matches the tested TV's 720p panel. Full-color wallpaper decoding costs about 3.5 MiB at that size. It does not turn a 720p display into a 4K display. For weaker GPUs, set `reduced_motion` to `true`; `focus_overshoot`, `advanced_effects`, and the full-screen `ambient_glow` are already off.

Edit `dock_apps` to change the favorites or their order. Press Down for the remaining TV-app grid, including Proton VPN. The all-apps library is disabled on this firmware to avoid surfacing maintenance/demo activities.

See the complete tested baseline and restoration notes in [V0.md](../../V0.md).
