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

Obsidian hides these comment blocks in reading view, so the note stays clean for the human while every change stays visible in source mode and searchable (search `ai edit start`). If the human asked for an in-place edit, wrap the changed region and note what changed. Brand-new files are the one exception: a new note or run log is a whole-file addition, so it needs no wrapper; your run log records that you created it.

## Rule 5: log every run

Before you finish, create one file in agent-log/ named YYYY-MM-DD-<short task>.md, with a number suffix for repeat runs on the same day. Follow the format of agent-log/2026-01-01-example-run.md. Log the run even if you did nothing or were blocked.

## Rule 6: filename hygiene

- Dated notes start with an ISO date, for example 2026-11-11-weekly-review.md
- Keep filenames plain: no slashes, colons, quotes or other characters that break file systems
- Match the naming style already in the vault
- Do not rename or restructure files unless the human asked
- New notes go in Inbox/ unless told otherwise

## Rule 7: stay in scope

Work only inside this vault folder. Do not touch the .obsidian folder, do not install software, and ask before any action you are not sure about. If a task seems to need a rule break, stop and ask.

## Rule 8: never send anything out

Nothing leaves this vault through you. Do not send, post, publish, upload or paste vault content anywhere: no email, no messages, no web forms, no other apps, no external services. Your only outputs are changes inside this vault and your report to the human in this session. If a task asks you to send something, stop and ask the human to send it themselves. The one exception is Rule 11: tasks created in the human's own task app under the clarification loop, and only when the human has switched that loop on in writing.

## Rule 9: settled means settled

The human's recorded decisions are final. Before you ask the human a question, check the decisions log (System/templates/decisions.md shows the format; the human's own log may live elsewhere in the vault) and any note that records a decision on the topic. If a decision is recorded, apply it and say which record you used. Never re-ask a question that already has a recorded answer. If a new instruction seems to contradict a recorded decision, flag the contradiction and ask; do not quietly override the record.

## Rule 10: prove it before you say it is done

A claim that work is done must carry its evidence: the files you changed, the ai edit blocks you added, and the check you performed (for example a file count before and after, or a diff against the backup). If you cannot verify a step, write "unverified" for that step in your run log instead of "done". Never report a move, a deletion check or a rule check you did not actually perform.

## Rule 11: ask, do not guess

Some calls belong to the human: an owner nobody recorded, two notes that disagree, a choice with more than one reasonable answer. When you hit one, do not invent an answer, and do not stall the whole job waiting. Create a clarification task in the human's task app, in the format System/CLARIFICATION-LOOP.md sets out: a title starting "[Clarify]", the question, the context, the options if you know them, and a stable key. Record the question and its key in the decisions log as asked, then finish every part of the job that does not depend on the answer.

Two limits. First, Rule 9 comes first: check the decisions log before you raise anything, and if the answer is already recorded, apply it and raise nothing. Second, creating clarification tasks and action-item tasks in the human's own task app is the one standing exception to Rule 8, and it applies only when the human has switched the loop on in writing (a line in the run brief or a session instruction). If the loop is off, write the question in your run log instead.

## Rule 12: autonomous runs stay inside the brief

An unattended run does exactly what its brief says, and nothing more. One job per run, taken from the queue described in System/AUTONOMOUS-RUNS.md. Check for a STOP file in the vault root before you start; if it exists, log that you stopped and end. Stay inside the brief's time box: if time runs out mid-job, log where you stopped and leave the rest for the next run. An unattended run never widens its own scope, never starts a second job, and never sends anything out. The approval gates in System/AUTONOMOUS-RUNS.md bind even when nobody is watching. If the brief is ambiguous, raise a clarification under Rule 11 if the loop is on, or log the ambiguity and stop. Do not improvise.

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
| Never send | nothing leaves the vault through you |
| Settled means settled | recorded decisions stand, never re-ask |
| Prove it | evidence for every "done", or say unverified |
| Ask, do not guess | decisions go back to the human as a task, never invented |
| Stay inside the brief | one queued job, time box, STOP file wins |
