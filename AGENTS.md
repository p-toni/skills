# Agent Guidance

This repository is a personal library of reusable AI skills.

When adding or changing skills here, optimize for **reusability, clarity of routing, cumulative improvement, and low context overhead** rather than prompt volume.

## Repository contract

- Put each skill under `skills/<kebab-case-name>/`.
- Every skill must have a `SKILL.md` entry point.
- Keep templates, references, examples, and other resources inside the owning skill unless there is a strong reason to share them globally.
- Keep the root `README.md` catalog current when adding, removing, renaming, or materially changing a skill.
- Read `AUTHORING.md` before creating a new skill or substantially restructuring one.

## Default bias: fewer, stronger skills

Do not create a permanent skill for something a capable current model can already do reliably from a short instruction.

A skill should preserve at least one of:

- non-obvious judgment;
- a reusable multi-step method;
- evidence/source discipline;
- recurring failure modes;
- a quality gate;
- personal context that materially improves execution;
- a process that benefits from cumulative refinement.

Skills are allowed to become obsolete. Remove them when their main value was compensating for limitations that no longer apply.

## Editing principles

- Preserve the existing purpose of a skill unless the requested change explicitly broadens or replaces it.
- Prefer the smallest change that captures a newly learned lesson.
- Encode repeatable judgment and failure modes, not conversation-specific details.
- Keep generic skills free from accidental personal/project-specific assumptions.
- Personal preferences are allowed when the skill is intentionally personal and says so clearly.
- Personal style guidance must be based on current examples; do not extrapolate a stale persona forward.
- Distinguish hard constraints from defaults; do not make every preference non-negotiable.
- Remove obsolete constraints instead of endlessly layering new ones on top.
- Do not duplicate the same rule across many skills if one local instruction is sufficient.

## New skill checklist

Before creating a skill, ask:

1. Is there a reusable method here, or only one-off content?
2. Would a short normal prompt already work well enough?
3. What exact situation should route to this skill?
4. What nearby task should *not* route to it?
5. What judgment or failure mode is worth preserving?
6. Does it need templates or references, or is `SKILL.md` enough?
7. How will repeated use make the method better?
8. What would cause us to delete or replace it later?

## Default structure

```text
skills/<name>/
  SKILL.md
  templates/      # optional
  references/     # optional
  examples/       # optional
```

Avoid adding files that do not materially improve execution, inspection, or maintenance.

## Changes to existing skills

When a run exposes a problem, classify it before editing:

- **routing** — the skill triggered when it should not, or failed to trigger when it should;
- **method** — the sequence or decomposition was wrong;
- **judgment** — an important distinction was missing;
- **evidence** — claims, sources, or uncertainty were handled poorly;
- **output** — the artifact shape was not useful;
- **scope** — the skill drifted into a neighboring job;
- **obsolescence** — model capability or the user's way of working changed enough that the skill is no longer useful.

Fix the underlying class of problem rather than adding a narrow patch for one example.

For obsolescence, deletion is a valid and often preferable fix.

## Do not

- turn the repository into a dump of long prompts;
- create a new skill for every task;
- keep obsolete skills for historical compatibility unless explicitly needed;
- hard-code entities from the first use case into a generally reusable method;
- silently broaden a skill until it overlaps several others;
- treat examples as requirements;
- freeze reasoning into rigid stages unless the task genuinely requires it;
- remove uncertainty or evidence discipline just to make outputs look cleaner.
