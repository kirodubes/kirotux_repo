# kirotux_repo

Signed pacman repository for the Kirotux Wayland editions, served through GitHub Pages.

Add it to `/etc/pacman.conf`:

```ini
[kirotux_repo]
SigLevel = Required DatabaseOptional
Server = https://kirodubes.github.io/$repo/$arch
```

Packages are signed with the Kiro signing key, which `kiro-keyring` makes trusted.
