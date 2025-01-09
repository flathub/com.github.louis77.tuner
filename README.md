## Builds
[Build Bot](https://buildbot.flathub.org/#/apps/com.github.louis77.tuner)

## Assets
_org.freedesktop.Platform_ latest version is 24.08

## Use
```
flatpak run org.flatpak.Builder --force-clean --sandbox --user --install --install-deps-from=flathub --ccache --repo=repo builddir com.github.louis77.tuner.yml
flatpak run --command=flatpak-builder-lint org.flatpak.Builder manifest com.github.louis77.tuner.yml
flatpak run --command=flatpak-builder-lint org.flatpak.Builder repo repo
```