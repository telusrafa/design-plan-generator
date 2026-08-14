# Cowork Skills

A personal collection of custom [Claude Cowork](https://claude.ai) skills. Each skill lives in its own folder under `skills/`, with a `SKILL.md` that defines what it does and how it should behave.

## Structure

```
skills/
  design-plan-generator/
    SKILL.md
    reference/
      intake.md
      extraction.md
      conflicts-and-gaps.md
      derive.md
      writing-the-plan.md
      checklist.md
```

Each `SKILL.md` starts with a YAML frontmatter block (`name`, `description`) followed by the core instructions. Larger skills split their step-by-step detail into a `reference/` folder, with `SKILL.md` pointing to the relevant file for each step.

## Skills

### design-plan-generator

Turns project source documents (SOWs, PRDs, briefs, kickoff decks, requirement checklists, planning trackers) into a written Design Plan that gets a designer oriented on a project they've just been allocated to. Every claim in the output is tagged as Found (cited to a numbered source), Inferred, Proposed, or Missing, so nothing is silently invented.

## Adding a new skill

1. Create a new folder under `skills/<skill-name>/`.
2. Add a `SKILL.md` with frontmatter (`name`, `description`) and the full instructions.
3. Commit and push.

## Installing a skill in Cowork

Upload the skill's folder (or a zipped version of it) in Cowork, or paste the `SKILL.md` contents when creating a custom skill.
