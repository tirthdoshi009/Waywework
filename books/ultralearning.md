# Ultralearning

Scott H. Young, 2019. Read while trying to work out why some systems became
clear to me in a week and others stayed opaque for months.

## What the Book Argues

Learning fails in three predictable ways. Practice happens in conditions that
do not match the conditions of use, so nothing transfers. Review feels
productive because recognising material is easy, so recognition gets mistaken
for recall. Honest correction is uncomfortable, so people collect feedback
that flatters instead of feedback that corrects.

Ultralearning is Young's name for learning that is self-directed, intense, and
strategic: the learner owns every decision, chooses the method that works over
the method that is comfortable, and researches the territory before entering
it. The nine principles below are each an attack on one of the three failures.

## The Nine Principles

- **Metalearning — first draw a map.** Before studying anything, research how
  the subject is structured and how people successfully learn it. Young's
  guideline is to spend around ten percent of the project's time on this.
  Answer why you are learning it, what concepts, facts, and procedures it
  contains, and how others have learned it. Prevents effort spent on the wrong
  material in the wrong order. *Tip: before opening the code, spend fifteen
  minutes listing the unknowns and sorting them into concepts, facts, and
  procedures. Concepts get traced, facts get looked up once, procedures get
  done.*
- **Focus — sharpen your knife.** Treat concentration as a trainable capacity
  with three separate failures: not starting, not sustaining, and not focusing
  well. Short commitments fix the first, spaced sessions and a cleared
  environment fix the second, and matching the intensity of the state to the
  kind of task fixes the third. Prevents being busy with the material without
  encoding any of it. *Tip: put the hard trace in a booked block with
  notifications off, and leave the shallow work for the fragmented hours. Do
  not spend a rare uninterrupted hour on something interruptible.*
- **Directness — go straight ahead.** Practise the actual skill in conditions
  as close as possible to the ones where it will be used. Build the real
  project, speak the real language, give the real talk. Where that is unsafe,
  simulate it. Prevents transfer failure, which is knowledge that cannot be
  used outside the room it was learned in. Young is explicit that this is
  uncomfortable by design, because it means being visibly bad at the real
  thing. *Tip: to learn a service, ship the smallest real change to it rather
  than reading it end to end. One merged one-line fix teaches more than a day
  of reading.*
- **Drill — attack your weakest point.** Find the component that is limiting
  overall performance, isolate it, practise it on its own, then put it back
  into the whole skill. The bottleneck is identified through direct practice
  first, so drilling is never the starting point. Prevents rehearsing what is
  already strong. *Tip: keep a note of the step that slows me down each week.
  When the same step appears three times, spend thirty minutes practising only
  that step, away from real work.*
- **Retrieval — test to learn.** Recall from memory instead of reviewing.
  Close the book and write down what you know, before you feel ready.
  Attempting a problem before being shown the answer improves how well the
  answer is encoded, even when the attempt is wrong. Prevents the illusion of
  competence, where recognising the material is mistaken for being able to
  produce it. *Tip: write the Known / Unknown / Not needed / Next from memory
  with the sources closed, then open them and correct it. The corrections are
  the actual result.*
- **Feedback — do not dodge the punches.** The type matters more than the
  amount. Outcome feedback says whether it worked, informational feedback says
  what was wrong, and corrective feedback says what was wrong and how to fix
  it. Design practice so the third kind arrives. Discard noise, which is
  variation that reflects luck rather than performance, and discount praise,
  which feels good and displaces the information that would have helped.
  *Tip: when a review says the change is fine, ask what would have made it
  wrong. "Looks good" is outcome feedback; the answer to that question is
  corrective.*
- **Retention — do not fill a leaky bucket.** Forgetting begins immediately, so
  retention has to be built in rather than assumed. Space reviews at widening
  intervals rather than massing them, practise skills until they run without
  effort, keep going past the point of first mastery, and use memory aids for
  the facts that resist all of that. *Tip: reopen one investigation note a week
  and reconstruct it from memory before reading it. What I cannot reconstruct
  is what I never understood.*
