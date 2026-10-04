# Changelog

## 2026.10.04

### What Changed
- New repository for the packages that stay installed on Kirotux systems (first: `kirotux-thunar`,
  `kiro-sddm-simplicity-hyprland`). Until now they only lived in a local folder used at ISO build time, so
  installed systems never received updates for them.

### Technical Details
- Same setup as `kiro_repo`: GitHub Pages, packages detach-signed with the Kiro key, unsigned database
  (`SigLevel = Required DatabaseOptional`). `repo.sh` and `up.sh` copied from `kiro_repo` with the database
  renamed to `kirotux_repo`; `repo.sh` exits cleanly when `x86_64/` has no packages yet. `setup.sh` unchanged
  (it picks the kirodubes identity from the `/KIRO…` path).

### Files Modified
- `repo.sh`, `up.sh`, `setup.sh`, `README.md`, `CHANGELOG.md`, `CLAUDE.md`, `LICENSE`, `.gitignore`, `.nojekyll`
