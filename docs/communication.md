# Communication

Good communication transfers enough context for someone to act without making
them absorb avoidable urgency or interruption.

## Prefer Asynchronous Communication

Use written, asynchronous communication for updates, questions, proposals, and
decisions that do not require an immediate exchange. This gives people time to
think and preserves the result for others.

A useful message makes the following clear:

- the context;
- the request or decision needed;
- who needs to act;
- when a response is genuinely needed; and
- what happens if no response arrives.

## Write to Clarify the Work

Writing is not only a way to communicate thinking after it is complete. The act
of writing can reveal what the work actually is.

Before starting a technical discussion or proposing a solution, write a short
account of what you observed. Name what the evidence supports, where your
understanding ends, and what the evidence does not require you to change. This
often exposes assumptions, narrows the problem, and prevents an open question
from quietly becoming additional scope.

A written message is useful even when its first reader is the author. Sending
it to the team then gives others something concrete to correct, extend, or act
on. The goal is not to make every thought public; it is to make consequential
technical reasoning clear enough to inspect.

## Separate What Is Known From What Is Not

When a technical situation is still being understood, write down the boundary
of current knowledge before proposing work. Separate the message into:

- **Known:** facts supported by observation or evidence;
- **Unknown:** questions that still need investigation;
- **Not needed:** work that current evidence does not justify; and
- **Next:** the smallest action that would resolve an important unknown.

Writing these separately prevents assumptions from quietly becoming facts. It
also makes scope visible: the team can act on what is known without treating
every uncertainty as a requirement.

For example:

> **Known:** Requests fail only when the optional header is absent.
>
> **Unknown:** Whether the gateway or the service rejects the request.
>
> **Not needed:** A redesign of the authentication flow.
>
> **Next:** Capture one gateway trace for a failing request and compare it with
> a successful request.

Use this structure when it adds clarity, not as a mandatory template for every
message. A short message can make the same distinctions in ordinary prose.

## Response Expectations

Sending a message does not create an obligation to respond immediately. People
may batch messages, mute notifications, and reply within their working hours.

Do not use repeated messages, extra mentions, or a channel switch to manufacture
urgency. If something is urgent, say why, state the real deadline, and use the
team's agreed escalation path.

Silence should not be treated as agreement for consequential decisions. Name
the reviewers and the decision date instead.

## Choosing a Channel

- Use shared channels for information the team may need later.
- Use direct messages for personal, sensitive, or truly individual matters.
- Move a discussion to a document when it needs structure or a durable decision.
- Move to a call when rapid back-and-forth will materially improve the outcome.
- Summarize decisions from private or verbal conversations in the shared place.

## Disagreement and Feedback

Address the work and its impact rather than assigning motive. Ask questions
before assuming intent. Give difficult feedback directly, privately, and with a
specific request where possible.

It is acceptable to pause a tense exchange and return after thinking. A fast
response is less important than a considered one.

## Review Questions

- Can the recipient tell what is being asked of them?
- Are facts, open questions, and non-goals distinguishable?
- Did writing the message clarify the work, or merely narrate activity?
- Is the urgency explicit and justified?
- Is this in the place where future readers will look for it?
- Does the message leave room for a thoughtful response?
