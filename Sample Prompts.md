# Sample prompts (lite)

Three of the sixteen prompts from the full version of The Agent-Ready Vault, so you can feel how they work before you commit. Replace anything in <angle brackets> before you send. Every prompt assumes your agent has read System/AGENT-RULES.md first; say so in your session if it has not.

## 2. Daily note tidy-up

Use when: end of day, to see what is still open in today's note.

```
Open today's daily note (YYYY-MM-DD.md) and read it in full. Append one ai edit block titled "Still open" that lists every unfinished task in the note, copied word for word. Under it, suggest at most three tasks for tomorrow, picked by deadline first, then size, and mark them as suggestions. Do not tick, move or rewrite any existing line. Write your run log.
```

## 14. Raise a clarification task instead of guessing

Use when: the agent reaches a decision that is yours, mid-job, and the clarification loop is on.

```
You have reached a question in <note or job> that is mine to decide: <the situation, in one line>. Do not guess. First check my decisions log for a recorded answer; if one exists, apply it and tell me which record you used. If none exists and the key is not already recorded as asked, create a clarification task in Todoist in the format System/CLARIFICATION-LOOP.md sets out: title "[Clarify] <the question> clr:<short-slug>", and a description with the context, the options if you know them, and the source note. Record the question and its key in the decisions log as asked. Then finish every part of the job that does not depend on the answer, and list the raised question at the end of your run log.
```

## 11. Verify before you claim done

Use when: an agent (including this one) says a job is finished and you want the claim checked, not trusted.

```
You told me the last job was done. Prove it. Re-read System/AGENT-RULES.md, then check the work against the files as they are now: list every file you changed with the ai edit block you added to each, show me the run log entry for the job, and confirm with evidence (file names and line content, not summaries) that nothing was deleted and nothing outside the vault was touched. If any part of the claim does not check out, say which part, plainly, at the top of your reply.
```
