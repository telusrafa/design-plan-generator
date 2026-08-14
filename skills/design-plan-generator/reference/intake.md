# Pass 1 detail — Intake

> Part of the `design-plan-generator` skill. See `../SKILL.md` for the full workflow overview and status vocabulary.

Read every source document fully before writing anything. Then establish five things, because they change how you interpret everything else.

## Engagement mode

Net-new work, one phase of a larger multi-phase contract, or a continuation of design work already in flight. This is the highest-leverage judgment you make. A continuation doesn't need a discovery plan — it needs an inventory of what already exists and what can't break. A single phase of a larger contract means the surrounding context is deliberately absent from your source and you should ask for prior-phase artifacts rather than treating their absence as a gap in the project.

See "Adapting to engagement mode" in `../SKILL.md` for how each mode reshapes the rest of the plan.

## Content layers

Note which parts of each document are formal scope language, informal negotiation or meeting notes, or pasted client material. Informal notes are signal, not noise — budget cycles already committed, a role not yet hired, a stakeholder who doesn't exist yet. These constraints are real and almost never make it into the polished scope section. Extract them, and label where they came from so the designer knows their status.

## Document shape

Narrative prose, structured template, tabular checklist, slide deck, or spreadsheet. Shape predicts where you'll have direct signal and where you'll be inferring heavily. A deck gives you objectives and almost no constraints; a spreadsheet gives you sequencing and almost no problem framing.

See "Adapting to document shape" in `../SKILL.md` for shape-specific tendencies.

## Direction of the document

Is this a forward-looking planning input, or a backward-looking record of work already done? A requirement-to-design coverage matrix looks like a scope document and is not one — it documents what was already built, for QA or handoff. If your only source is backward-looking, say so plainly at the top of your output, explain that it can tell the designer what exists but not what to plan, and ask for the forward-looking document.

## Conflicts between documents

With more than one source, compare them deliberately rather than noticing disagreements by accident — you can't ask about a conflict you never looked for. Sweep the facts where documents most often drift apart:

- Dates and durations
- The scope boundary
- Deliverable lists
- Who holds which role and who approves
- Staffing and budget figures

Note every discrepancy now; you'll refine the list during extraction and put it to the user in Pass 3 (see `conflicts-and-gaps.md`).

Also watch for a subtler kind: not two different values, but one document assuming something another rules out — a tracker with sprint columns for work the SOW lists as out of scope, say. Those matter more than mismatched dates and are much easier to read past.
