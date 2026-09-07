# Team Geek

Brian Fitzpatrick and Ben Collins-Sussman, 2012. A second edition appeared in
2015 as *Debugging Teams*, broadened for a non-technical audience because the
authors judged the first edition "perhaps a bit too focused on software
engineering". I read it after the [Deep Work](deep-work.md) note left me
with a handbook in which another person's attention is only ever a cost.

## What the Book Argues

The authors ran Subversion and then Google's Chicago engineering office, and
their claim is that the hard problems in software are social rather than
technical. Code can be reasoned about. People cannot, and most projects that
fail do so for reasons that have nothing to do with the code.

Their central target is the **Genius Myth**: the belief that important software
comes from a lone brilliant person working in isolation, and that the rest of
us should aspire to that. They argue the story is told backwards. What looks
like solitary genius was almost always a person surrounded by collaborators who
did not make the biography.

The myth has a practical form, and it is the expensive one. It is hiding work
until it is good enough to show. Hiding is a bet that you understood the
problem correctly, and you only find out you lost the bet after you have spent
the time. Their answer is to fail early, fail fast and fail often, which means
putting rough work in front of people while it is still cheap to be wrong.

The book then works outward: yourself, your team, your leader, difficult
people, the wider organisation, and finally your users. Underneath all of it
sit three pillars.

## The Three Pillars

**1. Humility. You are not the centre of the universe.** Accept that you are
not always right, and that the work is better when other people have had a go
at it. The authors are precise about what humility is not. It is not
self-deprecation or refusing to hold an opinion. It is holding the opinion
while genuinely accepting it might be wrong, which is what makes early sharing
survivable. Without it, showing unfinished work feels like exposure rather than
like getting information.

*Tip: send the half-formed version with the question attached. "Here is what I
think is happening and where I am unsure" costs nothing to be wrong about on
day one and a fortnight to be wrong about on day fourteen.*

**2. Respect. Care about the people, not just the output.** Take the people
you work with seriously as people, and treat their work as work rather than as
something to be corrected. This is where their advice on criticism sits: aim it
at the code and not at the person, and separate the two explicitly, because the
author will not do it for you.

*Tip: in review, write what the change does wrong, never what the author did
wrong. "This drops the error" and "you forgot the error" carry the same
information and land completely differently.*

**3. Trust. Believe others are competent and let them do the work.** Assume
good intent, and let people own things without checking over their shoulder.
The authors are honest that this is the hardest of the three, because it costs
you control and it occasionally goes wrong. Their argument is that the
alternative is worse: a team where nothing can proceed without one person is a
team with a **bus factor** of one, and that is a project risk before it is a
people problem.

*Tip: when I am the only person who knows how something works, that is not job
security, it is an outage waiting for a holiday. Write it down or walk someone
through it.*

The authors treat the three as diagnostic rather than aspirational. Nearly
every social conflict on a team, they claim, traces back to one of humility,
respect or trust being absent. That is a useful thing to check before deciding
that a disagreement is technical.

## What It Confirmed

[Saying I Do Not Know](../docs/saying-i-dont-know.md) is humility with a
mechanism. The doc already says to admit the gap and attach a question. The
book supplies the reason it works, which is that the admission is cheap now and
expensive later, and the cost only ever goes up.

Known, Unknown, Not needed, Next in
[Communication](../docs/communication.md) is early sharing given a shape. It is
a way to publish an incomplete understanding without it reading as confusion,
which is usually the thing that stops people publishing at all.

[Security Over Competition](../docs/security-over-competition.md) is nearly the
same argument arrived at independently. Both say that treating a colleague as a
rival is a losing move, and both locate the fix in the individual rather than
in process.

## What It Changed

**Publish before it is good.** The private network question sat with me for
weeks because nobody had told me how it should work, and I treated that as a
reason to keep reading rather than a reason to write. [Four Stages of a
Task](../docs/four-stages-of-a-task.md) says to name the question. This book
says to publish the half-formed answer along with it, on the day, and let being
wrong in public be the cheap thing it is.

**Count the bus factor on what only I know.** Not as a virtue and not as
documentation debt, but as a list. Anything on it that has no second reader is
a risk I am carrying on behalf of the team without anyone having agreed to it.

**A technical conversation is work, not an interruption to work.** The Deep
Work note scores the message that unblocks the day as shallow. This book scores
the same message as the entire point. When the two disagree, the situation
decides: if the question is already well formed, protect the block; if nobody
can yet say what needs doing, go and talk to someone.

## What I Rejected

The poisonous people chapter, at least as written. The advice on protecting a
project's attention from bad-faith participants is reasonable for a large open
source community. Applied inside a team it turns a person into a category, and
the same behaviour usually has a duller explanation, such as somebody being
under pressure or lacking context.

The authors kept the chapter and its title through the 2015 second edition, so
this is not a reading they later withdrew. The framing does disappear from
Fitzpatrick's 2020 rewrite of the same material in *Software Engineering at
Google*, where the word does not appear at all. In fairness, the chapter itself
already says the thing to remove is the behaviour rather than the person; my
objection is that the label makes that distinction very hard to hold onto.

The organisational manipulation material. It is aimed at engineers stuck under
poor management who need to route around it, and reads as advice for a
situation I am not in. The mission statement and consensus building sections
are similarly written for whoever is running the team.

## Review Questions

- Am I still reading because the answer is not clear, or because publishing an
  unclear answer feels bad?
- What do I know that nobody else on the team knows?
- Did that review comment describe the change, or the person?
- Is this disagreement actually technical, or is one of the three pillars
  missing?
- If this turns out to be wrong, when will I find out, and what will it have
  cost by then?
