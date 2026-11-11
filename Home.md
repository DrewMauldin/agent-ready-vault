# Home

This vault is set up so AI agents (Claude Code, Codex, Cursor and similar) can help with your notes without wrecking them. The safety comes from one rules file, visible edits, and a log of every run.

## What lives where

| Folder or file | Purpose |
| --- | --- |
| Inbox/ | everything unsorted lands here |
| System/AGENT-RULES.md | the rules every agent must follow |
| System/skills/ | small instruction files your agent can run |
| System/templates/ | meeting, daily and project templates |
| agent-log/ | one entry per agent run, never deleted |
| CLAUDE.md, AGENTS.md | pointer files so agents find the rules automatically |

## Before your first agent run

1. Skim System/AGENT-RULES.md so you know what your agent has agreed to.
2. Make a backup (one git command or a folder copy; see the setup guide that came with your download).

## Your first run

Open a terminal in this folder, start your agent, and paste:

> Read System/AGENT-RULES.md in full. Then follow its "Start of every session" section, run the inbox triage skill from System/skills/inbox-triage.md, and write your run log.

Then check the agent's work with the checklist in your setup guide: a log entry exists, nothing was deleted, and every change sits inside an ai edit block.

## Everyday use

- End of day: "run the daily note tidy skill"
- After a meeting: capture raw notes in a new Inbox note, then "run the meeting note formatter skill on <note>"
- Weekly: "run the inbox triage skill"

See System/SKILLS-INDEX.md for the full list and how to add your own skills.
