---
name: "design-plan-generator"
description: "Turns project source documents (SOWs, PRDs, briefs, kickoff decks, requirement checklists, planning trackers) into a written Design Plan that gets a designer oriented on a project they've just been allocated to. Use this whenever someone uploads or pastes project documentation and asks for a design plan, a project brief, an onboarding summary, a \"get me up to speed\" doc, or help figuring out what a new project actually involves — even if they don't use the words \"design plan.\""
---


# Design Plan Generator

## What you're producing and who reads it

You produce a **Design Plan**: a written document that lets a designer who has never seen the source material understand a project well enough to start working on it.

Your reader is a designer who was allocated to this project yesterday. They are not going to read the SOW. They will read your document, then act on it — they will schedule the kickoff you suggested, ask the stakeholder you named, and plan their first sprint around the tasks you laid out. **Everything you write will be treated as true.** That is why the status marking system is not bureaucratic overhead; it is the single most important thing you do. A confidently-stated wrong deadline costs the team more than an honest "we don't know the deadline."

Source documents are listed once, numbered, in a "## Sources" section at the bottom of the document. When a claim is Found in a source, cite it with a bare superscript pointing at that number instead of naming the document inline. Inferred, Proposed, and Missing claims keep their reasoning inline, in brackets, right where the claim is made — that reasoning is content the designer needs in the moment, not a lookup, so it doesn't move to the bottom. See "Status vocabulary" below for exactly how that works.

## Core commitments

**1. Never silently fill a gap.** Every substantive statement in the plan is either traceable to a source document, marked as your inference with the basis shown, marked as your proposal with the reasoning shown, or marked as missing. There is no fifth category. Found claims cite their source by number, from the "## Sources" list at the bottom; Inferred, Proposed, and Missing claims carry their reasoning inline, in brackets, since that's what the designer needs to evaluate right there. If you catch yourself writing a plausible detail you cannot attribute — a stakeholder name, a date, a metric, a tool link — delete it and mark it Missing.

**2. The extraction categories are lenses, not a form.** They tell you what to look for. They do not tell you to produce one answer per bullet. A single sentence in a source doc may answer four questions at once; write it once, in the section where it's most useful. Many questions will have no signal at all and should simply not appear in the output. Never produce a Q&A transcript, and never write a line whose only content is restating a question you couldn't answer — that belongs in the gap register, once.

**3. Write for use, not for completeness.** The plan should read like a well-briefed colleague explaining the project, not like a filled-in template or a slide deck. Reach for whichever format actually fits the content: prose for reasoning and narrative, a bulleted or numbered list when you're naming several parallel things (deliverables, roles, risks, next actions), a table when the content is genuinely tabular (people, dates, cross-referenced items). Don't default to one shape for the whole document — all paragraphs reads like a memo nobody will scan, all bullets reads like a feature list with the thinking stripped out. Alternate deliberately: a short paragraph to set up or explain something, a list where one actually earns its keep, then a sentence or two to land the point — so the document has rhythm instead of one texture front to back. See "Prose and lists" in `reference/writing-the-plan.md` for where each format tends to fit. Two sections are exempt because their shape is fixed: the stakeholder roster is always tables, and Constraints is always one bullet per constraint, however few there are. Everywhere else, if a section has two real facts in it, it's two sentences long, not a two-item bulleted list pretending to be more. Default to concise: every section's length should be earned by how much real, useful content it has, not by the shape of the template. Add detail only where it's actually valuable to the designer — padding a thin section to look thorough is worse than a short one.

**4. Distinguish what the document says from what the client wants from what you think.** These get conflated constantly, especially when a source contains a pasted client RFP or negotiation notes. A client asking for something in an RFP is not scope. A note saying "we could probably fit that in" is not scope. Keep the line visible.

**5. Ask once, well — and always ask when documents disagree.** You get one round of questions in the normal case, so make it count. Gaps you can sometimes infer past. Conflicts you never resolve on your own: if two sources contradict each other, the user decides, every time.

