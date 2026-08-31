# Writing Chronologically

I was describing a requests tab and could not make the design clear. I knew
that it showed allow-title requests, that the requests belonged to a title,
and that this was different from publishing. The facts were present, but the
relationship between them was not.

The explanation became clearer when I wrote it in the order the system runs:

1. The page loads a title.
2. It calls the API with the titleId.
3. The API returns an array of requests for that title.
4. The page displays each allow-title request in the array.

Once the sequence was visible, so was the question I had not been able to
name: publishing a title does not follow the same sequence. It is a separate
operation, not another mode of the requests tab.

Chronology did more than explain the design. It exposed where one design ended
and another began.

## Write in the Order the System Runs

When explaining behaviour, follow the path a request, event, or decision takes:
the trigger, the action, the response, the resulting state, and the next thing
that uses that state.

This gives the reader a chain they can inspect. If they disagree, they can
point to the exact step where their understanding differs. If a step cannot be
explained, the limit of my understanding is visible before it becomes an
assumption.

Writing by category does not provide the same test. Separate paragraphs about
the API, data, and interface may each be accurate while leaving the connection
between them unstated. Categories help a reader look up facts. Chronology helps
them understand behaviour.

## Use the Same Order for Bugs and Incidents

For a bug, write what triggered the behaviour, what the system did, what was
expected, and where the observed result diverged.

For an incident, write what changed, which effect appeared next, how the impact
spread, and what interrupted that sequence. Do not begin with a collection of
logs and observations and leave the reader to reconstruct the event.

The sequence should distinguish evidence from inference. "The client sent the
request, the gateway returned 403, and no service trace was created" is an
observed sequence. "The gateway rejected the request before it reached the
service" is the conclusion supported by that sequence. Writing both makes the
reasoning inspectable.

## Let a Missing Step Remain Missing

Do not join two observed events with a cause I have not verified. If I know
that one event happened and another followed, but not how they are connected,
write the gap plainly.

That gap is usually the **Unknown** in the Known / Unknown / Not needed / Next
structure from [Communication](communication.md):

> **Known:** The client sent the request and received 403. No service trace was
> created.
>
> **Unknown:** Whether the gateway rejected the request or routed it somewhere
> else.
>
> **Next:** Capture the gateway trace for the same correlation ID.

An incomplete sequence is more useful than a complete-sounding explanation
built on an assumption. It shows where investigation should continue.

## Separate System Order From Discovery Order

The order in which I learned something is usually not the order in which the
system does it. Investigation includes wrong assumptions, repeated searches,
and facts discovered before I understood their relevance. Reproducing that
journey makes the reader repeat my confusion.

Write the system's order in the final explanation. Include the discovery order
only when the wrong turn is itself useful—for example, when another person is
likely to make the same assumption and needs to know why it fails.

Investigation notes may remain chronological to preserve evidence. The final
technical explanation should reorganize that evidence around the behaviour
being explained.

## Lead With the Point

Writing chronologically does not mean withholding the conclusion until the
end. State the request, decision, or finding first, then provide the ordered
account that supports it.

For example:

> The requests tab and title publishing need separate designs. The requests
> tab loads allow-title requests by titleId, while publishing follows a
> different operation.

The sequence can follow underneath. The opening tells the reader why the
details matter; the chronology lets them verify the claim. This keeps the
message consistent with [Communication](communication.md): make the required
action clear without making the reader reconstruct the reasoning.

## Name Each Step Precisely

A sequence is useful only when its steps can be checked. "It calls the service
and gets the data" has an order but not enough information to investigate.
"The page calls the API with the titleId and receives an array of allow-title
requests" identifies the input, boundary, and result.

When I do not know the correct term, say so and find it. Writing around a
missing term hides the same kind of unknown as writing around a missing step.
[Saying I Do Not Know](saying-i-dont-know.md) applies to vocabulary as much as
it applies to behaviour.

## Use Chronology When Order Carries Meaning

Not every document should be a sequence. A reference page, a comparison, and a
list of constraints are easier to use when organized by subject.

Use chronology when the reader needs to understand how something behaves, why
something happened, or where a result diverged from expectation. Use categories
when the reader needs to find independent facts. If changing the order would
change the explanation, the order is part of the information.

## Review Questions

- Can the reader follow the request, event, or decision from beginning to end?
- Is this the order the system runs, or only the order in which I learned it?
- Which statements are observations, and which are conclusions?
- Have I left an unknown visible instead of filling it with an assumption?
- Does the reader know the point before the supporting sequence begins?
- Is each step precise enough for someone else to verify?
- Does order carry meaning here, or would a reference structure work better?
