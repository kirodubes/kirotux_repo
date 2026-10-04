# CLAUDE.md — kirotux_repo

Public pacman repo for Kirotux packages that stay installed on user systems, served at
`https://kirodubes.github.io/kirotux_repo/x86_64` (GitHub `kirodubes/kirotux_repo`, Pages from `main`, `/`).

- Publish: put `*.pkg.tar.zst` in `x86_64/`, run `./up.sh` (runs `repo.sh`: sign with Kiro key 33B761B0EE5AD4FD,
  `repo-add`, then commits and pushes). Same flow as `~/KIRO/kiro_repo`.
- Build-time-only packages (`calamares-wayland`, `kiro-calamares-config-wayland`) do NOT belong here: they stay
  in the local `~/KIROTUX/kirotux-repo` folder, because the install removes them anyway.
- Installed systems get this repo through the ISO's `airootfs/etc/pacman.conf` `[kirotux_repo]` section.
