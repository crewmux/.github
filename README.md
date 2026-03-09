<p align="center">
  <img src="assets/crewmux-hero.png" alt="CrewMux" width="720">
</p>

<h3 align="center">Coordinate AI agent teams in tmux</h3>

<p align="center">
  One project. One session. Multiple AI agents working together.
</p>

---

**CrewMux** turns a project directory into a tmux-based team session where Claude and Codex agents work side by side. Spawn workers, dispatch tasks, peek at output, and reconcile — from the terminal or a browser dashboard.

## What it does

```
crewmux team start                           # boot a session in your project
crewmux task spawn -t claude "Write tests"   # spawn a Claude worker
crewmux task spawn -t codex "Fix auth bug"   # spawn a Codex worker
crewmux ctl status                           # see who's doing what
```

- **Project-scoped sessions** — each project directory maps to one team
- **Master + workers** — master coordinates, workers implement
- **Multi-provider** — Claude and Codex in the same session
- **Built-in orchestration** — conflict-avoidance rules out of the box
- **Web dashboard** — browser UI on `localhost:7700`
- **Single binary** — one Rust binary, no runtime dependencies beyond tmux

## Architecture

```
 crewmux team start
       |
  tmux session
  ┌─────────────────────────────────┐
  │  master (claude)  │  claude-1   │
  │                   │  codex-1    │
  │                   │  codex-2    │
  ├───────────────────┴─────────────┤
  │  log (tail -f)                  │
  └─────────────────────────────────┘
```

State lives in `~/.crewmux/` as JSON metadata and plain-text logs. No database, no daemon required.

## Install

```bash
git clone https://github.com/crewmux/crewmux.git
cd crewmux
./install.sh
```

Or build manually:

```bash
cargo build --release
cp target/release/crewmux ~/.local/bin/
```

## Repositories

| Repo | Description |
|------|-------------|
| [crewmux/crewmux](https://github.com/crewmux/crewmux) | This repo — project overview and brand assets |
| [crewmux/cli](https://github.com/crewmux/cli) | CLI + web dashboard (Rust) |

## Brand

### Palette

| Color | Hex | Usage |
|-------|-----|-------|
| Navy | `#0B1830` | Primary background |
| Deep Blue | `#112B57` | Surface / cards |
| Accent Blue | `#5AA5FF` | Links, highlights |
| Teal | `#37D3C6` | Secondary accent |
| Amber | `#FFB84D` | Warnings, status |
| Soft Sky | `#EAF3FF` | Light text / borders |

### Assets

All brand assets are in [`assets/`](assets/):

| Asset | SVG | PNG |
|-------|-----|-----|
| Icon | `crewmux-icon.svg` | `crewmux-icon.png` |
| App Icon | `crewmux-app-icon.svg` | `crewmux-app-icon.png` |
| Favicon | `crewmux-favicon.svg` | `crewmux-favicon.png` |
| Mascot | `crewmux-mascot.svg` | `crewmux-mascot.png` |
| Hero Banner | `crewmux-hero.svg` | `crewmux-hero.png` |
| Social Card | `crewmux-social-card.svg` | `crewmux-social-card.png` |

### Design Concept

- **Theme**: crew coordination + tmux pane multiplexing
- **Icon**: pane grid combined with a helm symbol
- **Mascot**: a captain character managing multiple work panels

## Contributing

See [CONTRIBUTING.md](https://github.com/crewmux/cli/blob/main/CONTRIBUTING.md) in the CLI repo.

## License

MIT
