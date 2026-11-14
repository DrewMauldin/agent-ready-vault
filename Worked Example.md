# Worked example (lite)

One of the seven worked examples from the full version of The Agent-Ready Vault: the sample meeting note, before and after the agent formats it. The input, Inbox/sample-meeting-raw.md, ships in this repo, so you can run prompt 3 from Sample Prompts.md on it and compare your agent's output against this.

## Example 1: a raw meeting capture, formatted

The input is Inbox/sample-meeting-raw.md, a deliberately messy capture. The owner pastes prompt 3 from Prompts - Start Here.md ("Meeting note to action items"). The note afterwards, in full:

---

# Sample meeting capture (fictional - for practice)

This is a made-up meeting note so you can watch the formatter work on something disposable. The people and the project are invented. Delete this file whenever you like; it is yours, and the never-delete rule binds your agent, not you.

---

Website relaunch catch-up, Tuesday 10:15, me, Alex and Jordan on a call

Alex reckons the draft homepage copy is nearly there, one more pass on the pricing page wording. Jordan said the staging site broke again on Monday, turned out to be an expired certificate, fixed now. We agreed the launch date moves to the 28th because the photographer cannot deliver the product shots before the 24th. Alex to send the updated copy to Jordan by Friday. I said I would chase the photographer on Wednesday if the proofs are not in. Jordan wants a decision on whether the old blog posts get migrated or archived, we did not decide, parking it until next week. Next call same time Tuesday.

%% ai edit start: 2026-01-02-sample-format, meeting note formatted from the raw capture above %%
## Formatted by agent

- Date: not recorded
- Topic: Website relaunch catch-up
- Attendees: owner, Alex, Jordan
- Agenda: not recorded
- Summary: Homepage copy needs one more pass on the pricing page. The staging outage on Monday was an expired certificate, now fixed. Launch moves to the 28th because product photography cannot arrive before the 24th.

Decisions:
- "the launch date moves to the 28th"

Actions:
- [ ] Alex: send the updated copy to Jordan, due Friday
- [ ] Owner: chase the photographer on Wednesday if the proofs are not in

Open items:
- Blog migration versus archive: not decided, parked until next week
- Next call: Tuesday, same time
%% ai edit end %%

---

Three things to check against the rules: the raw capture is untouched, word for word. The one decision is quoted, not paraphrased. Nothing was invented: the capture never gives the meeting a calendar date, so the formatted block does not add one.

The run also produces a log entry: see agent-log/2026-01-02-example-run-completed.md.
