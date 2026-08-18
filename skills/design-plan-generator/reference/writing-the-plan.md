# Pass 5 detail — Writing the plan

> Part of the `design-plan-generator` skill. See `../SKILL.md` for the full workflow overview and status vocabulary.

Use this structure. Drop sections that have no content rather than including them empty — except Gaps, which always appears. Sources always appears last, numbered. Start directly with the project overview — there's no separate summary-of-the-summary section up top; the plan should be concise enough that it doesn't need one.

```
# Design Plan — [Project name]

## 1 — Project overview
## 2 — Design problem
[Optional: a short framing description directly below the title, if the
problem needs a sentence or two of context before the subsections below
make sense. Skip it when the subsections speak for themselves.]
### Framing
### Cause/hypothesis
### Pain points
### Successful outcome
## 3 — Stakeholders and project structure
### Client team
### Internal team
## 4 — Deliverables and scope
## 5 — Constraints
### General
### Design-related
## 6 — Design milestones
## 7 — Timeline
## 8 — Additional insights and opportunities
### General
### Design-related

## Unresolved conflicts
[Only if any survived Pass 3. Each: what the two sources say, which one
you're working from and why, and who can settle it. Omit this section
entirely when there are none — don't leave an empty heading implying
disagreement that doesn't exist.]

## Gaps to close
### Operational
### Technical
### Strategic
[Each subsection, if it has anything in it: a table of gap | why it
matters | who probably knows | what it blocks, ordered blocking-first
within the subsection. Drop any of the three with nothing in it — this
is the designer's to-do list for their first two days, so make it
actionable; a gap with no owner and no consequence isn't worth listing.]

## Suggested next actions
[Design work first, straight from Deliverables/Timeline — see "Choosing
what to start with" in derive.md. Secondary logistics items only if they
aren't already covered in the gap register.]

## Sources
[Each document used, numbered in the order it was introduced: name, type,
date if known, and what it was good for. Note the engagement mode and, if
relevant, that a source is backward-looking. Every number here should be
cited by at least one superscript somewhere above, and every such
superscript above should resolve to a number here.]
```

Section content follows the categories in `extraction.md`. Conflicts the user resolved don't get a section of their own — they're settled facts now, tagged in place inline with what they superseded (see the status vocabulary in `../SKILL.md`). Sections 2, 3, 5, 8, and the gap register are the five with a fixed subsection split — drop any individual subsection if it's empty, same as any other section, but don't merge them back into one undifferentiated list.

## Design problem: four subsections

Section 2 is split into four subsections so a designer can scan straight to the one they need rather than reading a wall of mixed reasoning: **Framing**, **Cause/hypothesis**, **Pain points**, **Successful outcome** — see `extraction.md` for what goes in each. Drop any of the four that has no content, same as any other subsection.

An optional short description can sit directly below the `## 2 — Design problem` title, before the first subsection, if the problem genuinely needs a sentence or two of context to make the subsections legible — for instance, naming the product and user at a glance before diving into Framing. Skip it when the subsections are clear on their own; don't manufacture a summary just to fill the space.

```
## 2 — Design problem

The current member portal is failing the one persona it was built for: a
time-pressed executive who needs fast peer-benchmarking answers, not a
content browser.¹

### Framing
Client language frames this as a content-discoverability problem, not a
visual-brand one — every named frustration is about finding the right
research fast, not how the site looks.¹ [Inferred — no visual/brand
language appears anywhere in the source material.]

### Cause/hypothesis
The current search is keyword-only with no filtering by content type or
interest group.¹ [Inferred — this, not visual design, is why members
report giving up and emailing staff directly instead of searching.]

### Pain points
"We have no single source of truth for our members" — stated directly by
the VP of Product Operations.¹

### Successful outcome
The client considers this successful when staff stop fielding manual
content requests and members self-serve instead.¹
```

## Stakeholders: client and internal, as tables

Section 3 splits the roster into two tables — client team and internal team — rather than one undifferentiated list, since a designer scanning this wants to know at a glance which side of the table a name sits on. Each table shares the same three columns: **Name**, **Role**, **Notes**. Notes is the catch-all for anything that doesn't fit the first two — context on why the person matters, FTE allocation or percentage of time (internal side), decision-making authority, a dated sign-off, or a flag that an entry is Inferred rather than Found.

```
### Client team

| Name | Role | Notes |
| --- | --- | --- |
| Jane Doe | VP of Product Operations | Signed the SOW; primary point of contact¹ |

### Internal team

| Name | Role | Notes |
| --- | --- | --- |
| John Smith | Design Lead | 50% allocation, weeks 1–6¹ |
```

Drop a table entirely if the source gives nothing for that side. An internal staffing table with only roles and allocation, no names yet, is still worth including; a client table with neither names nor titles is a gap for the register, not a table with a blank row. Methodology and cadence notes — sprints vs. waterfall, ceremonies, tool links — stay below the tables as prose or a short list, exactly as before; the tables replace only the roster itself.

