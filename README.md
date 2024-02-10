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
Adjustments have been made to the blend-desktop track so that it applies to any DE.

## Example GNOME `/system.yaml` (vanilla)

```
repo: 'https://pkg-repo.blendos.co/'

impl: 'https://github.com/blend-os/tracks/raw/main'

track: 'gnome'
```

## Important inclusion to '/system.yaml' for this fork
Ensure your system yaml has this section;
```
package-repos:
    - name: 'chaotic-aur' # repo name as it would appear in pacman.conf
      repo-url: 'https://cdn-mirror.chaotic.cx/$repo/$arch' # Repo URL as it would appear in pacman.conf
```
Otherwise, the garuda meta packages won't be available
(Details about adding the chaotic AUR were pulled from the official v4 alpha guide)
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
