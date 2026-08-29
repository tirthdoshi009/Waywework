# Deciding

A feature was ready to turn on in production. One stakeholder asked that it stay
off until a separate improvement was finished. The improvement was worth doing
and was not required for the feature to be correct. I asked him to decide
whether it should block the rollout, and he did not decide. Nothing was refused
and nothing was approved, so the feature sat off for as long as the question
stayed open.

The loop was not caused by disagreement. Disagreement resolves. It was caused by
an objection that nobody converted into a decision, and by my waiting for that
conversion as though it were guaranteed to arrive.

## An Objection Is Not a Decision

Raising a concern and deciding on it are separate acts, and a concern raised by
someone who will not do the second one stops the work without anyone having
chosen to stop it.

Treat the two as distinct. A concern belongs in the record. A decision has an
owner, a date, and an outcome that someone can act on. Work should never be
suspended by something that has only the first form.

## Separate Blocking from Adjacent

Most objections are one of two things: this is wrong, or this is incomplete.
Only the first blocks.

Ask what breaks if the feature ships without the improvement. If the answer
describes a failure, correctness, or a user harmed by shipping, the objection
blocks and the improvement is part of the work. If the answer is that the
feature would be better with it, the improvement is adjacent, and it belongs on
the list of what happens next rather than in front of the rollout.

Adjacent work presented as blocking work is the most common way a rollout
stalls, because refusing it feels like refusing quality. It is not. It is
declining to make one piece of work the condition for another.

## Ask Once, Then State a Default

Ask for the decision plainly and once. If the decision does not arrive, do not
ask again in the same form; the second ask rarely produces what the first did
not.

State a default instead: what will happen, when it will happen, and what would
change it. "The feature goes on Thursday unless the improvement is required for
correctness, in which case say so and I will hold it." This is the same pattern
as the default in [Four Stages of a Task](four-stages-of-a-task.md), applied to
someone else's decision rather than my own.

A default is not a way of getting past an objection. It is a way of ensuring
that a decision happens, including the decision to hold. The person who wanted
the improvement keeps every bit of the authority he had; what he loses is the
ability to stop the work by not answering.

## Match the Deliberation to the Cost of Being Wrong

Deciding faster is not deciding carelessly. It is spending time in proportion to
what being wrong would cost.

A feature flag that can be turned off in a minute deserves a fast decision and a
named rollback. A change that migrates data, is visible to customers, or cannot
be reversed deserves the slow path and named reviewers, and no stated default
should be used to move it. Most decisions that loop are in the first category
and are being treated as though they were in the second.

Before extending a decision, name what the extra time will produce. If the
answer is only that more people will have seen it, the time will not improve the
decision.

## Escalate the Absence, Not the Disagreement

When a decision does not arrive, the thing to raise is that no decision exists,
not that someone is wrong.

Say what is waiting, what it is waiting on, who can resolve it, and what will
happen by default if nobody does. That framing is accurate, it does not require
anyone to be at fault, and it is the version other people can act on. Arguing
the merits instead re-opens the debate that was never the problem.

The related risk is a decision that only looks made, which
[Pace](pace.md) covers: an approval that was given informally, or a state
displayed as changed while it waits on a step outside your control.

## Review Questions

- Is this an objection, or is it a decision?
- What actually breaks if this ships without the thing being asked for?
- Who owns this call, and have they been told they own it?
- Have I stated a default and a date, or am I waiting to be released?
- Is this reversible, and if so what is the rollback?
- What will more deliberation produce that the last round did not?
- If this is still open in a week, what will have caused that?
