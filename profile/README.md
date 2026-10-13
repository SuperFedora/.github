<div align="center">

# SuperFedora 🛸

**Curated keyboard-driven workstation on clean Fedora.**  
*Not an OS, not a DE, not an init system — the collection of things set up how you want them.*

[Website](https://superfedora.github.io) • [Documentation](https://superfedora.github.io) • [Keybindings Reference](https://github.com/SuperFedora/superfedora/blob/main/docs/keybindings.md)

</div>

---

## Quick Install

Start from a Fedora Minimal netinstall (or any Fedora installation) and run:

```bash
curl -fsSL https://superfedora.github.io/install.sh | bash
```

SuperFedora checks what is present and installs only what is missing. It is fully idempotent and safe to re-run at any time.

---

## Repositories & Architecture

| Repository | Role |
|---|---|
| [**superfedora**](https://github.com/SuperFedora/superfedora) | **Core Workstation Monorepo**: CLI orchestrator (`bin/superfedora`), idempotent modules (`00`–`90`), package manifests, desktop dotfiles (`hypr/`, `quickshell/`, `kitty/`), and automated Btrfs rollback. |
| [**superfedora.github.io**](https://github.com/SuperFedora/superfedora.github.io) | **Web Portal & Installer CDN**: Documentation website, interactive keybindings guide, and edge-cached `install.sh` bootstrap endpoint. |
| [**artwork**](https://github.com/SuperFedora/artwork) | **Brand Media & Wallpapers**: Vector logos, 16-bit pixel avatars, screenshots, and curated 16-bit retro desktop wallpaper bundles. |
| [**.github**](https://github.com/SuperFedora/.github) | **Organization Profile**: Organization guidelines, profile overview, and global issue templates. |

---

## Core Commands

```bash
superfedora status             # Report what is present / missing (changes nothing)
superfedora update             # Fetch latest release and apply missing components
superfedora dotfiles           # Deploy desktop configs into home directory
superfedora dotfiles --check   # Check for drift between live config and repo
superfedora rollback           # Undo installation via pre-install Btrfs snapshot
```

---

## License

MIT © 2026 SuperFedora
