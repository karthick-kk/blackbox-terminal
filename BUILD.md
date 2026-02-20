# Build

## Flatpak (using GitHub Actions locally)

Requires [act](https://github.com/nektos/act) and Docker.

```bash
# Build the flatpak bundle
act workflow_dispatch -j flatpak --bind

# The bundle will be at ./blackbox.flatpak
```

## Install

```bash
# Install the GNOME runtime (one-time)
flatpak install flathub org.gnome.Platform//47

# Install the bundle
flatpak install --user blackbox.flatpak

# Or reinstall if already installed
flatpak install --user --reinstall blackbox.flatpak

# Run
flatpak run com.raggesilver.BlackBox
```
