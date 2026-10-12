# NOSTROMO — Omarchy theme

A dark MU-TH-UR ship-terminal theme for [Omarchy](https://omarchy.org).
Your desktop, straight off a deep-space hauler's CRT wall — phosphor green
nominal, amber degraded, alarm-red lockdown — tuned so you can still ship
code on an 8-hour shift.

Installs as `nostromo`:

```bash
omarchy theme install https://github.com/sortofcoding/omarchy-nostromo-theme
omarchy theme set nostromo
```

Cycle wallpapers with `Super + Ctrl + Space`.

## Palette

| Role | Hex | Notes |
|---|---|---|
| `background` | `#060809` | Hull black, primary surface |
| `dark/darker_background` | `#040607` / `#020304` | Recessed wells |
| `lighter_background` | `#14191D` | Raised gunmetal panels |
| `foreground` | `#D6D2C4` | Aged-bone text (13.3:1 on bg) |
| `dark_foreground` | `#8A9499` | Brushed-steel secondary (6.5:1) |
| `accent` / `green` | `#33FF66` | Phosphor nominal (14.9:1) |
| `yellow` | `#FFB000` | Amber caution |
| `red` | `#FF4438` | Alarm, brightened a touch for legibility |
| `orange` | `#FF5C00` | Docking clamps |
| `cyan` | `#7DF9FF` | Hologram instruments |
| `blue` | `#4DA6FF` | Hypersleep glow |
| `magenta` | `#C792EA` | Signal violet — kept distinct from red/green in lightness, not hue alone |
| Focus border | phosphor → holo, 45° | `hyprland_active_border` gradient |

Every text-carrying pair clears WCAG AA (body ≥ 7:1, secondary ≥ 4.5:1,
all sixteen ANSI ≥ 4.5:1 against the background). Status colors keep
their semantics: green is never decoration, red never a brand moment.

File manager icons: `Yaru-olive` (colonial drab).

## Backgrounds

Six original 3840×2160 wallpapers in `backgrounds/`, cycled in filename
order: three survey vistas (red colony, green valley, starfield) and three
ship-terminal CRTs (system status, deck schematic, quarantine manifest).
All are procedural — layered gradients, line-art, terminal type, survey
grids, scanlines, film grain, vignette — generated with ImageMagick 7. No
photographs, no film stills, no AI generation. Each is under 700 KB and
keeps the top strip near-black so the bar stays readable. See
`backgrounds/CREDITS.md`.

## Clean-room note

This theme is an original work *inspired by* the on-screen terminal
aesthetic of late-70s/80s space-horror films (green-phosphor CRTs, dense
monospace telemetry, hazard striping). It ships no film stills, no studio
artwork, no corporate logos, and no reproduction of any third-party brand
identity. It was guided by the token system in the private
`weyland-yutani` design study (palette/typography/component language
described in our own words), not by its reference captures, which were
never copied, traced, or redistributed here. "Nostromo" names a fictional
towing vehicle; no affiliation with any studio is claimed.

## Layout

```
omarchy-nostromo-theme/
├── colors.toml        palette — the only required file; everything generates from this
├── backgrounds/       6 original 4K wallpapers + CREDITS.md
├── icons.theme        Yaru-olive
├── preview.png        theme-picker thumbnail
├── AGENTS.md          repo workflow
├── VERSION            single version source (lockstep with tag vX.Y.Z)
├── LICENSE            MIT
└── README.md
```

Deliberately ships no `.lua`, terminal configs, or `vscode.json`: Omarchy
drops those on install from a cloned repo anyway, so the theme is built to
look right from `colors.toml` alone.

## License

MIT — see `LICENSE`. Covers `colors.toml` and the original backgrounds alike.
