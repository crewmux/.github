<p align="center">
  <img src="https://raw.githubusercontent.com/crewmux/.github/main/assets/crewmux-hero.png" alt="CrewMux" width="720">
</p>

<h2 align="center">CrewMux</h2>

<p align="center">
  Coordinate Claude and Codex agents inside one tmux workspace.
</p>

<p align="center">
  CrewMux turns a project directory into an agent workspace with a master coordinator, focused workers, a browser dashboard, and terminal-native control in iTerm.
</p>

---

## What CrewMux Does

CrewMux is an open-source orchestration tool for running multiple coding agents in the same project without losing control of write scope, ownership, or session state.

It combines:

- A Rust CLI for session lifecycle and worker management
- A tmux-based runtime for master and worker panes
- A local web dashboard for dispatch, monitoring, and quick follow-ups
- Provider support for Claude Code and Codex CLI in the same session

## Core Workflow

```bash
crewmux team start
crewmux task spawn -t claude "Review the API surface"
crewmux task spawn -t codex "Implement the auth fix"
crewmux ctl status
```

Typical usage looks like this:

1. Start a session in the project directory.
2. Let the master coordinate decomposition and worker allocation.
3. Dispatch short instructions in the dashboard.
4. Open iTerm when direct terminal interaction is needed.

## Repositories

| Repository | Description |
| --- | --- |
| [crewmux/cli](https://github.com/crewmux/cli) | Main codebase, installer, documentation, and dashboard |
| [crewmux/homebrew-tap](https://github.com/crewmux/homebrew-tap) | Homebrew tap for installing CrewMux |
| [crewmux/.github](https://github.com/crewmux/.github) | Organization profile and shared GitHub assets |

## Installation

CrewMux is currently distributed through the CrewMux Homebrew tap:

```bash
brew tap crewmux/tap
brew install --HEAD crewmux/tap/crewmux
```

Alternative installation methods and platform notes are documented in [crewmux/cli](https://github.com/crewmux/cli).

## Design Principles

- One project directory maps to one coordinated session
- The master should minimize worker overlap and file ownership conflicts
- Terminal-native workflows remain first-class
- Session metadata stays local and inspectable

## Learn More

- Product source and docs: [crewmux/cli](https://github.com/crewmux/cli)
- Homebrew distribution: [crewmux/homebrew-tap](https://github.com/crewmux/homebrew-tap)

<p align="center">
  <img src="https://raw.githubusercontent.com/crewmux/.github/main/assets/crewmux-mascot.png" alt="CrewMux mascot" width="180">
</p>
