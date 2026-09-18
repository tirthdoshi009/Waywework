# Fail Fast, Learn Fast

Work often continues longest around the assumption nobody has tested. The
implementation grows, more people become involved, and the plan becomes harder
to change. When the assumption finally fails, the cost comes from everything
built around it rather than from the failure itself.

Fail fast means arranging the work so that the most important wrong assumption
is discovered early. Learn fast means allowing that discovery to change the
plan.

The goal is not to fail more often. It is to make uncertainty produce useful
evidence before commitment becomes expensive.

## Test What Could Stop the Work

Do not begin with the easiest or most familiar part merely because it produces
visible progress. Begin with the assumption most capable of making the rest of
the work unnecessary or incorrect.

Ask:

- what must be true for this approach to work;
- which of those claims has not been demonstrated;
- what would be most expensive to discover late; and
- what is the smallest test that could prove the assumption wrong.

The right first step is often an experiment, a narrow integration, a difficult
conversation, or a decision from an owner. It may produce less visible output
than implementation, but it reduces more risk.

## Make Failure Cheap

An early test should limit the cost of being wrong. Keep the scope small, avoid
irreversible changes, and decide in advance what result would cause the work to
stop or change direction.

Do not build a complete solution to answer a question that a small example can
answer. Do not involve every stakeholder when one owner can resolve the first
unknown. Do not migrate all the data to learn whether one representative record
can pass through the intended path.

Fast failure is responsible only when its impact is contained. Changes that
affect customers, security, privacy, or data integrity require safeguards,
review, and a rollback plan. "Fail fast" is not permission to move carelessly.

## Raise Concerns While Choices Remain

A concern raised early can change the design, sequence, scope, or date. The
same concern raised after implementation may leave only expensive choices.

State the concern when the evidence first supports it. Say what is known, what
could fail, how the risk can be tested, and when the result is needed. Do not
wait for certainty before making uncertainty visible.

Raising a concern is not predicting failure. It gives the team time to prevent
the failure or decide consciously to accept the risk.

## Define What the Test Will Teach

Activity is not automatically an experiment. Before testing an assumption,
write down:

- the question being answered;
- the result that supports the current direction;
- the result that challenges it; and
- the decision each result will cause.

Without those conditions, an ambiguous result can be interpreted as permission
to continue. The work then absorbs the cost of an experiment without receiving
its protection.

## Keep the Learning

A failure is valuable only if its lesson survives the moment.

Record what was assumed, what the evidence showed, and what changed because of
it. Update the design, plan, checklist, or operating guidance that allowed the
assumption to remain hidden. Share the result where the next person doing
similar work will find it.

Do not reduce the lesson to "communicate earlier" or "be more careful." Name
the missing signal, decision, owner, test, or boundary. A lesson that cannot
change future action is only a description of regret.

## Change Direction When the Evidence Changes

Learning fast is harder than failing fast. Teams can run an early test and
still continue with the original plan because time, identity, or prior
commitment is attached to it.

Treat changing direction as the purpose of the test, not as an admission that
the earlier work was wasted. The earlier work bought information. It becomes
waste only when the information is ignored.

After a failed assumption, choose explicitly whether to stop, reduce scope,
replace the approach, gather more evidence, or accept the risk. Do not continue
by default.

## Review Questions

- Which untested assumption could invalidate the most work?
- What would be most expensive to discover at the end?
- What is the smallest safe test that could prove us wrong?
- Have we decided what each possible result will cause us to do?
- Are concerns visible while the plan can still change?
- What changed because of the last thing we learned?
- Are we continuing because the evidence supports the plan, or because the
  plan already exists?

Related: [Communication](communication.md) covers separating evidence from
assumptions; [Deciding](deciding.md) covers turning concerns into decisions;
and [Raise Dependencies Early](raising-dependencies-early.md) applies this
principle to work that crosses team and service boundaries.
