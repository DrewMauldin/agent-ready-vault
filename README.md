# The Agent-Ready Vault (lite)

The free version of the Agent-Ready Vault: a folder skeleton and one rules file that let AI coding agents (Claude Code, Codex CLI, Cursor) help inside your Obsidian vault without mangling your notes.

## The method in four lines

1. Rules before work: the agent reads System/AGENT-RULES.md before touching anything.
2. Visible edits: every change is wrapped in %% ai edit %% comment blocks you can review in Obsidian.
3. Nothing deleted: append by default; obsolete content gets flagged, never removed.
4. Logged runs: the agent writes one log entry per session in agent-log/.

## Folder structure

```
your-vault/
├── Home.md
├── Inbox/
├── System/
│   └── AGENT-RULES.md
└── agent-log/
    └── 2026-01-01-example-run.md
```

## Using it

1. Copy these folders into your vault, or open this folder as a new vault in Obsidian.
2. Make a backup: `git init && git add -A && git commit -m "clean vault"`, or just copy the folder somewhere safe.
3. Start your agent in the vault folder and paste:

   > Read System/AGENT-RULES.md in full, then wait for my task.

The lite version has no CLAUDE.md or AGENTS.md pointer files, so include the rules path in your prompts, or add those two files yourself: one sentence pointing at System/AGENT-RULES.md is enough.

## What the full version adds

- CLAUDE.md and AGENTS.md pointer files, so agents find the rules on their own
- A skills system: an index plus three ready skills (daily note tidy, meeting note formatter, inbox triage) and a pattern for writing your own
- Three templates: meeting, daily, project
- A Home note wired to the whole system, an Inbox starter note, and the setup guide: a first agent run in under 15 minutes, with a rules checklist

Full version, A$29: [GUMROAD LINK]

## Licence

Free for personal use. Share it, fork it, adapt the rules to your own vault. Attribution appreciated, never required.
