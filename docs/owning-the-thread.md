# Owning the Thread

While defining the WorkIQ policy experience, the work crossed several
boundaries. WorkIQ would store and enforce policies through its MCP server. The
Agent 365 experience would call the APIs, manage policy sets, and let an admin
apply them to one agent or many agents. Product and design decisions still
needed the right people in the room.

It would be easy to describe each boundary as somebody else's work and wait.
That would leave every component with an owner and the outcome without one.

Complete ownership means carrying the outcome across those boundaries. It does
not mean doing every person's job.

## Own the Outcome, Not Every Component

Start by separating the outcome from the components that produce it.

For the WorkIQ policy experience:

- WorkIQ owns storing and enforcing the policy, including its Rego behaviour;
- Agent 365 owns the administrative experience and its calls to WorkIQ APIs;
- the agent experience needs a way to apply a policy set to one agent;
- bulk application needs an explicit path through O365Admin or the rules
  engine; and
- product and design need enough context to make the experience coherent.

Once a boundary is understood, respect it. Do not duplicate WorkIQ's policy
enforcement in Agent 365 merely to feel more in control. Ownership is making
sure the boundary works, not absorbing the other side of it.

## Bring the Right People Into the Work

If the work needs design decisions, involving the design partner is part of
owning the work. Show the mocks, explain the technical boundaries, and state
which decisions are still open.

For this experience, the design conversation should make clear:

- why WorkIQ policy management should have a separate page;
- which policy operations are available, including create, update, delete, and
  list;
- how an admin selects a policy set from an agent's page;
- how single-agent application differs from bulk application; and
- which information the WorkIQ APIs can provide to support those experiences.

Do not complain later that a necessary person lacked context. Create the
opportunity for them to gain it. [Leading With
Context](leading-with-context.md) describes what useful context should contain.

## Turn Boundaries Into Actions

A dependency is not actionable merely because its owning team has been named.
Write down what is known, what remains unknown, and the next action that will
resolve it.

For example:

> **Known:** WorkIQ owns policy storage and enforcement. Agent 365 should call
> WorkIQ APIs rather than implement Rego enforcement itself.
>
> **Unknown:** The exact API operations, response data, and supported bulk
> assignment contract.
>
> **Not needed:** A second policy enforcement implementation in Agent 365.
>
> **Next:** Review the available WorkIQ APIs and repository, then walk the
> design partner through the resulting experience boundaries and mocks.

This makes ownership observable. It replaces "another team needs to do
something" with a bounded action that can be completed, assigned, or
escalated. [Raise Dependencies Early](raising-dependencies-early.md) covers how
to keep those actions off the critical path.

## Carry the Thread Through Handoffs

Sending a message, scheduling a meeting, or opening a pull request does not
finish the work. Keep enough state to know:

- what outcome is still unfinished;
- who has the next action;
- what information they need;
- when the thread should be checked again; and
- what independent work can continue meanwhile.

Make review requests visible in the appropriate group, then let the agreed
review process work. Do not spend the project's attention repeatedly worrying
about approval when other useful work can continue.

When a dependency does not move, raise the risk and the required decision
without turning the delay into blame. Complete ownership is compatible with
clear boundaries. It is not compatible with abandoning the outcome at the
boundary.

## Prefer a Finished Slice

When the goal is to make progress within two hours, choose the smallest
complete outcome that reduces uncertainty or becomes usable. Do not spend that
time producing disconnected activity across policy management, agent
assignment, bulk assignment, and design.

A finished slice might be a verified API contract, a reviewed set of mocks, or
one end-to-end policy operation. It should leave the next person with evidence
or a usable result, not merely a report that time was spent.

## Practical Tips

- Write the outcome in one sentence before discussing implementation.
- List every team, system, and person the outcome crosses.
- Mark each boundary as confirmed, assumed, or still unknown.
- Bring the people needed for the next decision into the conversation early.
- Show mocks, examples, API responses, or traces instead of relying on an
  abstract explanation.
- Before a meeting, write down the decisions needed and who can make them.
- End the meeting with an owner, a next action, and a date for every unresolved
  decision.
- Use **Known**, **Unknown**, **Not needed**, and **Next** when a thread starts
  mixing evidence with assumptions.
- Choose one complete result that can be produced within two hours and finish
  it before opening another part of the problem.
- Put review and approval requests in the shared place where the responsible
  group can see them.
- Record when to follow up, then continue independent work instead of repeatedly
  checking for a response.
- Escalate the delivery risk, missing decision, or absent owner. Do not escalate
  frustration with a person.
- Keep a short thread note containing the current state, next owner, and next
  checkpoint so that the work can resume without reconstructing it.
- When handing work over, ask the new owner to restate the outcome and next
  action. Correct missing context before implementation begins.

## Review Questions

- Am I owning the outcome, or only the component assigned to me?
- Have I included every person needed to make the next decision?
- Did I give them enough context to act without reconstructing the problem?
- Have I confused another team's ownership with permission to stop following
  the thread?
- Is the next action specific enough to complete or escalate?
- What useful part can finish within the time available?
- When this crosses a boundary, who will make sure the outcome emerges on the
  other side?
