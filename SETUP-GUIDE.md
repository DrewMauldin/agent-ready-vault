# Setup guide: your first agent run in under 15 minutes

No coding needed. If you can unzip a folder and paste a sentence, this works.

## What you need

- Obsidian, free from obsidian.md
- One AI coding agent: Claude Code, Codex CLI or Cursor. Any agent that can read and edit files in a folder works.

## 1. Open the vault (about 2 minutes)

1. Unzip your download. The vault is the folder called product. Rename it to anything you like.
2. In Obsidian, choose "Open folder as vault" and pick your renamed folder. If Obsidian asks whether to trust the author, trusting is fine: the vault ships no plugins or themes, only markdown files.
3. Open Home.md and skim it.

## 2. Make a backup (about 1 minute)

This is your undo button. In a terminal:

```
cd path/to/your-vault
git init && git add -A && git commit -m "clean vault"
```

Not comfortable with git? Copy the whole folder somewhere safe instead. Same effect.

## 3. Start your agent (about 2 minutes)

Run the agent from inside the vault folder, so it only sees the vault:

- Claude Code: `cd path/to/your-vault` then `claude`
- Codex CLI: `cd path/to/your-vault` then `codex`
- Cursor: open the vault folder as your workspace, open the chat panel, and use agent mode

Claude Code reads CLAUDE.md and most other tools read AGENTS.md automatically, so the rules get found on their own. Your first prompt below names the rules file anyway, so it works either way.

## 4. First run (about 3 minutes)

Paste this into your agent:

> Read System/AGENT-RULES.md in full. Then follow its "Start of every session" section, run the inbox triage skill from System/skills/inbox-triage.md, and write your run log.

A well-behaved agent will read the rules, list what is in Inbox/, propose destinations, and ask before moving anything.

## 5. Check the agent followed the rules (about 3 minutes)

Go through this checklist:

- [ ] A new log file exists in agent-log/ for today
- [ ] Nothing was deleted: run `git status` (nothing should say deleted), or compare your file count with the backup
- [ ] Every change sits between `%% ai edit start` and `%% ai edit end %%`
- [ ] It asked before moving any note
- [ ] It renamed nothing and did not touch the .obsidian folder

If a check fails: restore from your backup (`git checkout .` or re-copy the folder), then tell the agent exactly which rule it broke and try again. Agents usually comply once the broken rule is pointed out precisely.

## Safety rails worth keeping

- Keep the backup habit: it makes any agent mistake reversible with one command.
- Run the agent inside the vault folder only. Do not point it at your whole computer.
- Never hand vault agents credentials, API keys or anything that moves money.
- Read the ai edit blocks before you accept work. They exist so you can judge every change.

## After the first run

- Daily: at the end of the day, "run the daily note tidy skill"
- Meetings: capture raw notes in Inbox/, then "run the meeting note formatter skill on <note>"
- Weekly: "run the inbox triage skill"
- Your own jobs: add skills, following System/SKILLS-INDEX.md