## Deliverables: task breakdown

Section 4 does two jobs, not one: report what the source says the deliverable is (Found/Inferred, exactly like every other section), then break it into the tasks and subtasks a designer would actually work through to produce it, with a day estimate on each task. The second half doesn't exist in any source — it's Proposed throughout — but it's also the part of the section a designer actually opens the document to use: a real starting checklist, not just proof that a deliverable was mentioned somewhere.

State the estimating basis once, near the top of the section (see "Task and subtask decomposition" in `derive.md`). Then, for each deliverable: a short framing sentence or two giving what the source says it is, followed by its tasks as a list, subtasks indented underneath each task, with a day range inline on the task line, closed out with a subtotal:

```
**Content Designs and Plan**

A content model and migration-ready plan for existing CEATI research documents.¹

- Content audit — 2–3 days: inventory existing PDFs/Word docs, tag by type and
  interest group, flag anything already outdated
- Content model — 2 days: define content types (project, webinar, RFI,
  benchmarking report), map fields per type
- Migration plan — 1–2 days: sequence the ~20 pilot documents², note what's
  deferred to Phase 2

**Subtotal: 5–7 days**
```

The subtotal is as far as Section 4 goes — placing these tasks on the calendar and checking the subtotal against available time both happen in Section 7, not here, so the deliverables section stays a catalog of what to build rather than duplicating the schedule.

Skip the task breakdown only for a deliverable that's genuinely atomic and non-design (e.g., a systems-architecture document that's really an engineering artifact the designer just needs to know exists) — say so in one line rather than forcing a checklist onto something that doesn't need one.

## Timeline: placing the deliverables

Section 7 is not a restatement of the phase start/end dates already Found in Section 4 or Section 1 — it's where every task from Section 4's breakdown actually gets put on the calendar.

Default to a table with deliverables as rows and sprints as columns: first column header is **Deliverable**, each following column header is a sprint (with its week range), and each cell holds what happens for that deliverable in that sprint — blank if there's no activity that sprint. This gives a designer a visible timeline at a glance: scan a row to see how a deliverable moves across sprints, scan a column to see everything landing in a given sprint.

```
**Phase 1 — Discovery (6 weeks / 3 sprints)**

| Deliverable | Sprint 1 (Weeks 1–2) | Sprint 2 (Weeks 3–4) | Sprint 3 (Weeks 5–6) |
| --- | --- | --- | --- |
| Outcomes workshop | Kickoff | | |
| Content audit | In progress | | |
| Stakeholder interviews | Kick off | | |
| Content model | | In progress | |
| Design audit + wireframes | | In progress | |
| CMS shortlist | | In progress | |
| Concept testing | | | In progress |
| Hi-fi mockups | | | In progress |
| Feature prioritization | | | In progress |
| Phase 2 work plan | | | Drafted |

Estimated: 24–29 designer-days across 6 weeks with 1 designer allocated full-time
— comfortably inside the available time.
```

Use one table per phase when a project spans multiple phases with different sprint cadences — don't force phases with different sprint counts into a single table. Keep rows at the deliverable level rather than one row per task or subtask, so the table doesn't grow past what's legible; if a deliverable's work genuinely splits across sprints in a way worth flagging, say so inline in the cell (e.g., "audit" in one column, "model" in the next) rather than adding a row per subtask.

Fall back to a grouped list only when the table stops being legible — gauge that by total cell count (deliverables × sprints), not sprint count alone, since a narrow table with many sprints but few deliverables can stay scannable well past 5 columns, while a wide one with many deliverables gets unreadable much sooner. As a rule of thumb, fall back once deliverables × sprints exceeds roughly 40–50 cells, or deliverables alone exceed a dozen, whichever comes first. Avoid a Mermaid or similar chart block regardless: a chart block simply won't render at all unless the viewer happens to support that syntax, where a markdown table degrades gracefully everywhere (Word, Notion, a plain markdown preview).

Close each phase's table (or grouping, if using the list fallback) with the reconciliation line from `derive.md` — the day-estimate total against what that phase's timeline and staffing actually support, stated plainly whether it's comfortable, tight, or over-allocated.

## Additional insights: bullets, and unmistakable AI proposals

Section 8 renders as bullet lists in both subsections — General and Design-related — never prose paragraphs. This is a scan section: a designer should be able to run down it in seconds, not read it as narrative.

The Design-related subsection carries two different kinds of content, and they should look different on the page so neither gets mistaken for the other:

- **Gap-driven proactive suggestions** (see "Proactive suggestions" in `derive.md`) — a kickoff alignment session, a prioritisation workshop — close a hole the source itself left open. These read like ordinary Proposed content, tagged inline the same as anywhere else in the plan.
- **Market-driven opportunities** (see "Market-driven opportunities" in `derive.md`) — ideas with no basis in any source, grounded instead in your own market or competitive research, meant to wow the client or spark the designer's own thinking. Propose these even when they fall outside the stated scope — say so plainly rather than dropping a good idea for not fitting the SOW. Because nothing here traces to a source, lead each one with a bold **Proposed** tag rather than the ordinary inline bracket, so it's unmistakable at a glance that this is the AI's own idea and not something the client asked for.

