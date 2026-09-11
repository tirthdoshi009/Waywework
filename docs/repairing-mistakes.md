# Repairing Mistakes

A rules engine became slower than expected because assumptions about its
behaviour had not been investigated deeply enough. The useful response was not
to defend why those assumptions had seemed reasonable. It was to make the
mistake inspectable, repair its effects, and change how similar work would be
approached.

Making a mistake weakens trust less than refusing to make the mistake visible.

## State What Happened

Say what happened, what part I owned, and what effect it had. Do not hide the
acknowledgement inside an explanation of why the mistake was understandable.

An explanation may still be necessary, especially when the failure reveals a
systemic problem. Give it after ownership is clear. Otherwise, the explanation
sounds like a request to be excused before the affected person has been heard.

Use plain language:

> I made the wrong assumption about how this would scale. It caused the rule
> evaluation to become slower as the data grew. I should have measured that
> path before treating the design as complete.

## Repair What Can Be Repaired

An apology is incomplete when the consequences are left for someone else.
Correct the immediate problem, tell affected people what changed, and identify
anything that still cannot be undone.

Do not make the person affected by the mistake responsible for deciding whether
I should feel forgiven. The purpose of the acknowledgement is to restore the
work and the relationship, not to receive reassurance.

## Change the Process

Learning should produce an observable change: a new measurement, a smaller
experiment, an earlier review, or a question that will be asked next time.

"I learned from this" is not useful unless another person can tell what I will
do differently. Write the change down while the failure is still specific.
General lessons written later tend to describe the person I hope to be rather
than the action the evidence requires.

This does not mean adding a permanent rule after every failure. Ask whether the
change would have detected or reduced this particular mistake. Remove it later
if it stops earning its cost.

## Make Experimentation Safe Enough to Fail

Trying something new creates a real possibility of being wrong. Reduce the cost
of that possibility rather than pretending it can be removed.

Prefer a reversible decision, a limited audience, an explicit measurement, and
a named rollback when the work permits them. The deliberation should still
match the cost of being wrong, as described in [Deciding](deciding.md).

Failure is useful only when it produces evidence. Repeating an experiment
without changing the question, the method, or the decision is not learning.

## Review Questions

- Have I stated what happened without first defending it?
- What effect did the mistake have on other people or the system?
- What can still be repaired, and who is doing that work?
- What will I do differently that another person can observe?
- Would the proposed process change have reduced this specific failure?
- Is the next experiment small and reversible enough for what remains unknown?
