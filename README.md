<div align="center">

```
    _   __          ____  _____
   / | / /__  _  __/ __ \/ ___/
  /  |/ / _ \| |/_/ / / /\__ \
 / /|  /  __/>  </ /_/ /___/ /
/_/ |_/\___/_/|_|\____//____/
```

**A beginner-friendly distro built on advanced bases.**

Arch · Alpine · Gentoo · NixOS, with one installer and one toolset on top.

</div>

---

## What is NexOS?

NexOS makes powerful Linux bases approachable. Instead of another "easy" distro built on a beginner-oriented foundation, NexOS gives you a friendly install and a unified toolset on top of the advanced systems: **Arch**, **Alpine**, **Gentoo**, and **NixOS**. You pick the base, and NexOS handles the rest.

> **Status:** early development. Bases are being built one at a time: Arch first, then Alpine, Gentoo, and NixOS.

## Features

- **Choose your base.** Arch, Alpine, Gentoo, or NixOS, each with its own installer ISO.
- **Graphical installer.** Boots into Xorg with Openbox and launches [Calamares](https://calamares.io) directly, including user account setup.
- **Ready-to-use desktop.** Each ISO ships with a pre-configured, themed desktop baked in, so you get a working system right after install.
- **Pick your desktop and apps.** A netinstall step after the base install lets you choose your DE/WM and applications. It is also used for system updates.
- **Rice importer.** Choose a DE and apps and import a rice (theme setup) hosted on GitHub.
- **Unified package manager: `tpkg`.** One command set across every base.
- **Easy rollback: `i-wanna-go-back`.** Revert system changes using Btrfs and Snapper.
- **Lean ISOs.** Target size is under 3 GB, with no bloat.

## Supported desktops

XFCE, KDE, Hyprland, Sway, i3, LXDE, LXQt, and more. Each gets a custom NexOS rice.

## `tpkg`

A wrapper that gives you the same commands no matter which base you installed.

| Command | Description |
| --- | --- |
| `tpkg --install <pkg>` | Install a package |
| `tpkg --uninstall <pkg>` | Remove a package |
| `tpkg --repair` | Repair package state |
| `tpkg --update` | Update packages |
| `tpkg --sysupdate` | Update the whole system |

## Rollback

Made a mess? Run:

```
i-wanna-go-back
```

It uses Btrfs snapshots (via Snapper) to take you back to an earlier working state.

## How it works

1. **Boot** the ISO for your chosen base. Xorg starts with Openbox and launches Calamares.
2. **Install** the base system. Calamares unpacks a prebuilt squashfs for that base using rsync-based unpackfs.
3. **Netinstall** your desktop and apps after the base is in place.
4. **Update** later through the same netinstall and `tpkg` tooling.

## Releases

Release and build codenames follow the NATO phonetic alphabet: Alpha, Bravo, Charlie, and so on.

## Building

Build instructions for each base will be added as they land. The Arch ISO build uses `yay` to build AUR-only packages such as Calamares.

## Contributing

Issues and pull requests are welcome. Open an issue before starting on a big change so we can talk it through.

## License

TBD

---

<div align="center">
<sub>NexOS has a stable image and undergoing testing, be patient.</sub>
</div>
