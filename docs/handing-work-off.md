# Handing Work Off

Most of this handbook is about how one person does their own work. This
document is about the point where that stops being the limiting factor.

A task that looks like one item on a board is usually several decisions
wearing a single title: how data is stored, how it moves, how things are
associated, what happens as the numbers grow, what the dependencies are, and
what failure looks like. One person can hold all of that. One person holding
all of it is also why the next six things wait.

## Owning Every Decision Makes You the Queue

The cost of keeping a task is not the hours it takes. It is that every
decision inside it now passes through one calendar.

This is easy to miss, because the symptom does not look like a bottleneck. It
looks like being busy, being asked a lot of questions, and being the person
who knows how the thing works. Those feel like contribution. They are also
what a queue looks like from the inside.

The test is not whether I am adding value on a task. It is whether anything is
waiting on me that would not be waiting on someone else.

## Hand Over the Problem, Not the Implementation

What transfers well is the problem, the constraints, and what the outcome has
to be. What transfers badly is the sequence of steps I would have taken.

Specifying the steps produces the result I already imagined. It also
guarantees that nobody else has looked at the problem, so the assumptions I
brought are the only assumptions the work is ever checked against. If my
design is wrong, someone implementing my steps finds out late; someone handed
the constraints may find out on the first day.

State the constraints that are real, meaning the ones that would make an
answer wrong rather than merely different. Leave the rest open. If I cannot
say why a constraint exists, it is preference, and preference does not belong
in a handoff.

The written form of a handoff is the Known / Unknown / Not needed / Next
structure in [Communication](communication.md). What is worth being specific
about is covered in [Four Stages of a Task](four-stages-of-a-task.md).

## Trust Is Not a Thing You Say

Saying I trust someone and then reviewing every decision they make is not
trust with extra care. Both statements cannot be true, and the person on the
other side resolves the contradiction correctly: they believe the behaviour,
not the sentence.

The practical version is narrower than it sounds. It does not mean no review.
It means deciding in advance what the review is for, such as correctness,
risk, or reversibility, and not reopening choices outside that. A decision I
would have made differently is not by itself a defect.

Withholding the decision also withholds the learning. Someone who is only ever
handed steps does not develop the judgment that would let them be handed the
problem next time.

## Say That You Were Wrong, Specifically

[Saying I Do Not Know](saying-i-dont-know.md) covers admitting the edge of
what I know. This is the other case: I did know, I was confident, and I was
wrong.

The useful form is short and contains no defence.

> I made a mistake. Here is what happened. Here is what I learned. Here is
> what I am changing.

What makes this worth doing is not the apology. It is that the last two
sentences are information the team did not previously have. An apology without
them is a request for reassurance, in the same way a hedged unknown is.

The alternative compounds the way overconfidence does. Someone who never
acknowledges an error cannot be used as a source, because their account of
what happened is not separable from their account of how they look.

## Failure Is the Price of the Boundary Moving

Work in an area nobody has worked in before will sometimes be wrong, and the
cause is usually assumptions that were never investigated rather than
decisions made carelessly. That cost is ordinary, and it is separable from
negligence.

A record of never failing is not evidence of judgment. It is usually evidence
of having stayed inside the part of the system already understood.

The question after a failure is therefore not whether it should have happened.
It is whether it was cheap, whether it surfaced early, and whether what was
learned was retained. Failures that are expensive, late, and repeated are a
different problem, and the discipline that prevents them is stating the
unknown while it is still cheap.

## Review Questions

- What is waiting on me that would not be waiting on someone else?
- Did I hand over the problem and the constraints, or my implementation of
  them?
- Which of the constraints I stated can I actually justify?
- Have I said I trust someone whose decisions I then keep reopening?
- Am I reviewing for correctness and risk, or for a different choice than
  mine?
- When I was last wrong, did I say what I changed, or only that I was sorry?
- If nothing I tried recently failed, what does that say about where I worked?

Related: [Security over competition](security-over-competition.md) covers the
status pressure that makes the apology hard; [Pace](pace.md) covers holding
open more work than can be finished.
