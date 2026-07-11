---
name: remember
description: Store a durable fact, preference, or lesson in Claude's long-term memory (the Memory/ folder) so future sessions know it. Use when the user says "remember that...", "from now on...", or invokes /remember.
---

# Remember something

Take what the user wants remembered and persist it to `Memory/`:

1. `git pull origin main` first.
2. Pick the right file:
   - Facts about who the user is → `Memory/About Me.md`
   - How they like things done → `Memory/Preferences.md`
   - Anything else durable → `Memory/Learnings.md` (dated entry, newest first)
3. Edit in place — update or replace stale entries rather than appending duplicates.
   Bump the `updated:` frontmatter date.
4. Never store secrets or credentials; while this repo is public, keep out personal
   contact details too. If the item is sensitive, say so instead of storing it.
5. Commit as `memory: <what changed>` and `git push origin main`.
6. Confirm in one line what was remembered and where.
