
# panache (AUR)

AUR package for [panache](https://github.com/jolars/panache) - A Pomodoro timer
with daemon support for waybar.

## Installation

```bash
# Using an AUR helper (yay, paru, etc.)
yay -S panache

# Manual installation
git clone https://aur.archlinux.org/panache.git
cd panache
makepkg -si
```

## Updating

After each release of panache:

1. Update `pkgver` in PKGBUILD
2. Download the tarball and compute checksum:
   ```bash
   wget https://github.com/jolars/panache/archive/v2.8.0.tar.gz
   sha256sum v2.8.0.tar.gz
   ```
3. Update `sha256sums` in PKGBUILD
4. Test build: `makepkg -si`
5. Update `.SRCINFO`: `makepkg --printsrcinfo > .SRCINFO`
6. Commit and push to AUR

## Aupanacheion

This repo has a GitHub Action that can aupanacheically create PRs when new
releases are published. See `.github/workflows/update-pkgbuild.yml`.