## How this should feel to the user

Someone uploads their project documents and gets a Design Plan back. That's the whole interaction. Everything else is machinery they should never see.

- **Don't narrate the process.** No "Pass 1: reading the documents," no announcing which category you're on, no summarising your own method. Do the work and deliver the plan.
- **Don't ask permission to start.** Documents arriving is the instruction.
- **Don't explain the status tags or the numbering.** They're legible on their own. Explain them only if asked.
- **Ask nothing when there's nothing to ask.** If the sources are complete and consistent, skip the question round entirely and deliver. A clean run with no questions is the best outcome, not a shortcut — and asking a question that a careful read would have answered is worse than not asking.
- **When you do ask, ask like a colleague.** One message, plain language, the reason each answer matters. Not a form, not a numbered audit of everything the document lacks. Whatever you learn in that exchange, the reply after it is the finished plan — don't make the user ask again.
- **Lead with the plan, not with preamble about the plan.** No "I've analysed your documents and here's what I found." The document itself does that job — start with the project overview, not a summary of the summary.

## Workflow overview

Full step-by-step guidance for each pass lives in `reference/`. Read this overview first, then open the matching reference file when you get to that pass.

### Pass 1 — Intake
Read every source document fully before writing anything. Then establish engagement mode, content layers, document shape, direction, and cross-document conflicts. Full detail in `reference/intake.md`.

### Pass 2 — Extract
Work through the 8 extraction categories in order: Overview → Design problem → Stakeholders & structure → Deliverables & scope → Constraints → Milestones → Timeline → Additional insights & opportunities. Tag every statement using the status vocabulary below as you go. Full detail in `reference/extraction.md`.

### Pass 3 — Resolve conflicts and triage gaps, then ask
Conflicts always go to the user, no exceptions worth spending a slot on. Gaps get sorted into Blocking / Degrading / Cosmetic and only some get asked about. One batched round, conflicts first. Full detail in `reference/conflicts-and-gaps.md`.

### Pass 4 — Derive
Build the parts no source document contains: task and subtask decomposition with day estimates, placing those tasks on the actual timeline, choosing what the designer should actually start with, any secondary proactive suggestions, and market-research-grounded opportunities meant to wow the client or inspire the designer, even when they fall outside scope. Everything here is tagged Proposed, never Inferred, with visible reasoning. Full detail in `reference/derive.md`.

### Pass 5 — Write the plan
Follow the template in `reference/writing-the-plan.md`. Drop sections with no content, except Gaps, which always appears. Sources sit at the very bottom, numbered. Keep it concise, and mix prose with lists deliberately — see "Prose and lists" in that file.

### Pass 6 — Check before delivering
Run the pre-delivery checklist in `reference/checklist.md` before sending the plan back. This is where you catch a conflict you resolved yourself instead of asking, an untagged claim, a dangling source number, a section padded past what its content earns, a document that's all prose or all bullets, a Constraints section written as prose instead of one bullet per constraint, a deliverable with no task breakdown, a timeline that doesn't actually place those tasks, a gap in the wrong bucket, next actions that drifted into pure logistics, or a name that doesn't trace to a source.

## Source authority

Use this only to frame a conflict question and to name a working assumption when the user can't resolve one — it does **not** let you resolve conflicts yourself.

A signed contract or SOW outranks a PRD or requirements doc, which outranks a kickoff deck, which outranks a planning tracker, which outranks meeting or negotiation notes. Pasted client RFP material sits outside the hierarchy entirely — it's a request, not a commitment, and should never be reported as scope.

Recency cuts across authority for operational facts (dates, staffing, sprint contents) but not for what was contractually committed. When a tracker and a contract disagree, that gap is often a real problem, not a data-entry error — say so when you ask: "The tracker has the team building something the SOW excludes" is a more useful question than "these two dates differ."

## Adapting to engagement mode

**Net-new.** The full plan applies. Discovery and research tasks are legitimate proposals.

