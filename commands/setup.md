---
description: Set up your personal workspace for the Growth plugin. Reads .claude/folders.json if it exists, creates only the missing folders, and never overwrites a file.
---

# Setup

Prepare the folders the Growth agents write to. Be careful and report everything you did.

## Steps

1. **Read your folder names.** If `.claude/folders.json` exists in the current folder, read it. It maps the standard folders to the names you already use, for example `{"drafts": "Drafts", "workflows": "Analyses"}`. Use the mapped name everywhere below. If the file does not exist, use the standard names `drafts` and `workflows`, and do not create the file.
2. **Check what exists.** List which of the two folders are already there.
3. **Create only what is missing.** Make a missing folder. Never delete, move, rename or overwrite anything that already exists, including files inside those folders.
4. **Check for a `CLAUDE.md`.** If none exists, say so and offer to create a short one that names the two folders. Do not create it without a yes. If one exists, do not edit it.
5. **Report in a table:** folder | mapped name | already existed or created.
6. **Hand over.** Tell the person to say "I'm new, set me up" to start the onboarding coach.

## Rules

- Append or ask. Never silently overwrite.
- Do not read or copy anything outside the current folder.
- No em dashes.
