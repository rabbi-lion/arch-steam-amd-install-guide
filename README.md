# Arch Linux Steam Install Guide for AMD Systems

A simple guide for installing Steam on Arch Linux systems using AMD graphics.

## Enable multilib

Open the Pacman configuration:

```sh
sudo vim /etc/pacman.conf
```

Find:

```ini
#[multilib]
#Include = /etc/pacman.d/mirrorlist
```

Uncomment both lines:

```ini
[multilib]
Include = /etc/pacman.d/mirrorlist
```

Save the file and exit the editor.

## Install Steam

Update the system and install Steam:

```sh
sudo pacman -Syu steam
```

When prompted for the 32-bit Vulkan driver, select:

```text
lib32-vulkan-radeon
```

This provides the 32-bit Vulkan driver required for Steam on systems using the open-source AMD Radeon Vulkan driver.

The corresponding 64-bit `vulkan-radeon` package is installed as a dependency.

## Start Steam

Launch Steam:

```sh
steam
```

Allow Steam to complete its first-run update, then sign in.

## References

This guide was written independently using the official Arch Linux documentation and package information as technical references.

Relevant documentation:

- ArchWiki: Steam
- ArchWiki: Vulkan
- Arch Linux: `steam`
- Arch Linux: `vulkan-radeon`
- Arch Linux: `lib32-vulkan-radeon`

Arch Linux is a rolling-release distribution. Check the current Arch documentation before installation in case package names or procedures have changed.

## License

Made by rabbi-lion.

Original text in this repository is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License.

Referenced projects and documentation retain their respective licenses.

See `LICENSE` for the full license text.
