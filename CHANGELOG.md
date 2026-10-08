# Changelog

## 2026.10.08

### What Changed
- Removed `kiro-sddm-simplicity-hyprland-26.07-1` (+ `.sig`) from `x86_64/`. The package is renamed to
  `kirotux-sddm-simplicity-hyprland`, and its next build lands here under the new name.

### Technical Details
- `repo.sh` rebuilds the database from the files present, so deleting the package file is enough to drop the old name.
  The new package `replaces` the old one, so installed systems switch over on `pacman -Syu`.

### Files Modified
- `x86_64/kiro-sddm-simplicity-hyprland-26.07-1-any.pkg.tar.zst` (+ `.sig`) removed

## 2026.10.04

### What Changed
- New repository for the packages that stay installed on Kirotux systems (first: `kirotux-thunar`,
  `kirotux-sddm-simplicity-hyprland`). Until now they only lived in a local folder used at ISO build time, so
  installed systems never received updates for them.

- First packages: `kirotux-thunar` 26.10-2 and `kirotux-sddm-simplicity-hyprland` 26.07-1, moved here with their
  existing Kiro-key signatures from the local `kirotux-repo` folder (and removed from its database).

### Technical Details
- Same setup as `kiro_repo`: GitHub Pages, packages detach-signed with the Kiro key, unsigned database
  (`SigLevel = Required DatabaseOptional`). `repo.sh` and `up.sh` copied from `kiro_repo` with the database
  renamed to `kirotux_repo`; `repo.sh` exits cleanly when `x86_64/` has no packages yet. `setup.sh` unchanged
  (it picks the kirodubes identity from the `/KIRO…` path).

### Files Modified
- `repo.sh`, `up.sh`, `setup.sh`, `README.md`, `CHANGELOG.md`, `CLAUDE.md`, `LICENSE`, `.gitignore`, `.nojekyll`
