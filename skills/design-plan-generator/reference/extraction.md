# Pass 2 detail — Extract

> Part of the `design-plan-generator` skill. See `../SKILL.md` for the full workflow overview and status vocabulary.

Work through the categories below, in this order — some are derived from others:

1. Overview, Design problem, Stakeholders & structure, Deliverables & scope, Constraints — extract these from the sources.
2. Milestones — depends on deliverables being resolved first.
3. Timeline — depends on both cadence (from Stakeholders) and task breakdown (from Deliverables).
4. Additional insights & opportunities — do this last, as a sweep. It's where everything that didn't fit elsewhere lands, plus the gaps in the source that should trigger a proactive suggestion.

Tag each statement as you go, using the status vocabulary in `../SKILL.md` — a source number for Found, inline reasoning for everything else. Out-of-scope items appear in both Deliverables and Constraints as categories below — state them once, in Constraints (under whichever of General or Design-related actually fits it), and cross-reference from Scope rather than duplicating.

These are **lenses, not a form** (see Core commitment 2 in `../SKILL.md`). Many questions will have no signal in a given document and should simply not appear in the output. Most are extractive — they interrogate the document, and their answers become plan content. A few, marked *[construct]*, ask you to build something the source doesn't contain; those are handled in Pass 4 (`derive.md`) and tagged **Proposed**, never Inferred, because the client never asked for them.

An extractive question the document doesn't answer isn't a dead end — it's a candidate question for the user in Pass 3. That's the pipeline this whole system runs on: read, fail to answer, triage, ask, mark what's left Missing.

Intake questions — engagement mode, content layers, document shape, direction, cross-document conflicts — are handled in Pass 1 (`intake.md`) and deliberately not repeated here.

## 1 — Project overview

- What business is the client in, and what's their product?
- What product type and maturity stage is this — new build, redesign, feature add-on, mature platform?
- Who is the end user of the client's product, as distinct from the client-side stakeholders the team works with?
- What specific objective was the agency hired for, and how does it relate to the product's broader objective — the same scope, narrower, or adjacent?
- What business metric or target — growth target, adoption number, revenue figure — defines success for this work, if one is stated?

## 2 — Design problem

- What pain points or complaints does the client state directly?
- What cause or hypothesis is offered for the problem, versus what's only described as a surface symptom?
- What user stories, direct stakeholder or user quotes, or named pain points appear in the source? If none, what does the deliverable list imply about the underlying problem?
- What does the client consider a successful outcome?
- What kind of problem does the source frame this as — UX, visual/brand, process, or strategic — and what language signals that? This shapes which phases of the work matter most.

## 3 — Stakeholders and project structure