- **Intuition — dig deep before building up.** Understanding is built by
  refusing shortcuts, not by talent. Sit with a hard problem for a set period
  before looking up the answer, derive a rule rather than memorise it, start
  from a concrete example before generalising, and explain the idea as though
  to someone with no background. Gaps in the explanation are gaps in the
  understanding. Prevents pattern-matching that collapses when the problem
  changes shape. *Tip: before asking anyone, write down what I expect the
  answer to be and why. Send the question anyway; the prediction costs twenty
  minutes and makes the answer stick.*
- **Experimentation — explore outside your comfort zone.** Copying a proven
  method is right at the start and insufficient later, because at the frontier
  no one method covers the ground. Compare approaches directly, impose
  constraints that force new ones, and combine skills from unrelated areas.
  Prevents the plateau that comes from only ever executing what was taught.
  *Tip: experiment where failure is free. A scratch branch, a trace nobody
  needs, a design that will not ship. Not on the change that is going out
  today.*

Young's own caveats are worth keeping. The principles are simultaneous
supports rather than a sequence. An ultralearning project is demanding and is
not the right tool for every subject, and the principles can be applied inside
ordinary learning time without running a project at all.

## What It Confirmed

The definition of understanding in [Four Stages of a Task](../docs/four-stages-of-a-task.md)
is the book's Feynman technique with a prediction test attached. Stating the
problem to someone who has read none of the sources is the explanation half;
predicting what will break is the half most people skip.

Known / Unknown / Not needed / Next in [Communication](../docs/communication.md)
is free recall with a structure. Writing it from memory before rereading the
evidence is the version that teaches; writing it with the sources open is
transcription.

Rollout rings in [Pace](../docs/pace.md) are a corrective feedback ladder.
Each ring surfaces a class of failure the previous one could not, which is the
same reason drills are ordered by bottleneck rather than by comfort.

Starting from the smallest step someone can correct is directness. So is
reading the actual code instead of the summary of it.

## What It Changed

Say the prediction before asking. [Saying I Do Not Know](../docs/saying-i-dont-know.md)
says to do the reading that is cheap and ask about what stays expensive. That
is a good policy for resolving an unknown and a poor one for learning, because
the expensive part is where the understanding is and it gets outsourced every
time. Sit with the expensive unknown for a bounded period, write down what I
expect the answer to be, then ask. The question still goes out on the same
timeline. A wrong prediction makes the answer stick.

Reconstruct one old investigation note a week from memory before opening it.
The gap between what I recall and what I wrote is the only concrete measure of
the "deeper technical understanding" that [Security Over Competition](../docs/security-over-competition.md)
asks for. Ten minutes, no new work in progress.

Separate a slow step from a missing skill. Four Stages says stalled work is
usually an unasked question rather than a missing skill. That is right often
enough to be dangerous. When the same kind of step is slow across three
unrelated tasks, it is a skill bottleneck, and the fix is to practise it once
off the critical path rather than pay the tax on every task.

Map before reading. Naming the question gives an exit condition but not a
route. Before opening anything, sort the unknowns into concepts, facts, and
procedures. Concepts need tracing, facts need looking up once, procedures need
doing. Treating all three as reading is how reading becomes browsing.

## What I Rejected

Flashcards, a spaced repetition tool, a personal curriculum, and a learning
backlog. Those are built for taking a subject from zero. I am learning systems
while working inside them, which is already direct, and each of those would add
a standing commitment that [Working With Restraint](../docs/working-with-restraint.md)
exists to prevent.

The intensity. The book is aggressive by design and treats discomfort as
evidence the method is working. That does not fit a handbook whose mantra is to
react less and give more. Take the mechanisms, leave the pace.

## Review Questions

- Did I write what I expected the answer to be before I asked?
- Did I write the Known / Unknown / Not needed / Next from memory, or with the
  sources open?
- Can I still explain last month's investigation without rereading the note?
- Is this step slow because a question is unasked, or because I cannot yet do
  the step?
