# CrewMux GitHub Meta Repository

This repository manages the public-facing GitHub organization profile for **CrewMux**.

It exists to keep organization-level assets, profile content, and shared branding separate from the product codebase. The primary source code lives in the repositories listed below.

## Repositories

| Repository | Purpose |
| --- | --- |
| [crewmux/cli](https://github.com/crewmux/cli) | Main Rust codebase for the CrewMux CLI, tmux runtime, installer, and web dashboard |
| [crewmux/homebrew-tap](https://github.com/crewmux/homebrew-tap) | Homebrew tap for installing CrewMux |
| [crewmux/.github](https://github.com/crewmux/.github) | Organization profile, shared branding, and GitHub meta configuration |

## Contents

| Path | Description |
| --- | --- |
| [`profile/README.md`](./profile/README.md) | GitHub organization landing page shown at `github.com/crewmux` |
| [`assets/`](./assets/) | Shared brand assets for GitHub, documentation, and release materials |

## Maintenance

When updating this repository:

1. Keep repository references aligned with the current public repo layout.
2. Prefer concise, product-level language in `profile/README.md`.
3. Keep asset filenames stable so external references do not break.
4. Treat this repository as organization metadata, not product documentation.

## Brand Assets

The `assets/` directory contains the current CrewMux identity set:

- App icon
- Favicon
- Primary icon
- Hero banner
- Mascot
- Social preview card

For product usage, installation, and contribution guidance, use the main project repository: [crewmux/cli](https://github.com/crewmux/cli).
