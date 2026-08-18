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
[A flat chronological bullet list — one milestone per bullet, name first,
then when it lands and whether it gates the next phase.]
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

## Milestones: a bullet list, chronological

Section 6 answers one question — what the client sees and signs off on, and when — so it's a flat bullet list in chronological order, one milestone per bullet. Not prose: a paragraph forces a designer to re-read the whole thing to find the one gate they're checking. And not a table either, tempting as a name-and-a-date looks: there are rarely enough milestones to earn columns, and the part that matters most is the gate clause, which is a sentence, not a cell.

Each bullet runs **bold milestone name** → when it lands → what it gates, with the status tag inline exactly as everywhere else: a superscript for Found, a bracket for Inferred, Proposed, or Missing.

Every bullet says whether it's a hard approval gate or just a checkpoint — including when the source names no approval at all. Write that absence out ("review only; no sign-off named"), because silence in this section reads as "no gate" when it usually means "nobody wrote it down," and those two lead a designer to plan very differently.

Order chronologically. A milestone with no date sits where its sequence puts it, with the missing date flagged inline — that's more useful than exiling undated items to the bottom, where their position stops telling the designer anything.

```
## 6 — Design milestones

- **Discovery outbrief** — end of week 6: research findings and content model
  presented to the client; sign-off required before Phase 2 starts.¹ (§5.1)
- **Hi-fi design review** — week 10, exact date not fixed. [Inferred — the SOW¹
  names a review window per phase but dates only Phase 1.] Review only; no
  approval gate named.
- **Final handoff** — no date in any source, and no sign-off named. [Missing —
  the agency project lead would know whether this is a contractual gate or an
  internal checkpoint.]
```

Keep the boundary with Section 7 clean: Section 6 names the client-visible checkpoints and the approval gates between phases, Section 7 places Section 4's tasks on the calendar around them. A milestone list that walks through the whole schedule is doing Section 7's job twice — name the gate and let the timeline carry the sequencing.

Keep the list flat, too — a milestone needing sub-bullets is usually two milestones, or one whose explanation belongs in the bracket. This fixed shape is deliberate and overrides the vary-the-format guidance below for Section 6, the same way Section 3's tables do.

## Timeline: placing the deliverables

Section 7 is not a restatement of the phase start/end dates already Found in Section 4 or Section 1 — it's where every task from Section 4's breakdown actually gets put on the calendar. Group by sprint or week-range, not by deliverable, since a designer reading this wants to know what's happening when.

Default to a grouped list rather than a table or a chart:

```
**Phase 1 — Discovery (6 weeks / 3 sprints)**

- Sprint 1 (Weeks 1–2): outcomes workshop, content audit, stakeholder interviews kick off
- Sprint 2 (Weeks 3–4): content model, design audit + wireframes, CMS shortlist
- Sprint 3 (Weeks 5–6): concept testing, hi-fi mockups, feature prioritization, Phase 2 work plan drafted

Estimated: 24–29 designer-days across 6 weeks with 1 designer allocated full-time
— comfortably inside the available time.
```

A simple table (Sprint | Tasks | Notes) is an acceptable substitute only when the timeline is short and every sprint's task list is genuinely brief enough not to wrap. Avoid a week-by-week Gantt-style grid, and avoid a Mermaid or similar chart block: past a handful of columns a grid wraps or truncates in most places a designer will actually open this document (Word, Notion, a plain markdown preview), and a chart block simply won't render at all unless the viewer happens to support that syntax. A list degrades gracefully everywhere; a grid or a chart doesn't.

Close each phase's grouping with the reconciliation line from `derive.md` — the day-estimate total against what that phase's timeline and staffing actually support, stated plainly whether it's comfortable, tight, or over-allocated.

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

In practice, most sections read best as a short paragraph of framing followed by a list where one is genuinely warranted, occasionally closed out with a sentence that draws the conclusion — paragraph, list, paragraph, not list-only or prose-only. A section that's naturally just two or three sentences doesn't need to manufacture a list to look structured; a section that's naturally a roster or a checklist doesn't need to be dressed up in false narrative. Let the content pick the shape, and vary it enough across the document that no two consecutive sections look identical. Sections 3 and 6 are the standing exceptions — the roster is always tables, milestones are always a chronological bullet list — so read the variation rule as applying to everything around them.

## Length

Length follows the source, and it should be the minimum that does the job. A thin one-page brief supports maybe 400–700 words plus a gap register — no throat-clearing, no restating the obvious, sections that have little to say stay short rather than getting padded to match the others. A full SOW plus a planning tracker can support two to three thousand words, but only because there's genuinely that much load-bearing content to report — length earned by substance, not assumed by document size. The Section 4 task breakdown and Section 7 timeline are the two places real length is expected even in a thin plan, since they're doing the most concrete work for the designer. Padding a thin source to look thorough is the failure mode to avoid elsewhere; so is over-explaining a section just because the template gives it a heading. A short plan with an honest gap register is a more useful artifact than a long one full of hedged filler.
