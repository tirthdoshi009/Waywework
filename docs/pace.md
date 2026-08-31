# Pace

Restraint governs the pause before a single action. Pace governs the shape of
work across days, weeks, and releases. The two are related but not the same: a
person can be admirably restrained in every individual exchange and still run a
quarter at a speed that guarantees a mistake.

Pace is mostly not a personal preference. Most systems worth working on already
encode a correct speed, and the useful skill is reading it rather than
overriding it.

## Read the Pace the System Already Encodes

A rollout ladder is the clearest example. Exposure moves through tenant
isolation, then internal users, then first release, then worldwide, with a bake
period between rings. The ladder is not bureaucratic delay. Each ring is the
smallest population that can surface a class of failure the previous ring could
not.

Skipping a ring does not deliver the change sooner. It moves the discovery of
the failure to a larger blast radius. The work of finding the problem still
happens; only the cost changes.

Before overriding a system's built-in pace, name what the pace is protecting
against. If that cannot be named, the pace is probably load-bearing and the
impatience is the thing to examine.

## Finish One Thing Before Starting the Next

Complete one substantial change end to end before beginning another. This is
stronger than keeping work in progress low, because it applies even when the
second task looks independent.

Two changes staged at once against the same system are rarely as independent as
they appear. Shared session state, shared approval queues, and shared review
attention all couple them. A partially staged second change can strand the
first, and the recovery costs more than the sequencing would have.

The cost of concurrency is not the second task. It is the state that must be
held open while both remain unfinished.

## Distinguish Finished from Finished-Looking

A change that has been applied is not necessarily a change that is live. An
edit can be staged, displayed as the new value, and still be waiting on an
approval that has not happened. Reading the result from the interface alone
reports a state that does not yet exist.

Before calling work done, identify the last step that a system outside your
control must take, and confirm it. Announcing completion early is not speed; it
transfers the remaining risk to whoever believed the announcement.

## Let Quality Buy the Pace

Working at a considered pace is not granted by policy. It is extended to people
whose output does not need re-checking.

This is worth stating plainly rather than pretending the latitude is universally
available. The order matters: being reliably right is what earns the room to
work deliberately, not the other way around. Someone whose work is regularly
returned will be managed more closely, and no principle about pace will survive
that.

The practical consequence is that quality is the investment that funds
everything else here.

## Review Questions

- What is this system's own pace, and if I am overriding it, what am I
  overriding it for?
- What state am I currently holding open, and what would it cost to close one
  item before opening another?
- Is this finished, or does it only look finished from where I am standing?
- Am I moving quickly because the outcome needs it, or because moving quickly
  resembles working?
- What would have to be true for the slower path to be the cheaper one?

Related: [Working with Restraint](working-with-restraint.md) covers the pause
before an individual action; [Work Boundaries](work-boundaries.md) covers
availability and recovery.
