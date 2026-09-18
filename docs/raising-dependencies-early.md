# Raise Dependencies Early

The auto-consent permissions project looked like one feature, but its path ran
through several teams. The permissions first had to be stored in AgentX's
Cosmos store. After that, another part of the system had to match those
permissions against its rules before the feature could proceed.

Each dependency became visible only when the work reached it. When help from
another team did not arrive, the work waited and I kept asking. By then, the
dependency was already on the critical path, so every unanswered message felt
urgent.

The problem was not that the project depended on other teams. The problem was
that the dependencies became delivery concerns before they became shared
plans.

## Find the Boundaries Before Building

At the start of work, trace the outcome across team and service boundaries.
For every boundary, write down:

- what must be provided;
- which system and team own it;
- what is known about the contract;
- what remains unverified; and
- the smallest test that would prove the dependency works.

Do not wait until the main implementation reaches a dependency to contact its
owner. A dependency discovered early is a planning question. The same
dependency discovered at the end is an escalation.

This is not a demand for a complete design before starting. The purpose is to
find where progress depends on an assumption, an interface, or another team's
time.

## Turn Help Into a Concrete Request

"We need help" is difficult to schedule and easy to defer. State the specific
decision, artifact, or action needed.

A useful dependency request says:

- **Known:** what has already been confirmed;
- **Unknown:** what only the owning team can answer;
- **Next:** the smallest action that resolves the unknown;
- **Owner:** the person or team able to take that action; and
- **Date:** when the answer is needed to protect the plan.

For example:

> **Known:** Auto-consent permissions must be stored in the AgentX Cosmos
> store before rule matching can use them.
>
> **Unknown:** The schema and write path the matching flow expects.
>
> **Next:** Agree on one sample permission record and verify that the matching
> flow can read it.
>
> **Owner:** AgentX and the rule-matching owner.
>
> **Date:** Before implementation of the full write path begins.

This gives the other team something bounded to respond to. It also makes clear
whether the project is waiting for information, a decision, or implementation.

## Fail Fast Means Test the Dependency First

Fail fast does not mean moving carelessly or expecting the project to fail. It
means testing the assumptions most capable of stopping the work while they are
still cheap to change.

Build the smallest end-to-end proof across the uncertain boundary before
finishing the surrounding feature. Write one representative permission, read
it through the expected path, and apply one representative rule. If that path
does not work, the project has learned something useful before investing in
the complete implementation.

The result of an early failure should be retained: update the dependency map,
record the contract that was misunderstood, and change the plan. A failure
that produces no durable learning is only delay.

## Raise the Risk Before Raising the Urgency

When a dependency is not moving, raise the delivery risk early. Do not wait
until the deadline is close and then compensate with repeated messages.

State:

- what outcome is blocked;
- which dependency is unresolved;
- when it becomes critical;
- what attempts have already been made;
- who can resolve it; and
- what scope, sequence, or date changes if it remains unresolved.

Escalate the absence of an owner, answer, or commitment rather than frustration
with another team. The goal is to make the risk visible to people who can
change priorities, assign ownership, or change the plan.

Repeatedly pinging the same person is not an escalation path. If the request is
clear and still has no owner or date, raise it through the project's regular
status and decision channels.

## Learn Fast by Changing the Plan

Learning matters only when it changes what happens next. After a dependency
fails or takes longer than expected, decide whether to:

- reduce the first deliverable;
- sequence independent work ahead of the blocked work;
- replace an assumption with a tested contract;
- assign an explicit owner and checkpoint; or
- move the delivery date while the cost is still visible.

Do not preserve an obsolete plan merely because work has started. The point of
finding a problem early is to retain more choices.

## Review Questions

- Which parts of this outcome are owned outside my team?
- What assumption at a team or service boundary could stop the work?
- What is the smallest end-to-end test of that dependency?
- Is my request specific enough for another team to schedule?
- Does every critical dependency have an owner and a date?
- Have I raised the risk while the plan can still change?
- What did the last failed assumption cause us to do differently?

Related: [Communication](communication.md) covers how to state knowns and
unknowns; [Deciding](deciding.md) covers escalating when a needed decision
does not arrive; and [Fail Fast, Learn Fast](fail-fast-learn-fast.md) covers
testing uncertain assumptions while they are still cheap to change.
