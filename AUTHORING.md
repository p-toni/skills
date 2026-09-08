# Authoring Skills

This repository is a personal library of reusable methods. The purpose of authoring a skill is not to preserve a prompt; it is to preserve **judgment, sequence, constraints, evidence discipline, and lessons learned** so a useful process can be repeated and improved.

A permanent skill has a context cost. It should earn that cost.

## When to create a skill

Create one when at least one of these is true:

- a workflow has proved useful repeatedly;
- the method contains non-obvious judgment worth preserving;
- there are recurring failure modes that should not be relearned each time;
- the task benefits from a stable sequence, decomposition, or quality gate;
- personal context materially improves how the work should be done;
- repeated use should make the process better over time.

Do **not** create a skill just because:

- a model can perform the task from a short instruction;
- a prompt happened to work once;
- the task is generic proofreading, summarization, rewriting, brainstorming, or formatting;
- a rigid workflow is being used mainly to constrain capabilities that current models can handle more flexibly;
- there is one-off project content worth remembering but no reusable method behind it.

The default should be **no new skill** until the workflow demonstrates reusable value.

## Prefer methods over compensating guardrails

Do not encode restrictions whose main purpose was to compensate for limitations of an older model generation.

Examples of suspicious patterns:

- freezing meaning before any drafting when drafting itself can improve the thinking;
- forbidding synthesis or inference categorically;
- requiring artificial stage boundaries that prevent useful iteration;
- forcing fixed output templates when structure should follow the problem;
- setting arbitrary edit percentages or stylistic quotas;
- creating a skill for an operation a capable model performs reliably without one.

Hard boundaries are still appropriate when they are intrinsic to the task, such as evidence requirements, safety properties, exact transformations, or explicit user constraints.

## Shape

Each skill lives at:

```text
skills/<kebab-case-name>/SKILL.md
```

A skill may also contain local resources:

```text
skills/<name>/
  SKILL.md
  templates/
  references/
  examples/
```

Keep resources local to the skill unless multiple skills genuinely need the same source of truth.

## Frontmatter

Every `SKILL.md` should begin with at least:

```yaml
---
name: <skill-name>
description: >
  What the skill does, when it should be used, and any important boundary
  needed to distinguish it from nearby workflows.
---
```

The directory name and `name` should match.

The description is part of routing. Write it so another agent can decide correctly when the skill applies without reading the whole file.

## What a good skill contains

Not every skill needs every section, but strong skills usually make the following explicit.

### Purpose
What durable job does this skill perform?

### Trigger / when to use
What user intent or situation should cause the skill to be used?

### Boundaries / when not to use
What nearby tasks should not be pulled into this skill?

### Method
What sequence, decomposition, or iterative loop should be followed?

### Judgment
What distinctions matter that would be easy to miss from generic instructions?

### Evidence or source discipline
If the task depends on research, files, or external facts, what counts as evidence and how should uncertainty be represented?

### Failure modes
What did prior runs teach us not to do?

### Quality gates
What must be true before the output should be considered ready?

### Output contract
When useful, what artifacts or structure should the skill normally produce?

## Hard constraints vs defaults

Be deliberate about strength of language.

Use hard constraints only for behavior that would invalidate the method if violated:

- `MUST`
- `DO NOT`
- `Never`

Use defaults for choices that are generally good but context-dependent:

- `Prefer`
- `Usually`
- `By default`
- `When useful`

Too many hard constraints make a skill brittle. Too few make it drift.

## Keep the skill general; keep examples concrete

A skill should encode the method, not the first project that produced it.

If a specific project taught an important lesson, preserve the lesson and use the project as an example rather than hard-coding its entities into the workflow.

Good:

> Do not infer cross-domain continuity from multi-domain coverage alone.

Less reusable:

> Vendor A supports web and cloud, therefore check whether Vendor A pivots between them.

## Personal skills are allowed

This is a personal repository, so a skill may intentionally encode personal preferences or ways of working.

But personal skills should still be based on **current evidence** of how the user works. Do not preserve a stale voice, persona, or workflow merely because it was once useful.

If a personal style or writing skill becomes outdated and there is not enough fresh material to recalibrate it, remove it and rebuild later from recent examples rather than guessing.

## Templates and references

Add a template when repeated runs should produce a consistent artifact or when a blank structure reduces accidental omissions.

Add references when the skill depends on a stable external method or specification that should remain inspectable.

Do not add supporting files merely to make a skill look complete.

## Evolving a skill

When repeated use reveals a new lesson:

1. Identify whether the problem was routing, method, judgment, evidence, output shape, or stale assumptions.
2. Ask whether the skill still deserves to exist at all.
3. Change the smallest part that would prevent the same failure next time.
4. Preserve useful flexibility; do not encode one observed edge case as a universal rule without reason.
5. Remove obsolete constraints rather than only adding new instructions.
6. Update templates if the method changed materially.
7. Update the root README catalog if the skill's purpose changed.

Sometimes the correct evolution is deletion.

A good skill should accumulate **better judgment**, not just more instructions.

## Repository-level checklist

Before adding or materially changing a skill:

- [ ] The method is genuinely reusable.
- [ ] A short ordinary prompt would not provide equivalent value.
- [ ] The skill has one clear primary purpose.
- [ ] The frontmatter routes it accurately.
- [ ] Important boundaries are explicit.
- [ ] Reusable judgment is encoded, not only procedural steps.
- [ ] Known failure modes are represented when relevant.
- [ ] Hard constraints are reserved for truly non-negotiable behavior.
- [ ] The skill does not preserve obsolete model-era compensations without reason.
- [ ] Examples do not accidentally become hard-coded scope.
- [ ] Supporting files are necessary and local to the skill.
- [ ] Existing stale skills were removed or updated rather than left for compatibility.
- [ ] The root README catalog is current.
