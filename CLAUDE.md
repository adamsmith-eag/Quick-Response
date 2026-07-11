# Claude instructions for this vault

This repository is the user's Obsidian vault and your long-term memory. Treat it as a
living knowledge base, not a codebase.

## At the start of every session

Read every file in `Memory/` before doing anything else. That folder is your accumulated
knowledge about the user — who they are, how they like things done, and what you've
learned in past sessions. Act on it without being asked.

## Capturing notes

When the user sends a note (a "note:", "capture", "jot down", or `/note` request):

1. Write it to `Inbox/<YYYY-MM-DD> <short-title>.md` using the frontmatter format in
   `Templates/Note.md`.
2. Keep the user's wording — clean up formatting, don't rewrite their meaning.
3. Add relevant `tags` and `[[wikilinks]]` to existing notes where they genuinely apply.
4. Commit and push immediately, one commit per note: `note: <short-title>`.

If the user asks to file or organize notes, move them from `Inbox/` into `Notes/`
(create subfolders as topics emerge — don't invent a deep hierarchy up front).

## Maintaining memory

When the user tells you something worth keeping ("remember that …", `/remember`, or
preferences/facts that clearly matter beyond this session):

1. Update the relevant file in `Memory/` — edit in place, keep each file current rather
   than append-only. `Memory/Learnings.md` is the catch-all for dated observations.
2. Commit and push: `memory: <what changed>`.

At the end of a substantial session, ask yourself whether you learned anything durable
about the user or this vault; if so, record it in `Memory/` before finishing.

Never store secrets, credentials, or anything the user marks as sensitive in this repo.
While the repo is public, also keep out personal contact details.

## Git conventions

- Work directly on the default branch for note and memory commits — no PRs for content.
- Pull before writing (`git pull origin main`) so you don't clobber notes synced from
  the user's Obsidian app.
- Never delete or rewrite the user's notes without being asked.