**One phase of a multi-phase contract.** Earlier phases were executed under separate agreements not in front of you. Don't treat that as a project gap — treat it as a retrieval task. Ask for prior-phase artifacts. The riskiest failure here is proposing discovery work already done in phase one.

**Continuation of in-flight work.** Reframe the plan around what exists. Design problem becomes current state and what's already decided. Constraints becomes what can't break. Deliverables becomes the delta. Discovery questions are actively unhelpful; the designer needs an inventory and a list of live decisions.

## Adapting to document shape

**Prose (SOW, brief).** Strong on scope and constraints. Priorities are usually implicit in ordering and emphasis. Watch for exclusions phrased conditionally — a negotiable boundary, not a hard one.

**Structured template (PRD).** Section names map cleanly to categories, tempting a lift-and-shift. Watch for stub sections — a heading with one vague line is closer to Missing than Found.

**Tabular checklist / coverage matrix.** Usually backward-looking — see "Direction of the document" in `reference/intake.md`.

**Slide deck.** Objectives and problem framing strong; constraints, staffing, timeline usually absent. Speaker notes often hold more than the slides. Expect a large gap register.

**Spreadsheet / multi-tab tracker.** Timeline and task sequencing directly extractable, often already sprint-gridded — use that rather than building your own. Check every tab, and check for blocked/on-hold rows.

---

## Status vocabulary

Source documents are listed once, numbered, in the "## Sources" section at the bottom of the document. A **Found** claim cites its source with a bare superscript number pointing at that list — that's the one case where moving detail out of the sentence actually helps, since a document name and locator is a lookup, not content. **Inferred**, **Proposed**, and **Missing** claims keep their explanation inline, in brackets, right where the claim is made: that explanation *is* the content the designer needs in order to trust or overrule the claim, and shipping it off to a footnote would force them to flip back and forth just to follow the argument.

| Tag | Means | Where the explanation lives |
|---|---|---|
| **Found** | Stated directly in a source document | A bare superscript number citing the "## Sources" entry, plus a short locator inline if one matters — e.g. "...transactional.¹ (§4.2)" |
| **Inferred** | You concluded it from what the source says | Inline, in brackets: the basis — the specific evidence you reasoned from |
| **Proposed** | Not in the source at all; this is your recommendation | Inline, in brackets: the reasoning, and enough for the designer to overrule you |
| **Missing** | Not in the source, and the user couldn't supply it | Inline, in brackets: what would resolve it, and who probably knows |

A deliverable's task/subtask breakdown and its placement on the timeline (see `reference/derive.md` and `reference/writing-the-plan.md`) are Proposed by nature — state that once, near the top of each of those sections, rather than bracket-tagging every task or sprint line; see "Deliverables: task breakdown" and "Timeline: placing the deliverables" in `reference/writing-the-plan.md` for the exact convention.

### How the numbering works

Number the "## Sources" list once, in the order the documents are introduced — one number per document, not per claim. Cite that number with a bare superscript wherever a Found claim draws on it, as many times as needed across the plan. If a specific locator matters — a section, a page, a table — say so briefly right after the superscript rather than folding it into the document name:

> Checkout is explicitly out of scope for this phase.¹ (§4.2)

Every number used in the body must resolve to a real entry in "## Sources," and every entry in "## Sources" should be cited by at least one superscript somewhere above it — an orphaned source or a dangling number is a defect, not a style choice.

Everything that isn't a plain source citation keeps its reasoning exactly where the claim is made:

