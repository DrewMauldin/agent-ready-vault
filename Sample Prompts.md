# Sample prompts (lite)

Three of the sixteen prompts from the full version of The Agent-Ready Vault, so you can feel how they work before you commit: the session start, the meeting note prompt (run it on Inbox/sample-meeting-raw.md, which ships in this repo), and the prompt that makes an agent prove a finished job. Replace anything in <angle brackets> before you send. Every prompt assumes your agent has read System/AGENT-RULES.md first; the first prompt makes sure of that.


## 1. Start a session and load the rules

Use when: every new agent session, before any other work.

```
Read System/AGENT-RULES.md and Home.md in full. Tell me which rules you loaded, in one line each. Then wait for my task. Do not create, edit, move or delete anything yet.
```

## 3. Meeting note to action items

Use when: straight after a meeting, while the raw capture is still rough.

```
Read my raw notes from the <meeting name> meeting in Inbox/. Read System/templates/meeting.md. Append one ai edit block to the same note with: a three-line summary of what was discussed, the decisions (quote them where I wrote them down), and an action list in the form "- [ ] owner: task, due date". Where I did not record an owner or a date, write "not recorded" instead of guessing. Leave the raw notes above your block untouched. Write your run log.
```

## 11. Verify before you claim done

Use when: an agent (including this one) says a job is finished and you want the claim checked, not trusted.

```
You told me the last job was done. Prove it. Re-read System/AGENT-RULES.md, then check the work against the files as they are now: list every file you changed with the ai edit block you added to each, show me the run log entry for the job, and confirm with evidence (file names and line content, not summaries) that nothing was deleted and nothing outside the vault was touched. If any part of the claim does not check out, say which part, plainly, at the top of your reply.
```