- Who requested or signed the source document?
- How are roles indicated — explicit labels (requestor, stakeholder, approver, internal), or only names and titles from which seniority has to be inferred?
- What does any approval or sign-off table reveal about the real decision-maker? A dated sign-off block is more reliable evidence than a job title.
- What agency-side staffing is described — roles, FTE allocation, percentage of time by week? (This staffing picture is also what you'll check task-breakdown day estimates against in Pass 4 — note it with that reuse in mind.)
- What methodology is named, or implied by deliverable cadence — sprints, phases, waterfall milestones?
- What ceremonies or meeting cadences are specified?
- What tool links are provided (Figma, Jira, Drive, Slack), and which are marked as still to be confirmed rather than genuinely absent?

Expect to flag gaps here more than anywhere else. Real documents range from a clean four-row contact table, to a twenty-person roster with no decision-maker identified, to nothing at all.

## 4 — Deliverables and scope

- What concrete deliverables are named?
- To what level is scope decomposed — named sub-items (specific flows, features, journeys) that map directly to tasks, or only high-level deliverables that still need breaking down?
- What phase structure organizes the deliverables, or are they all due at the same point?
- How is priority signalled — explicit language (must, critical, nice-to-have), structural cues (a phase number, an "on deck" or backlog label), or not at all?
- Where is the in-scope/out-of-scope boundary defined — an explicit table, or only inferable from prose?
- What complexity signals exist for each deliverable — a stated document count, number of named flows/screens, member or user count, existing-system count — that a day estimate could be scaled against later?
- *[construct]* What task sequence — down to subtasks — can each deliverable be decomposed into, and how many days does each realistically take? Handled fully in Pass 4 (`derive.md`) and written up per "Deliverables: task breakdown" in `writing-the-plan.md` — don't try to build the estimate during extraction, just collect the complexity signals above while they're in front of you.

Whether the document is a forward-looking scope or a backward-looking coverage record is settled in Pass 1. If it's the latter, this category describes what already exists rather than what to plan. This is also the section "Suggested next actions" (`writing-the-plan.md`) will draw from directly — keep that reuse in mind while you're extracting and decomposing here.

## 5 — Constraints

Sort what you find into two buckets as you go — they end up as two separate subsections in the plan (see `writing-the-plan.md`). The rule of thumb: if it changes what appears on screen or how an interaction works, it's Design-related; if it changes cost, legal exposure, staffing, or internal process without touching the interface, it's General. When something genuinely touches both — accessibility is often written up as a cost line item but shapes components directly — put it where the designer will look for it first, which is usually Design-related. (The same General / Design-related split, and the same rule of thumb, applies to category 8 below.)

**General (business-facing, still worth the designer knowing):**
- What budget-cycle or resourcing constraints appear informally — next year's budget already committed, a role not yet hired — even if absent from the formal scope section?
- What compliance requirements are stated that aren't about the interface itself — data residency, GDPR/privacy responsibility, industry regulation?
- What contractual process constraints affect how design work gets approved or changed — change-order process, review/approval windows, cancellation terms?
- Who owns content rights, warranty terms, and other business-risk allocations that could affect what the designer can safely assume is settled?

**Design-related (shapes what gets designed or how):**
- What existing brand or design system is referenced?
- What tech stack is named, especially anything that constrains UI or interaction patterns (a legacy CMS, a fixed API shape, a specific framework)?
- What's explicitly out of scope for the interface or experience, and what language indicates whether each exclusion is hard or conditional? "Out of scope for now, but we could accommodate it — it would add time and cost" is a negotiable boundary, not a wall, and the difference changes how a designer plans.
- What accessibility requirements are stated, and what's the actual baseline versus what would cost extra?
- What browser, device, or responsive requirements are stated?

## 6 — Design milestones

- Which deliverables double as client-visible checkpoints — sign-off, handoff, review gate?
- What review or approval checkpoints are named at phase transitions, such as a design review window or a final outbrief? Absent those, what can be inferred from deliverable due dates?
- Which milestone requires client approval before the next phase can start?

## 7 — Timeline

- What start and end dates, or fixed external deadlines, are stated?
- How is the timeline expressed — phase-to-week ranges needing sprint breakdown, or already sprint-gridded and directly extractable?
- What blocked or on-hold items affect sequencing — work paused pending a hire or a decision?
- *[construct]* This is where Section 4's task breakdown actually gets placed on the calendar, sprint by sprint or week by week, respecting dependencies (research before wireframes, content model before hi-fi, approval gates before the next phase) — not just a restatement of the phase start/end dates already Found above. Handled fully in Pass 4 (`derive.md`) and written up per "Timeline: placing the deliverables" in `writing-the-plan.md`, including reconciling the day-estimate totals against what the timeline and staffing can actually support.

## 8 — Additional insights and opportunities

Sort these into General and Design-related too, same two subsections and same rule of thumb as category 5: does it change what gets designed or how (Design-related), or is it business/competitive/organizational context that doesn't touch the interface (General)? An insight can legitimately produce one line in each bucket — a competitor's business model is General, but the UX implication you draw from it is Design-related — rather than forcing one framing to carry both halves.

**General:**
- What's mentioned as adjacent but not in scope — "eventually we'd also like..." — when the thing itself is a business/organizational move rather than an interface change?
- What future phases are hinted at, at the organizational or contractual level?
- What does any open-questions log or decision tracker reveal, including decisions since reversed, when the decision is about process, staffing, or scope rather than the interface?
- What informal asides reveal an unstaffed role or an organizational gap?
- What competitive or market context (a competitor's size, model, or positioning) is worth the designer knowing, separate from any design implication it carries?

**Design-related:**
- What informal asides reveal an unresolved design ambiguity or a suggested-but-unscoped interface idea — "maybe we surface a recommendation engine eventually"?
- What does member/user survey or research data in the source imply about design priorities specifically?
- *[construct]* Where are the gaps in the source document itself — no stakeholder map, unclear priorities, no design system — that warrant a proactive suggestion such as a kickoff alignment session, a prioritisation workshop, or a request for missing design assets?