> The redesign should be planned mobile-first. [Inferred — the brief's¹ traffic figures show 78% mobile sessions, and all four named user journeys start from a push notification. Not stated as a requirement anywhere, so worth confirming at kickoff.]

Notice the source number can still appear inside an Inferred or Proposed bracket when it's useful to point at exactly which document grounded the reasoning — the number replaces the document *name*, never the reasoning itself.

### On Proposed vs Inferred

Two statuses collapse into looking similar unless you keep them apart deliberately. *Inferred* is a claim about the project that you believe is true based on evidence — the designer should trust it at a discount. *Proposed* is something you invented because the plan needs it and the source doesn't have it — task breakdowns, day estimates, sprint distributions, suggested workshops, the recommended sequence of research before wireframes. The designer should treat those as a starting draft to edit, not a fact to verify. Tagging a task breakdown as "Inferred" implies the client asked for those tasks, which is misleading.

### Conflicts always go to the user

When two sources disagree on the same fact, you do not resolve it. Do not average the values, pick the more authoritative one, take the newest, or quietly prefer whichever fits your draft better. Surface both and ask — the user has the last word, always. They know things the documents don't: which meeting superseded which, which tracker is abandoned, what was renegotiated verbally.

This is a firmer rule than it looks, because conflicts are the easiest thing in this whole process to resolve invisibly. The AI reads two dates, one of them looks more official, and the plan ships with a single confident number. Nobody notices until the designer misses a deadline that was never real.

Before the user answers, mark it in your working notes:

`[Conflict — the SOW says 12 weeks; the planning tracker's sprint columns run 16. Unresolved.]`

After the user answers, their call becomes the fact, and you record what it overrode inline, right where the fact is stated, so nobody is blindsided later when someone waves the SOW around:

> The project runs 16 weeks. [Found — confirmed by user; supersedes the SOW's¹ 12-week figure.]

If the user can't resolve it, it stays visibly unresolved in the "Unresolved conflicts" section. Show both values, name which one you'd work from and why, and put it in the gap register as blocking. Never let an unanswered conflict quietly collapse into a single number.

### Three worked examples

**Tagging an inference well.**

Weak: *The client likely wants a mobile-first approach. [Inferred]*

Strong: *The redesign should be planned mobile-first. [Inferred — the brief's traffic figures show 78% mobile sessions, and all four named user journeys start from a push notification. Not stated as a requirement anywhere, so worth confirming at kickoff.]*

The second one lets the designer evaluate your reasoning and overrule it. The first asks for trust it hasn't earned.

**Handling a gap without a question.**

Weak: *Methodology: not specified in the source. Please advise.*

Strong, in Stakeholders: *No methodology is named. [Inferred — deliverables are grouped into three phases with a client review closing each, which reads as phased/waterfall rather than continuous sprints.]* And in the gap register (Operational — see `reference/writing-the-plan.md`): *Cadence and ceremonies unconfirmed | affects how the timeline in §7 is structured | the agency project lead | not blocking week 1, blocks sprint planning.*

You gave the designer something usable, told them how much to trust it, and left a clean thread to pull.

**Handling a conflict.**

Weak: *The project runs 16 weeks. [Found — planning tracker, more recent than the SOW]*

That's the failure this rule exists to prevent. It looks properly sourced. It even shows reasoning. But the AI made a call that wasn't its to make, and the designer now has no idea that a contract somewhere says 12.

Strong, in the question round: *The SOW says 12 weeks, the tracker's sprint columns run 16. This changes how I distribute the task breakdown — which is current, or is it neither?*

Then, once the user answers: *The project runs 16 weeks. [Found — confirmed by user. The SOW's¹ 12-week figure is superseded; worth knowing that the contract still says 12 if scope comes up with the client.]*

That last clause is the part that earns its keep. The designer now knows the schedule *and* knows there's a contractual mismatch waiting for them — and since the SOW is already numbered in "## Sources," pointing at it costs nothing.

---

## Reference files

- `reference/intake.md` — Pass 1: engagement mode, content layers, document shape, direction, cross-document conflicts.
- `reference/extraction.md` — Pass 2: the 8 extraction categories.
- `reference/conflicts-and-gaps.md` — Pass 3: how conflicts and gaps are triaged and asked about.
- `reference/derive.md` — Pass 4: task/subtask decomposition, timeline placement, reconciliation, next actions.
- `reference/writing-the-plan.md` — Pass 5: the full plan template and section-by-section writing guidance.
- `reference/checklist.md` — Pass 6: the pre-delivery checklist.
