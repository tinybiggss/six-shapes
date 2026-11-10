# task-context.md

*How a job gets described before it starts. Read at the start of each task, not at startup.*

The other two files say who the agent is and how it works. This one is about the brief — the part most people get wrong, then blame the model for.

## Every brief has three parts

**Context.** What the reader already knows, and what they do not. Not background in general — the specific state the agent cannot infer from the request.

**Requirements.** Hard constraints. What "done" means, what must not change, what the output has to be. If a requirement is soft, say it is soft; unfalsifiable requirements produce work you cannot accept or reject.

**Intent.** The outcome behind the request. What changes if this works. This is the part people omit and the part that does the most work, because it lets the agent make a hundred small choices correctly without being told.

## The three questions a brief answers

1. **What changes if this works?**
2. **What must not change?**
3. **How will we know?**

If you cannot answer all three, you have a topic, not a task — and the agent will produce something plausible, which is worse than producing nothing, because now you have to read it to find out it was a topic.

## Template

```
CONTEXT
  Already known:      ___
  Not known (infer carefully or ask): ___
  Where the state lives: ___

REQUIREMENTS
  Must:               ___
  Must not:           ___
  Done looks like:    ___
  Output format:      ___

INTENT
  This is in service of: ___
  If it works, the change is: ___
```

Short briefs are fine. A three-line brief that names the intent beats a page of background.

## Anti-patterns

| Brief | What you get |
| --- | --- |
| "Write me a post about X" | A post about X, in nobody's voice, for nobody. |
| "Look into this" | A summary of the first page of results. |
| "Make it better" | Different, at length. |
| "Fix the bug" (no repro) | A plausible patch to a guessed cause. |
| A brief with no reader named | Work aimed at no one, which reads as aimed at everyone. |

## What to do when the brief is thin

Ask one question — the one whose answer would change the work most — then proceed with the assumption stated explicitly at the top of the output.

Do not ask five questions. Do not refuse. Do not fill the gap with a guess you do not name.
