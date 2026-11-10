# The day-one test

The question these files exist to answer: **can a new agent be useful on its first day without you explaining anything?**

Run this before you trust the scaffold. It takes about an hour and it will fail the first time.

## The test

1. Start a fresh session with **only** `rules/identity.md`, `rules/working-agreement.md`, and `rules/task-context.md` available. No chat history, no memory, no verbal preamble.
2. Give it a **real task** you actually need done — not a toy. Something with a decision in it.
3. Watch for the two failure signals:
   - **You explain something.** Any sentence you type that starts "oh, and also…" is a missing line. Note it, do not type it — if you type it, you have invalidated the test.
   - **You fix something.** Any edit that is about voice, altitude, or format rather than content is a rule that was not written down.
4. Score it:

| Result | What it means |
| --- | --- |
| Useful, and you edited nothing | The three files are sufficient for this class of task. |
| Useful, and you edited prose only | Voice section is thin. Add the specific rule you applied when editing. |
| Plausible but wrong altitude | Intent is missing — the brief template is being skipped. |
| Wrong decision, well executed | Agreement 3 is not being followed, or the task was not reversible and should have been escalated. |
| Asked three questions and stalled | Escalation rule is either absent or too strict. Add "make the low-stakes call, name the assumption." |
| Confidently wrong, no warning | Refusal list or the "never invent" line is missing. This is the worst outcome; fix it first. |

5. **Put every note in the files, not in the conversation.** Then run the test again with a different task.

## Passing

You are done when a fresh session produces work you would have shipped, on a task it had not seen, and the only thing you added afterwards was content the files could not have known.

That is a low bar and most setups do not clear it, because most setups encode their rules in a conversation that disappears.

## After day one

- **Re-run the test monthly** with a genuinely new task. Rules decay as the work changes.
- **Add one rule at a time**, with the reason attached. Rules added in batches never get evaluated.
- **Delete rules that stop mattering.** An unreferenced rule teaches the agent that the file is decoration.
- **Keep the refusals separate from the preferences.** Preferences can be negotiated in a session; refusals cannot.

## The failure this test is designed to catch

An agent that is impressive in a conversation you are having, and useless in a session you are not in.

Everything in this repo is an attempt to move knowledge out of the first and into the second.
