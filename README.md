# Quick Response — Obsidian ⇄ Claude Code Vault

This repository is an [Obsidian](https://obsidian.md) vault that doubles as a shared
workspace between you and Claude Code. Notes you capture in Obsidian sync here via git;
notes Claude captures for you land here and sync back into Obsidian. Claude also keeps
its long-term memory in this vault, so it gets more useful the more you use it.

## One-time setup (on your machine)

1. Clone this repo somewhere permanent:
   ```
   git clone https://github.com/adamsmith-eag/Quick-Response.git
   ```
2. In Obsidian: **Open folder as vault** → select the cloned `Quick-Response` folder.
3. Install the community plugin **Obsidian Git** (Settings → Community plugins → Browse → "Git").
4. In Obsidian Git settings, enable auto-pull and auto-commit/push (e.g. every 5–10 minutes).

That's it. From now on, anything Claude pushes appears in your Obsidian app within one
sync interval, and anything you write in Obsidian is visible to Claude in its next session.

> ⚠️ **Privacy:** this repository is currently **public**. If you're going to keep real
> notes here, make it private: GitHub → Settings → General → Danger Zone → Change visibility.

## How the vault is organized

| Folder | Purpose |
|---|---|
| `Inbox/` | Quick captures — notes you send via Claude Code land here for later filing |
| `Notes/` | Your organized, permanent notes |
| `Memory/` | Claude's long-term memory — context it maintains about you and your work |
| `Templates/` | Obsidian note templates |

## Using it from Claude Code

- **Send a note:** tell Claude "note: …" or use the `/note` skill. It writes the note to
  `Inbox/`, commits, and pushes.
- **Teach Claude something durable:** use the `/remember` skill (or just say "remember
  that …"). Claude updates `Memory/` so future sessions know it too.
- Claude reads `Memory/` at the start of every session in this repo (wired up via
  `CLAUDE.md`), which is how it evolves over time.
