<p align="center">
  <img src="https://raw.githubusercontent.com/crewmux/crewmux/main/assets/crewmux-hero.png" alt="CrewMux" width="720">
</p>

<h3 align="center">Coordinate AI agent teams in tmux</h3>

<p align="center">
  One project. One session. Multiple AI agents working together.
</p>

---

**CrewMux** turns a project directory into a tmux-based team session where Claude and Codex agents work side by side. Spawn workers, dispatch tasks, peek at output, and reconcile — from the terminal or a browser dashboard.

```
crewmux team start                           # boot a session in your project
crewmux task spawn -t claude "Write tests"   # spawn a Claude worker
crewmux task spawn -t codex "Fix auth bug"   # spawn a Codex worker
crewmux ctl status                           # see who's doing what
```

### Repositories

| Repo | Description |
|------|-------------|
| **[crewmux/crewmux](https://github.com/crewmux/crewmux)** | Project overview and brand assets |
| **[crewmux/cli](https://github.com/crewmux/cli)** | CLI + web dashboard (Rust) |
