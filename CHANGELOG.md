# Changelog

## 0.1.0 (2026-10-05, download updated 2026-10-08)

First public release. The app was formerly named AI Terminal; the first launch copies the old data folder to the new location.

### Added

- Terminal: a real zsh session (bash and fish are supported), tabs, split panes, session history, command blocks, a process panel, terminal search and clickable links.
- Agent: runs commands in the same session, reads, edits and creates files with undoable diffs, plan mode, streaming answers, per-project allow rules, four permission modes, secret masking, a network-block mode and audit-log export.
- Models: local models through Ollama, OpenAI-compatible servers, the OpenAI API and Codex CLI. API token usage and KV-cache savings for local models.
- SSH: the agent can work on a server (approvals name the server), a CPU / memory / GPU / disk strip and a status panel for the server, a session manager with `~/.ssh/config` import, jump hosts, X11 and port forwarding, and server and Mac file trees with drag-and-drop copy verified with SHA-256.
- A built-in editor for `~/.ssh/config` in the session panel: syntax check with the real `ssh -G`, line-numbered errors, backups of the previous content and a conflict check.
- Remote screen (VNC) inside the window: the picture travels only through the tab's SSH connection (no port is opened on your Mac, no extra login) and the VNC password is never stored. The AI chat does not see or operate the screen.
- An AI chat button in the top bar (Shift+Cmd+A): the AI pane and its input bar open and close together, so the terminal can use the whole window.
- Local network access: Settings, SSH, Local network access asks macOS to let the app reach servers on your home or office network. Connection attempts give up after 10 seconds, and when this Mac is on a different network than the server the app says so.
- vim integration (`:AitAI`, LSP diagnostics), bash and fish integration, Korean and English interface and accessibility work.
- Your Mac's CPU load in the top bar, a larger default window and a top bar that scales down instead of being cut off.

### Fixed

- The app no longer aborts when it is quit while a terminal is still closing.
- macOS now asks for local network access: the app's programs have identifiers of their own (the main program used to share one with other Electron apps, which could keep macOS from asking).

### Known limits

- Signed with a self-signed certificate, not notarized.
- No Intel build is available.
- SSH was exercised against a local test server, an Ubuntu VM and one NVIDIA DGX Spark (login and monitoring). Servers that only allow password login were not tested.
- The remote screen was exercised against a test VNC server and a TigerVNC server on an Ubuntu VM. Other VNC servers, slow connections, sound, file transfer and multi-monitor selection are not covered.
