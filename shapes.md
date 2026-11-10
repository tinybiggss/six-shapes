# The six shapes

Six shapes, one rule: **a new problem gets an existing shape, or it waits.**

Not "or it gets a new shape." The waiting is the mechanism. If you write your idea down as one sentence and it does not fit any of the six, the next question is not "what is the seventh shape" but "is this actually work that needs a loop".

Each shape below has:

- **the invariant** — the property that makes it that shape, and the thing that breaks when you bend it;
- **what it refuses** — the failure mode it is most likely to slide into;
- **what it needs** — the inputs to fill in.

---

## 1. Brief

*Assemble scattered state into one decision-ready page.*

**Invariant — it ends in a decision, not a summary.**

A brief gathers from wherever state actually lives (calendar, mail, issues, notes), compresses it to one page with a skeleton that never changes, and delivers it before you would have gone looking. The skeleton matters more than the prose: a fixed structure means you can read it in ninety seconds and notice when something is missing.

It refuses to be a dashboard. A dashboard answers "what is the state of things"; a brief answers "what do you do next". If your page does not end in a recommendation, you have built the former.

**Needs:** the sources, a fixed page skeleton, a delivery time before the point where you would otherwise check manually, and a hard output rule (one page, one recommendation).

---

## 2. Watcher

*Poll a source, stay quiet until something changes.*

**Invariant — silence is the success signal.**

A watcher polls on a cadence, keeps a fingerprint of what it last saw, and speaks only on a change. It remembers what it already said, so the same fact does not arrive twice.

It refuses to report its own aliveness. A watcher that says "nothing changed" every hour has become a clock, and clocks train you to ignore them — which costs you the one message that mattered.

**Needs:** the source, a cadence slower than the rate at which the thing changes, a stored fingerprint, and a delivery rule that allows "nothing" to produce no message at all.

---

## 3. Sweep

*Walk a backlog on a timer and finish what went stale.*

**Invariant — the work is chosen by age, not by priority.**

A sweep enumerates a queue you already know about, finds everything past an age threshold, applies the smallest action that un-sticks each item, and reports a count rather than a story. Age is the scheduling signal because the queue is already ranked, badly, by whoever last touched it.

It refuses to start new work. A sweep may close, retry, escalate, or park — never begin. The moment it can begin, it becomes an inbox with a timer and the backlog moves rather than shrinks.

**Needs:** an enumerable queue, an age threshold, a small closed set of un-sticking actions, and a summary line.

---

## 4. Intake

*Turn an external event into a tracked object with an owner.*

**Invariant — every arrival gets one object, one class, one owner, or an explicit park bucket.**

Intake watches an arrival surface, classifies each event, dedupes it against everything already open, and creates a tracked object with a pre-diagnosis and a named owner. The pre-diagnosis is what makes it worth having: the person picking it up starts from a hypothesis rather than a log.

It refuses to act on what it filed. Filing and fixing are different loops. The moment intake also fixes, you lose the count — and the count of arrivals per class is the only early warning you get that something upstream is sick.

**Needs:** the arrival surface, a class list small enough to be exhaustive, a dedupe key, a routing table from class to owner, and a park bucket for the unclassifiable.

---

## 5. Gate

*Verify a claim before it is allowed to be true.*

**Invariant — the gate has to be able to say no, and it has to fail closed.**

A gate runs a fixed check set against a proposed change — tests, schema, forbidden patterns, a build, a diff review — and lets it through only on a pass. A refusal is a first-class outcome with a reason attached, not an exception to be worked around.

It refuses to warn. A gate that can only warn is a suggestion, and suggestions get clicked through. The value of a gate is that a red stops the line, which means the check set has to be small enough that you never learn to override it.

**Needs:** the claim being checked, an automatable check set, a blocking failure path, and a rule for what happens when the gate itself is broken (fail closed, always).

---

## 6. Ritual

*Scheduled hour that forces a decision you would defer.*

**Invariant — the output is a decision, and the loop is cheap to re-run by hand.**

A ritual holds a calendar-shaped slot with a fixed agenda, opens the context you would otherwise have had to assemble, asks the same questions every week, and writes the decision somewhere it will be read again.

It refuses to be optional. A ritual you are allowed to skip is a wish with a calendar entry. The cheap-to-re-run-by-hand property is what makes the schedule honest: you will miss the clock, and when you do, running it manually has to cost one command rather than an hour of context collection.

**Needs:** a slot, a fixed agenda, the context it opens by itself, and a place to write the decision.

---

## Telling them apart

When two shapes both fit, ask which one produces the right thing on a day when nothing is wrong — that is most days.

| Question | Shape |
| --- | --- |
| Does something have to be read? | Brief |
| Should most days produce nothing? | Watcher |
| Is it about age rather than priority? | Sweep |
| Did something arrive from outside? | Intake |
| Must something be allowed before it is true? | Gate |
| Is it a decision you keep deferring? | Ritual |

## The seventh shape

There is no seventh shape. There are two things that look like one:

- **a chain** — two existing shapes wired together, which is a composition and not a new shape;
- **a fix** — something you are doing by hand that should be a one-off, which is a script, not a loop.

If a genuine seventh appears, six shapes was the wrong claim and the count is not the point anyway. The point is that every added shape costs you the ability to hold the set in your head, and that ability is what lets you look at a proposed loop and say "that is a watcher with extra steps".
