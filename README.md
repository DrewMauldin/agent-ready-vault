# The Agent-Ready Vault

**Let an AI agent loose in your Obsidian vault without dreading what it did to your notes: twelve written rules, every edit marked, every run logged, and real decisions sent back to you as questions instead of guesses.**

This repository is the free lite version: the complete rules file, a working starter skeleton, and three sample prompts. The full package, with the workflows, all sixteen prompts and the complete setup guide, is on Gumroad:

**[Get The Agent-Ready Vault on Gumroad (A$29)](https://mauldins.gumroad.com/l/llaegg)**

## The problem

AI coding agents (Claude Code, Codex, Cursor) are genuinely useful inside a notes vault, and genuinely risky. Ask for something small and you can come back to a note rewritten in a different voice, a list tidied into a different order, or a section deleted because it looked redundant. Nothing records what changed, so checking the agent's work means re-reading your own notes. Most people respond the obvious way: they stop trusting the agent with anything that matters.

## The fix: change the agent's defaults

Not a plugin, and not a bigger prompt. One rules file the agent has to read before it touches anything, a small folder layout that gives it a place to work, and habits built for checking rather than trusting. The rules are instructions, and an agent can still get them wrong, so the system assumes it will: marked edits you can search, a log in a fixed format, and a backup as the rollback. This is convention, not enforcement. It sets defaults and leaves an audit trail.

## The twelve rules, in short

The full file, with the reasoning and the exact formats, is `System/AGENT-RULES.md` in this repo, complete and identical to the paid version.

1. **Read before you edit.** The whole note, and anything it links to, before changing a line.
2. **Append by default.** New material goes at the end or in a marked block, never woven into your existing paragraphs.
3. **Never delete.** Flag it or archive it; deletion is the one failure you cannot undo.
4. **Mark every edit.** Agent additions sit inside `%% ai edit %%` blocks, invisible in reading view, obvious in source view.
5. **Log every run.** What was asked, what changed, what was created, what was left alone and why.
6. **Keep filenames clean.** Letters, digits, spaces, hyphens, dates as YYYY-MM-DD up front.
7. **Stay in scope.** Inside the vault, on the task given, nothing else.
8. **Never send anything out.** The agent does not email, post or message from the vault.
9. **Settled decisions are final.** If a decision is recorded, the agent does not reopen it or ask about it again.
10. **Evidence before "done".** A step the agent cannot verify is written up as "unverified", not "done".
11. **Ask, do not guess.** When the answer is not recorded anywhere, the agent raises a question instead of inventing one.
12. **Autonomous runs stay inside their brief.** One job per run, inside a time box, approval gates for anything beyond the brief.

## Two loops that make it work

**The night-shift queue.** You fill a queue file in the evening, one job per line. A scheduled run takes one job only, does the filing, and writes a plain-language summary of what it changed. A file called STOP in the vault root halts every run until you remove it.

**The clarification loop.** Rule 11 needs a mechanism, because "ask me" does not work at 2am. When a run reaches a decision that is genuinely yours, the agent creates a task in your task app with the question, the context and the options it can see. You answer when you get to it. The agent applies the answer, records it in the decisions log as settled, and never asks you the same question twice.

The working detail for both loops, the queue format, the exact task format, the brief template, the approval gates, is in the full package. The rules above state the principles; the guides make them run.

## What is in this free repo

- `System/AGENT-RULES.md` — all twelve rules in full, unchanged from the paid version
- The starter skeleton: `Home.md`, `Inbox/`, and `agent-log/` with a sample run log in the required format
- `Sample Prompts.md` — three of the sixteen prompts, so you can feel how they work: the daily note tidy-up, raising a clarification instead of guessing, and making the agent prove a finished job
- `System/templates/decisions.md` — the decisions log template, the record that makes "settled means settled" work
- Short pointers in `System/AUTONOMOUS-RUNS.md` and `System/CLARIFICATION-LOOP.md` describing what the full guides cover
- `SETUP-GUIDE.md` — the short version; getting started is also covered below

## Getting started

1. Download or clone this repo, and open the folder as a vault in Obsidian (or copy `System/AGENT-RULES.md` into a vault you already have).
2. Make a backup copy of the folder. It is your rollback for everything that follows.
3. Start your agent inside the folder and tell it to read `System/AGENT-RULES.md` before it touches anything.
4. Try the daily tidy prompt from `Sample Prompts.md` on a copy of a real note. Check its work: your words untouched, its additions inside `%% ai edit %%` blocks, and a run log entry written.

If that first run behaves, you have the core of the system. Everything in the full package builds on it.

## What the full package adds

The paid version (A$29) is the complete working vault, not just the rules:

- `CLAUDE.md` and `AGENTS.md` pointer files, so Claude Code and Codex find the rules on startup
- `System/AUTONOMOUS-RUNS.md` in full: the scheduled-run pattern, queue format, approval gates, the STOP file, and a fill-in run brief template, plus a starter run queue with a worked example
- `System/CLARIFICATION-LOOP.md` in full: the exact task format, how you answer, how answers are applied and recorded as settled decisions, and a worked example from question to closed loop
- `System/TRANSCRIPTS.md`: the transcript workflow, from a folder of meeting exports to filed notes with the original kept word for word, actions as tasks, and ambiguities raised as clarifications
- All sixteen copy-paste prompts: daily notes, meeting actions, inbox triage, weekly review, decision capture, project sweep, contradiction checks, running the queue unattended, processing transcripts, and more
- Three starter skills (daily note tidy, meeting note formatter, inbox triage), each stating what the agent reads, what it may append, and when it must ask first, plus a pattern for writing your own
- `System/VERIFICATION-CHECKLIST.md`: the three-minute checks to run against a session before you trust its log
- Worked examples: a raw meeting capture before and after, a triage table, and what a bad run looks like
- Four templates: meeting, daily, project, and the decisions log
- A fictional sample meeting note to practise on, a blank run log format, and a completed sample run log
- The complete `SETUP-GUIDE.md`, ending with a chapter on going autonomous: scheduling runs, reviewing diffs, and switching on the clarification loop

**[Get the full package on Gumroad](https://mauldins.gumroad.com/l/llaegg)** — A$29, personal use on all your own machines, every future update included at no extra cost.

## Honest limits

The rules are plain instructions in files your agent reads, and current agents follow them well in most sessions. When one does not, the marked edits show you where, the run log shows you what it claims, and your backup undoes it. If you never intend to run an AI agent in your vault, none of this has a job to do. And if you want the agent to decide everything for you, this system is built to do the opposite: it hands decisions back, on purpose.

## Licence

See `LICENCE.md` in this repository. Short version: personal use on your own machines, no redistribution.
