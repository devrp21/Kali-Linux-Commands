# 🔧 Tmux Commands Reference Guide

This document provides a comprehensive list of essential `tmux` commands and shortcuts, organized for ease of reference. Useful for managing multiple terminal sessions, panes, and windows efficiently.

---

## 📁 **Session Management**

| Command | Description |
|--------|-------------|
| `tmux` | Start a new tmux session. |
| `tmux new -s tryhackme -d` | Create a new **detached** session named `tryhackme`. |
| `tmux ls` or `tmux list-session` | List all active tmux sessions. |
| `tmux attach -t tryhackme` | Attach to the `tryhackme` session. |
| `tmux kill-session -t box-dev` | Kill the session named `box-dev`. |
| `tmux kill-session -t tryhackme -a` | Kill all sessions **except** `tryhackme`. |
| `tmux kill-server` | Kill the tmux server (all sessions). |

---

## 🚪 **Detach & Re-Attach**

| Keybind | Description |
|---------|-------------|
| `Ctrl + B`, then `D` | Detach from the current session. |
| `Ctrl + B`, then `S` | Show list of sessions and switch using arrow keys. |

---

## 🪟 **Window Management**

| Keybind / Command | Description |
|-------------------|-------------|
| `Ctrl + B`, then `C` | Create a new window. |
| `Ctrl + B`, then `,` | Rename the current window. |
| `Ctrl + B`, then `N` | Move to the next window. |
| `Ctrl + B`, then `P` | Move to the previous window. |
| `Ctrl + B`, then `0-9` | Jump to window by number. |
| `Ctrl + B`, then `W` | List and navigate all windows. |

---

## 🖼️ **Pane Management**

| Keybind / Command | Description |
|-------------------|-------------|
| `Ctrl + B`, then `%` | Split the window vertically. |
| `Ctrl + B`, then `"` | Split the window horizontally. |
| `Ctrl + B`, then `O` | Switch between panes. |
| `Ctrl + B`, then arrow keys | Navigate between panes. |
| `Ctrl + B`, then `;` | Return to the last active pane. |
| `Ctrl + B`, then `X` | Kill the current pane (Y/N to confirm). |
| `Ctrl + B`, then `!` | Break the pane into a new window. |
| `Ctrl + B`, then `Q` | Show pane numbers. |
| `Ctrl + B`, then `Space` | Cycle pane layouts. |

---

## 🔁 **Pane Swapping & Rotation**

| Command | Description |
|---------|-------------|
| `swap-pane -s 0 -t 1` | Swap pane 0 with pane 1. |
| `swap-pane -t 0 -s 1` | Swap pane 1 with 0 (reversed). |
| `Ctrl + B`, then `Shift + }` | Rotate panes clockwise. |
| `Ctrl + B`, then `Shift + {` | Rotate panes counterclockwise. |

---

## 🔗 **Join Panes Across Windows**

| Command | Description |
|---------|-------------|
| `join-pane -s t1` | Join from window `t1`. |
| `join-pane -t t2` | Join to window `t2`. |
| `join-pane -s 1 -t 2 -v` | Join vertically. |
| `join-pane -s 1 -t 2 -h` | Join horizontally. |

---

## 📋 **Copy Mode & Clipboard**

| Keybind / Command | Description |
|-------------------|-------------|
| `Ctrl + B`, then `[` | Enter copy mode. |
| `Ctrl + R` | Search **backward** in copy mode. |
| `Ctrl + S` | Search **forward** in copy mode. |
| `Ctrl + Space` | Start selection. |
| `Alt + W` | Copy selected text. |
| `Ctrl + B`, then `]` | Paste from buffer. |
| `Ctrl + B`, then `Shift + #` | Preview clipboard contents. |

---

## ⚙️ **Configuration & Customization**

| Command | Description |
|---------|-------------|
| `tmux show -g` | Show global configuration settings. |
| `set -g prefix C-a` | Change default prefix to `Ctrl + A`. |
| `set -g status-style bg='#44475a',fg='#8be9fd'` | Change status bar color. |
| `setw -g window-status-current-style fg=black,bg=white` | Highlight active window. |

📝 Add the configuration to `~/.tmux.conf` to make it persistent.

---

## 🏆 **Tips & Best Practices**

- Use `tmux` for multi-tasking in terminal environments.
- Customize your prefix key to avoid conflicts (`Ctrl + A`, `Alt + A`, etc.).
- Use `tmux list-keys` to view all shortcuts.
- Combine tmux with `.bashrc` or `.zshrc` for auto-starting sessions.

---

🎓 **Practice Tip**

You can use the [TryHackMe TmuxRemux Room](https://tryhackme.com/room/tmuxremux) to practice all these commands in a hands-on environment.

---

© 2025 Tmux Commands Guide. All Rights Reserved.