```
### Design-related

- A prioritisation workshop would help before Sprint 1 starts. [Proposed — no priority
  signal anywhere in the deliverables list, and three of five items look equally urgent.]
- **Proposed:** Competitors in this space have moved from filter-only discovery to an
  AI-assisted search bar — this could be a strong differentiator here even though it
  falls outside the current scope. [Grounded in a quick market scan of comparable
  member-portal products; worth raising with the client as a Phase 2 idea rather than
  something to build into the current SOW.]
```

## Gaps to close: three kinds, not one list

Classify every gap that survived Pass 3's triage into exactly one of three buckets, using whichever bucket names the actual missing thing rather than the deliverable it happens to affect:

- **Operational** — access, stakeholders, ownership, process. Who does what, who's missing, what isn't scheduled or decided yet. A missing approver is Operational even though the deliverable it blocks is a hi-fi design; a tool or environment access gap is Operational even though engineering will be the one to grant it.
- **Technical** — design system, integrations, tooling. What technical or design-system asset is missing, unconfirmed, or looks like boilerplate that doesn't actually apply.
- **Strategic** — business goals, north star metrics, success criteria. What the project is actually trying to achieve, and how anyone will know it worked, when that's directional rather than measurable.

When a gap seems to fit two buckets, default to whichever one the missing *thing* actually is: "no named approver for the design system" is Operational (ownership), not Technical, even though the artifact in question is technical. Drop any of the three subsections that end up empty rather than leaving a bucket with nothing in it.

## Suggested next actions: design work, grounded in Section 4

This section is not a grab-bag of "things someone should probably do" — it's the shortlist from "Choosing what to start with" in `derive.md`, i.e., specific tasks pulled from Section 4's own breakdown, in the order a designer would actually pick them up. Each one names the task, restates its day estimate, and gives the one-line reason it's near the top of the list:

```
- Start the content audit (2–3 days, Content Designs and Plan) — no dependencies,
  and its findings feed the content model and the migration plan right behind it.
- Run the outcomes workshop in parallel — the fastest way to turn "measure more
  activity" (Section 1) into something concrete enough to design against.
```

Logistics items — confirming a tool, scheduling an alignment session, chasing an access request — belong here only when they aren't already sitting in the gap register with an owner attached; don't duplicate an entry, and don't let logistics outnumber or precede the actual design-task callouts. If everything closeable is already in the gap register, this section can legitimately be design tasks only.

## Prose and lists

Neither format should carry the whole document. A plan written entirely in paragraphs buries the things a designer needs to scan — the roster, the deliverable list, the constraint checklist. A plan written entirely in bullets flattens the reasoning that makes the plan worth reading over the raw source docs — why a gap matters, how a milestone was inferred, what a conflict resolution overrode. Use both, and switch deliberately rather than picking one for the whole document:

- **Reach for a list** when you're naming several genuinely parallel items with little connecting tissue between them: the delivery team roster, a deliverable checklist, supported browsers, out-of-scope items, next actions. A list of 3–7 short items is easier to scan than the same items stitched into one run-on sentence.
- **Reach for prose** when the value is in the connective reasoning, not the items themselves: why the design problem is what it is, how a milestone was inferred from a contract clause, what a stakeholder's frustration implies about priorities. Collapsing that into bullet fragments strips out the "because," which is usually the point.
- **Reach for a table** only when you have several items that share the same 2–4 attributes and a reader will want to compare across rows — the gap register is the clearest example. Don't reach for a table just because a list has gotten long.

In practice, most sections read best as a short paragraph of framing followed by a list where one is genuinely warranted, occasionally closed out with a sentence that draws the conclusion — paragraph, list, paragraph, not list-only or prose-only. A section that's naturally just two or three sentences doesn't need to manufacture a list to look structured; a section that's naturally a roster or a checklist doesn't need to be dressed up in false narrative. Let the content pick the shape, and vary it enough across the document that no two consecutive sections look identical.

## Length

Length follows the source, and it should be the minimum that does the job. A thin one-page brief supports maybe 400–700 words plus a gap register — no throat-clearing, no restating the obvious, sections that have little to say stay short rather than getting padded to match the others. A full SOW plus a planning tracker can support two to three thousand words, but only because there's genuinely that much load-bearing content to report — length earned by substance, not assumed by document size. The Section 4 task breakdown and Section 7 timeline are the two places real length is expected even in a thin plan, since they're doing the most concrete work for the designer. Padding a thin source to look thorough is the failure mode to avoid elsewhere; so is over-explaining a section just because the template gives it a heading. A short plan with an honest gap register is a more useful artifact than a long one full of hedged filler.
