---
name: note
description: Capture a quick note into the Obsidian vault's Inbox and push it so it syncs to the user's Obsidian app. Use when the user says "note:", "jot down", "capture this", or invokes /note.
---

# Capture a note

Take the note text from the arguments (or the user's message) and:

1. `git pull origin main` first, so you don't clobber notes synced from Obsidian.
2. Create `Inbox/<YYYY-MM-DD> <short-title>.md` — derive a 3–6 word title from the
   content. Use today's date; if a file with that name exists, append the time (`HHMM`).
3. Use this structure:

   ```markdown
   ---
   created: <YYYY-MM-DD>
   source: claude-code
   tags: [<1-3 relevant tags, or leave empty>]
   ---

   # <Short title>

   <the note, in the user's own words, lightly formatted>
   ```

4. Add `[[wikilinks]]` to existing vault notes only where clearly relevant.
5. Commit as `note: <short-title>` and `git push origin main`.
6. Confirm to the user with the filename — one line, no ceremony.
