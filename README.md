# blendOS Tracks

* GNOME: `gnome`
* Plasma: `plasma`
* Cinnamon: `cinnamon`
* LXQT: `lxqt`
* MATE: `mate`
* XFCE: `xfce`

# Fork intentions

This is just meant to be a simple fork which takes the base created by ico277, 
but with the additions of VirtManager and Virtualbox via Garuda's metapkgs for each.
Anything else should be installed in containers or via flatpak.
Primarily, this fork's changes will be stored in plasmavirt.yaml

## Example GNOME `/system.yaml` (vanilla)

```
repo: 'https://pkg-repo.blendos.co/'

impl: 'https://github.com/blend-os/tracks/raw/main'

track: 'gnome'
```

## Example GNOME `/system.yaml` with Caddy

```
repo: 'https://pkg-repo.blendos.co/'

impl: 'https://github.com/blend-os/tracks/raw/main'

track: 'gnome'

packages:
    - 'micro'
    - 'caddy'

services:
    - 'caddy'

package-repos:
    - name: 'chaotic-aur'
      repo-url: 'https://cdn-mirror.chaotic.cx/$repo/$arch'
```
