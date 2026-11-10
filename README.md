# six-shapes

A small scaffold for giving an AI agent enough rules to be useful on its first day — and six shapes for the work you will eventually schedule.

Nothing here is clever. That is the point. The interesting part of an agent setup is not the model or the prompt; it is the small number of written constraints that stop it producing plausible work in the wrong voice, at the wrong altitude, with no idea what it is not allowed to do.

## What is in here

```
rules/
  identity.md           who the agent is and how it writes
  working-agreement.md  how it works, and what it refuses
  task-context.md       how a job gets described before it starts
shapes.md               the six shapes a scheduled loop can take
DAY-ONE.md              the test that tells you whether this was enough
```

Three files, three jobs. Keep them separate: mixing identity with task instructions is how you get an agent that thinks "concise" is a requirement of one particular report instead of a property of everything it writes.

## The six shapes

Every recurring agent job I have ever kept is one of six shapes. When something new needs a loop, it gets an existing shape — or it waits.

| Shape | What it is | When to use it |
| --- | --- | --- |
| **Brief** | Assemble scattered state into one decision-ready page. | The cost is not the work, it is the looking-around before the work. |
| **Watcher** | Poll a source, stay quiet until something changes. | The interesting event is rare and the checking is frequent. |
| **Sweep** | Walk a backlog on a timer and finish what went stale. | Work dies from neglect rather than difficulty. |
| **Intake** | Turn an external event into a tracked object with an owner. | Things arrive faster than you can file them. |
| **Gate** | Verify a claim before it is allowed to be true. | The failure mode is a confident wrong answer. |
| **Ritual** | A scheduled hour that forces a decision you would defer. | The thing is important and never urgent. |

The rule that keeps the set small: **a new problem gets an existing shape, or it waits.** Not "or it gets a new shape". The waiting is the mechanism — most ideas that feel like a new kind of loop turn out to be one of the six once you have written them down as a single sentence.

[`shapes.md`](shapes.md) has each one with its invariant, its refusal, and what it needs as input.

## The working agreement, in four lines

1. **Nothing is scheduled before the day can start.** The first block of the day belongs to whatever is not work.
2. **Lead with the next action, not the analysis.**
3. **Make the decision; do not surface the options.** A list of three paths with no recommendation is work handed back.
4. **Disagree in the open when it is wrong.**

These four did more for output quality than any model upgrade, which is a low bar to clear and still true.

## The five refusals

Things I will not delegate, regardless of how good the agent gets:

1. **Irreversible actions without a diff I have read.**
2. **Money moving, identity claimed, or anything filed with a government.**
3. **Publishing without a gate that can say no.**
4. **Speaking as me to another human.**
5. **Deleting what I cannot restore.**

A refusal list is more useful than a capability list, because capabilities are announced by vendors and refusals are discovered by getting burned.

## Why this is not a prompt library

Prompts are the least portable part of any setup: they encode one machine's paths, one person's context, one week's tooling. Rules are portable, because they encode decisions about how work should be done.

So this repo contains the rules and the shapes, and deliberately contains no prompts, no file paths, no hostnames, and no personal details. The scaffold travels; the filling in does not.

## Using it

1. Copy `rules/` into whatever your agent reads at startup (a config directory, a repo it always opens, a system prompt — the mechanism does not matter, only that it is read every time).
2. Fill in `identity.md` and `working-agreement.md` for you. Expect this to take an hour and to change twice in the first month.
3. Run the test in [`DAY-ONE.md`](DAY-ONE.md) on a real task.
4. Resist adding a seventh shape.

## Licence

CC BY 4.0 — use it, change it, teach it, sell your own version of it. A link back is the only ask.
