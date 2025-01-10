## Builds
[Build Bot](https://buildbot.flathub.org/#/apps/com.github.louis77.tuner)

## Assets
_org.freedesktop.Platform_ latest version is 24.08

## Process
### Check Metadata
- _meson.build_ version number
- _data/com.github.louis77.tuner.appdata.xml.in_ release version number
### Check Build
Before checking in, test build and lint:
```
flatpak run org.flatpak.Builder --force-clean --sandbox --user --install --install-deps-from=flathub --ccache --repo=repo builddir com.github.louis77.tuner.yml
flatpak run --command=flatpak-builder-lint org.flatpak.Builder manifest com.github.louis77.tuner.yml
flatpak run --command=flatpak-builder-lint org.flatpak.Builder repo repo
```
