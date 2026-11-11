# Agent rules for this vault

Every AI agent session in this vault must follow this file. Read all of it before you create, edit, move or delete anything. If CLAUDE.md or AGENTS.md exists at the vault root, it points here. This file is the single source of truth, and it wins over your usual defaults.

## Rule 1: read before you edit

Read a note in full before you change it. Never edit from a filename guess or a partial preview. If a note is long and you only read part of it, say so in your run log.

## Rule 2: append by default

Add new content as a new dated section or a new ai edit block. Do not rewrite, rephrase, tidy or summarise the human's existing words unless they asked for exactly that. In-place edits are allowed only on explicit request.

## Rule 3: never delete

Never delete notes, sections, frontmatter, tasks or attachments. If something looks obsolete or duplicated, leave it where it is and raise it in your run log under follow-ups. Never empty a folder. Moving a note is allowed only when the human asked for the move or approved your proposal.

## Rule 4: mark every edit

Wrap every change you make in an ai edit block:

```
%% ai edit start: <run id>, <one line purpose> %%
your added or changed content
%% ai edit end %%
```

Obsidian hides these comment blocks in reading view, so the note stays clean for the human while every change stays visible in source mode and searchable (search `ai edit start`). If the human asked for an in-place edit, wrap the changed region and note what changed.

## Rule 5: log every run

Before you finish, create one file in agent-log/ named YYYY-MM-DD-<short task>.md, with a number suffix for repeat runs on the same day. Follow the format of agent-log/2026-01-01-example-run.md. Log the run even if you did nothing or were blocked.

## Rule 6: filename hygiene

- Dated notes start with an ISO date, for example 2026-11-11-weekly-review.md
- Keep filenames plain: no slashes, colons, quotes or other characters that break file systems
- Match the naming style already in the vault
- Do not rename or restructure files unless the human asked
- New notes go in Inbox/ unless told otherwise

## Rule 7: stay in scope

Work only inside this vault folder. Do not touch the .obsidian folder, do not install software, do not send vault content to external services, and ask before any action you are not sure about. If a task seems to need a rule break, stop and ask.

## Start of every session

1. Read this file.
2. Read Home.md.
3. Say which rules you loaded, then wait for the task or run the skill you were given.

## Quick reference

| Rule | In one line |
| --- | --- |
| Read before edit | full read, then change |
| Append by default | add, do not rewrite |
| Never delete | flag it, do not remove it |
| Mark every edit | wrap changes in ai edit blocks |
| Log every run | one entry per session in agent-log/ |
| Filename hygiene | ISO dates, plain names, no renames unless asked |
| Stay in scope | vault folder only, ask when unsure |
