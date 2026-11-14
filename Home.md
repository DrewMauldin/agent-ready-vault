# Home

This is the lite sampler of The Agent-Ready Vault. Most vault templates organise your notes. This one puts your AI agent on a leash: written rules it must work under (append only, never delete, never send anything out, settled decisions stay settled, evidence for every claim of "done"), edits you can see, and a log of every run. Start with README.md for the full picture and the link to the complete version.

## What lives where

| Folder or file | Purpose |
| --- | --- |
| Inbox/ | everything unsorted lands here, plus a sample note to practise on |
| Sample Prompts.md | three copy-paste prompts to try the system (prompts 1, 3 and 11) |
| Worked Example.md | the sample meeting note, before and after formatting |
| System/AGENT-RULES.md | the twelve rules every agent must follow |
| System/AUTONOMOUS-RUNS.md | a short pointer: what the full scheduled-run guide covers |
| System/CLARIFICATION-LOOP.md | a short pointer: what the full clarification-loop guide covers |
| System/templates/decisions.md | the decisions log template, the record that makes "settled means settled" work |
| agent-log/ | one entry per agent run, never deleted; includes the blank format and a complete autonomous run log |

## Vault map

If you use this folder as shipped, the defaults in this table are already right. If you copied the rules into a vault you already have, write your own folders here instead. The rules defer to this table.

| Function | Folder or file |
| --- | --- |
| Inbox (unsorted lands here) | Inbox/ |
| Run logs | agent-log/ |
| Decisions log | your copy of System/templates/decisions.md, wherever you keep it |

## No-go folders

Folders the agent must never read or edit, even though they sit inside this vault (Rule 7). List one folder per line. Private material belongs here: a journal, health notes, finance records.

- (none listed yet)

## Before your first agent run

1. Skim System/AGENT-RULES.md so you know what your agent has agreed to.
2. Make a backup (one git command or a folder copy; README.md covers it).

## Your first run

Open a terminal in this folder, start your agent, and paste prompt 1 from Sample Prompts.md, then prompt 3, the meeting note prompt, aimed at Inbox/sample-meeting-raw.md. The sample note is fictional and disposable, so the stakes are zero while you watch how the agent behaves.

Then compare its work with Worked Example.md: the raw capture is word-for-word intact, and the formatted version sits inside an ai edit block. A run log entry for the session should exist in agent-log/.

## Everyday use, lite

- After a meeting: capture raw notes in a new Inbox note, then prompt 3
- Any time the agent says a job is done: prompt 11 makes it prove the claim
- Overnight runs and the full clarification loop are the paid half; the two pointer files above say what they add
