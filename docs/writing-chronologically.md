# Writing Chronologically

Technical explanations are easier to inspect when they follow the order in
which a system behaves.

While documenting two related operations, describing their properties did not
make their relationship clear. Writing each operation in the order it ran
showed which steps were known and where the explanation depended on an
assumption:

1. A person initiates an action.
2. One component sends data to another.
3. The receiving component returns a result.
4. The result changes what the person sees or can do next.

Writing one operation this way does not explain the other. Each path must be
traced before their relationship can be stated or a design decision can be
made. The sequence makes the missing relationship visible without filling it
with a convenient explanation.

Chronology is useful when the order is part of the information. It is not a
substitute for evidence, precise terminology, or an account of the system's
boundaries.

## Write in the Order the System Runs

When explaining behaviour, follow the path taken by the request, event, or
decision. Name the initial state, trigger, operation, response, resulting
state, and next consumer when each is relevant.

Use precise, checkable terms. "The interface gets the data" does not identify
enough for another person to verify the account. Name the component, operation,
input, and result when they matter.

Do not include steps merely to make the account look complete. A step that
cannot be supported should remain an explicit unknown. Do not silently change
the kind or scope of data between two steps unless the transformation has been
observed.

## Do Not Let Order Imply Cause

One event following another does not prove that the first caused the second.
A chronological account should distinguish:

- **Observed:** what the available evidence directly shows;
- **Inferred:** the explanation currently supported by that evidence; and
- **Unknown:** the connection that has not yet been verified.

An inference should not be presented as another step in the sequence. If an
action is followed by an error, the order alone does not prove which step
failed. It may support a hypothesis, but another condition may explain the
same observation.

Use the Known / Unknown / Not needed / Next structure from
[Communication](communication.md) when an unverified connection matters to the
work. An incomplete but accurate sequence is more useful than a fluent account
that hides an assumption.

## Separate System Order From Discovery Order

The order in which a system behaves is usually different from the order in
which its behaviour is discovered. Investigation may include wrong assumptions,
repeated searches, and facts found before their relevance is understood.

Preserve discovery order in investigation notes when it provides useful
evidence. Organize the final explanation around the system's behaviour so that
readers do not have to repeat the investigation.

Include a wrong turn only when it is useful—for example, when another person is
likely to make the same assumption and needs to know why it fails.

## Use Another Structure When Order Is Not Enough

Not every system has one linear order. Asynchronous work, retries, fan-out, and
concurrent events may form several related paths rather than one sequence. Do
not flatten them into a single narrative that the evidence does not support.

Choose the structure that carries the important information:

- use a comparison when two operations need to be distinguished;
- use a state model when valid transitions and lifecycle rules matter;
- use a dependency map when several components or effects interact; and
- state an invariant directly when it applies across every path.

A sequence describes one path through a system. It may not explain the system's
architecture, ownership boundaries, or rules that remain true across all
paths.

## Lead With the Point

Chronology organizes the supporting explanation, not necessarily the message
as a whole. State the request, decision, or finding first, then provide the
ordered account that supports it.

This tells the reader why the sequence matters without asking them to
reconstruct the purpose of the message from the details.

## Review Questions

- Would changing the order change the explanation?
- Is this the order the system runs or the order in which it was investigated?
- Which statements are observations, inferences, and unknowns?
- Does the sequence imply a cause that has not been verified?
- Is each step precise enough for another person to check?
- Would a comparison, state model, dependency map, or invariant be clearer?
