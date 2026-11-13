# The Agent-Ready Vault (Lite)

A starter Obsidian vault that puts your AI agent on a leash, then lets it work the night shift.

Most vault templates organise your notes. This one organises the agent. Inside is a rules file of twelve written rules your agent works under: read before editing, append instead of rewriting, never delete, mark every change, log every run, never send anything out of the vault, treat your recorded decisions as settled, and prove every claim that work is done. Two rules run the second half: when a decision is genuinely yours, the agent asks instead of guessing, by creating a short clarification task in Todoist; and when the agent runs unattended, it stays inside its brief, one queued job at a time, with a STOP file that halts everything.

The result is a second brain that can run itself on a schedule. You queue a job in the evening. Overnight the agent does the filing and the first pass, files your meeting transcripts, extracts the actions into Todoist, and writes a plain-language log of what it changed. What it sends you is not a report to wade through; it is the few decisions that were actually yours, waiting as tasks with the question, the context and the options. You answer, and the answer is recorded as settled, so you are never asked twice.

This repository is the free lite version. It is a genuine working subset, not a screenshot of one.

## What lite includes

- System/AGENT-RULES.md: the full twelve rules, unchanged from the paid version
- Sample Prompts.md: three of the sixteen prompts (daily note tidy-up, raising a clarification task instead of guessing, and making the agent prove a finished job)
- System/templates/decisions.md: the decisions log template, the record that makes "settled means settled" and the clarification loop work

## What the full version adds

The full vault, at https://mauldins.gumroad.com/l/llaegg, adds the structure around the rules:

- The complete starter vault: Home note, Inbox with a fictional sample meeting note to practise on, an agent-log format with a completed sample run
- All sixteen prompts, including running the queue unattended, processing answered clarifications, and turning a meeting transcript into a filed note with actions and clarifications
- The three workflow files: the autonomous run pattern (queue, brief template, approval gates, STOP file), the clarification loop in full with a worked example, and the transcript workflow
- Three starter skills (daily note tidy, meeting note formatter, inbox triage) plus an index that shows how to write your own
- A verification checklist for checking an agent's run log against the files, worked examples of good and bad runs, and meeting, daily and project templates alongside the decisions log
- A setup guide that walks from opening the vault to scheduling overnight runs, and a licence covering all your own machines, with updates included

## Using lite

1. Copy System/AGENT-RULES.md into your own vault, or open this folder as a vault in Obsidian to look around first.
2. Start your agent (Claude Code, Codex CLI, Cursor) inside the folder and tell it to read System/AGENT-RULES.md before it touches anything.
3. Try the daily tidy prompt from Sample Prompts.md on a copy of a real note, and check its work: your words untouched, its additions inside `%% ai edit %%` blocks, a run log entry written.

## Licence

See LICENCE.md in this repository. Short version: personal use on your own machines, no redistribution.
