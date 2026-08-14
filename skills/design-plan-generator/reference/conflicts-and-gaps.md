# Pass 3 detail — Conflicts and gaps

> Part of the `design-plan-generator` skill. See `../SKILL.md` for the full workflow overview and status vocabulary.

You have two kinds of question, and they behave differently.

## Conflicts come first, and you ask about all of them

Every substantive disagreement between documents goes to the user. These aren't subject to the triage below and they don't compete with gap questions for space — they're fast to answer, they're picks rather than compositions, and getting one wrong silently corrupts everything downstream of it. Lead with them.

Ask a conflict like this: show both values, name the source of each, and say what the choice affects. Offer a third option, because sometimes both documents are stale.

> The two sources disagree on duration. The SOW says 12 weeks; the planning tracker's sprint columns run 16. This determines how the task breakdown gets distributed, so it's worth settling first — which is current, or is it neither?

The one narrow exception: a discrepancy with no substantive content — a name spelled two ways, a date off by one in an obviously superseded draft — doesn't need a question. Pick the likelier reading, note it in a single inline aside, and don't spend a slot on it. Keep this exception narrow. If the difference could change what someone does, it's substantive, and it goes to the user.

## Then sort your gaps by urgency, and separately by kind

Urgency (does this gap get asked about at all):

- **Blocking** — the designer cannot start, or will plan wrongly, without this. No timeline. No named approver when there are sign-off gates. Unclear whether a major deliverable is in scope.
- **Degrading** — the plan works without it but is weaker. Missing success metric. No stated methodology.
- **Cosmetic** — leave it. Don't ask.

Ask about the blocking ones and the degrading ones that are cheap for the user to answer. Skip anything you can reasonably infer — inferring with the basis shown inline is more useful to the user than a question they have to answer.

Kind (which bucket the gap lands in once it's written up — see "Gaps to close" in `writing-the-plan.md` for the full definitions): **Operational** (access, stakeholders, ownership, process), **Technical** (design system, integrations, tooling), or **Strategic** (business goals, north star metrics, success criteria). Keep this classification in mind as you triage — it doesn't change whether you ask, but it's worth noting alongside each gap so you're not reclassifying from scratch when you write the plan.

## How to ask

- One batched round: conflicts first, then gaps. Five gap questions is comfortable; seven is the ceiling. More than that and people abandon.
- **Show your current belief and ask for a correction, not a composition.** "I read the timeline as starting mid-September and ending in November, from the phase table — is that right?" is answerable in five seconds. "What is the timeline?" is homework.
- Say what each answer unblocks, so the user can triage too.
- Make skipping explicit and cost-free: they may not know, and that's a legitimate answer.
- Never ask about something that's in the documents. It reads as though you didn't read them.
- If the platform supports selectable options, offer them — conflicts in particular are a natural fit, since the answer is usually one of two known values.

## After the round

Fold in what you got, tag resolved conflicts inline with the user's call and what it superseded (see the status vocabulary in `../SKILL.md` for the exact format), mark unanswered items **Missing** or **Unresolved** inline, and move on. Do not ask again.

A second round is warranted only if an answer opened a genuinely new blocking question — for instance, the user reveals this is phase two of a project you'd been reading as net-new.
