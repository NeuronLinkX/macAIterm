# Changelog

## 0.1.0 (2026-10-05)

First public release. The app was formerly named AI Terminal; the first launch copies the old data folder to the new location.

### Added

- Terminal: a real zsh session (bash and fish are supported), tabs, split panes, session history, command blocks, a process panel, terminal search and clickable links.
- Agent: runs commands in the same session, reads, edits and creates files with undoable diffs, plan mode, streaming answers, per-project allow rules, four permission modes, secret masking, a network-block mode and audit-log export.
- Models: local models through Ollama, OpenAI-compatible servers, the OpenAI API and Codex CLI. API token usage and KV-cache savings for local models.
- SSH: the agent can work on a server (approvals name the server), a CPU / memory / GPU / disk strip and a status panel for the server, a session manager with `~/.ssh/config` import, jump hosts, X11 and port forwarding, and server and Mac file trees with drag-and-drop copy verified with SHA-256.
- vim integration (`:AitAI`, LSP diagnostics), bash and fish integration, Korean and English interface and accessibility work.
- Your Mac's CPU load in the top bar, a larger default window and a top bar that scales down instead of being cut off.

### Known limits

- Not signed or notarized.
- No Intel build is available.
- SSH was exercised against a local test server, an Ubuntu VM and one NVIDIA DGX Spark (login and monitoring). Servers that only allow password login were not tested.
