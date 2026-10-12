# omarchy-nostromo-theme — project specifics

Omarchy dark theme: MU-TH-UR ship-terminal aesthetic, installs as `nostromo`.

## Layout

- `colors.toml` — source of truth: full canonical palette + `hyprland_active_border`
- `backgrounds/` — 3 original procedural 4K JPGs + `CREDITS.md` (no third-party assets, ever)
- `icons.theme` — single line (`Yaru-olive`)
- `preview.png` — 1800×1012 picker thumbnail
- `VERSION` — single version source, lockstep with git tag `vX.Y.Z`

## Commands

- `omarchy theme set nostromo` — apply (symlink or copy dir into `~/.config/omarchy/themes/nostromo` first for local test)
- `omarchy theme color --file colors.toml --all` — resolved palette incl. derivations
- `identify backgrounds/*.jpg` — confirm 3840×2160
- `git status --short`, `git diff`, `git log --oneline -5` — pre-commit review

## Verify loop (before every commit)

1. `git status --short`, `git diff`, `git log --oneline -5`
2. `colors.toml` parses (all keys `#RRGGBB`, `mode = "dark"` first); contrast re-check:
   fg/bg ≥ 7:1, dark_fg/bg ≥ 4.5:1, every ANSI ≥ 4.5:1
3. Backgrounds 3840×2160, each < 3 MB, top strip near-black
4. Never ship `.lua`, terminal configs, `vscode.json`, symlinks, or any
   reference/film/studio artwork — clean-room rule (see README)
5. Bump `VERSION` patch in same commit, tag `vX.Y.Z`, push branch + tag so local == remote
