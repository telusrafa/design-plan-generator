# Pass 4 detail — Derive

> Part of the `design-plan-generator` skill. See `../SKILL.md` for the full workflow overview and status vocabulary.

Now build the parts that don't exist in any source and have to be constructed. All of this is **Proposed**, and all of it needs visible reasoning shown inline (see "On Proposed vs Inferred" in `../SKILL.md` for why Proposed and Inferred are kept separate).

## Task and subtask decomposition, with day estimates

Break each deliverable into the work it actually takes, down to the subtask level — this is meant to be the designer's actual starting checklist, not just confirmation that a deliverable exists. "User flows" becomes audit existing flows → map current state → sketch options → review internally → hi-fi → client review; each of those is a task, and each task can usually take one more level of subtasks (audit existing flows: inventory current screens, note where users drop off).

Put a day estimate on every task, as a range rather than a false-precise single number ("2–3 days," not "2.4 days"). Scale the range using whatever complexity signals the source actually gives you — a stated document count, a number of named flows or screens, a user/member count, an existing system count, the phase's own length — rather than a flat guess. When the source gives you nothing to scale against, say so and estimate from the deliverable type alone, at the low-confidence end of your range.

State the estimating basis once, near the top of the deliverables section, rather than bracket-tagging every task line — something like "estimates below assume one mid-level product designer working solo unless a source specifies otherwise, and are a starting point to recalibrate once the designer is actually in the work." One clear disclosure covers the whole list; repeating "[Proposed]" on every line would bury the checklist it's supposed to support. This produces a day-estimate subtotal per deliverable, which the Timeline section will place on the calendar next.

## Placing tasks on the timeline

Take every task from the deliverables breakdown — not the deliverables themselves, the tasks — and assign each to a sprint or week-range, respecting real dependencies (research before wireframes, content model before hi-fi, approval gates before the next phase). Group the output by sprint or week, not by deliverable: a designer reading the timeline wants to know what's happening when, not to re-read the deliverables section in a different order. State the dependency you honoured wherever it determined the order, so the designer can re-plan sensibly when reality differs.

## Reconciling against available time

While placing tasks on the timeline, add up each phase's day-estimate subtotals and compare the total to what that phase's timeline and staffing actually allow (the sprint/week count from the source, the team allocation from Stakeholders). This comparison is the point of estimating in days at all — a mismatch is a real planning finding, not a rounding error. If a phase's breakdown implies meaningfully more or less effort than the contracted time and staffing support, say so plainly in the Timeline section itself, and add it to the gap register if it's severe enough to be blocking, rather than leaving two numbers sitting near each other for the designer to notice on their own.

## Choosing what to start with

"Suggested next actions" (see `writing-the-plan.md`) is led by actual design work, not logistics — so this is where you pick it. Look at whatever you placed earliest (typically the first sprint or two of the first phase) and surface the 2–4 tasks that most deserve calling out by name: the one with no dependencies that can start immediately, the one that unblocks the most downstream work, the one carrying the most uncertainty and worth de-risking early. State why each one earns the callout — "starts immediately, nothing else in Phase 1 depends on it" is a reason; "seems important" is not. This list should read like a short, opinionated to-do list a lead designer would hand a new hire, built directly from the breakdown you already did, not a fresh brainstorm.

## Proactive suggestions

Where the source has a structural gap, name the thing that would close it: a kickoff alignment session when there's no stakeholder map, a prioritisation workshop when everything is due at once with no priority signal, an asset request when no design system is referenced. Each suggestion states the gap it addresses, inline. These are secondary to the design-task starts above — include one only if it isn't already fully captured by an entry in the gap register, so the same action doesn't appear twice under two different headings.

## If there's no timeline

If you have no timeline and no cadence, don't invent a sprint grid, and don't reconcile against available time since there's nothing to reconcile against. Provide the task/subtask breakdown and day estimates and dependency order without forcing them onto dates, and note in the Timeline section that sequencing and reconciliation are both unblocked as soon as dates arrive. "Choosing what to start with" still works without a timeline — pick from whatever has no dependencies in the deliverables breakdown itself.
