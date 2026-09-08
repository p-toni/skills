# Skills

A personal collection of reusable AI skills for workflows worth carrying forward.

The goal is simple: **turn good one-off processes into reusable, versioned methods that improve through use.**

This repository is intentionally small. A skill should exist only when it preserves judgment, sequence, constraints, evidence discipline, or failure modes that materially improve future work. It should not exist merely because a task can be prompted.

## Principles

- **Methods over prompts.** Encode a repeatable way of working, not a long instruction block for something modern models already do well.
- **Earn a permanent skill.** Repeated usefulness, non-obvious judgment, or recurring failure modes should justify the context cost.
- **Reasoning stays flexible.** Do not freeze early interpretations or add guardrails that prevent useful synthesis unless the workflow genuinely requires it.
- **Evidence over confidence.** Preserve facts, inference, uncertainty, and source quality when research matters.
- **Narrow purpose.** Each skill should have a clear job and explicit boundaries.
- **Portable by default.** Keep skills self-contained and avoid accidental dependence on one conversation or project.
- **Personal when useful.** This is a personal repository; a skill may encode ways of working that are specifically useful to Toni when that is intentional.
- **Improve through use.** When a run exposes a better distinction or recurring failure mode, update the method so the next run starts smarter.

## Repository structure

```text
skills/
  <skill-name>/
    SKILL.md
    templates/      # optional
    references/     # optional
    examples/       # optional
```

Every skill lives under `skills/<name>/` and has a `SKILL.md` entry point. Supporting material stays local to the skill unless there is a clear reason to share it.

See [AUTHORING.md](./AUTHORING.md) for the authoring and maintenance conventions.

## Skill catalog

### Work and thinking

- [`develop-work-doc`](./skills/develop-work-doc/) — Develop strategic, product, technical, or operating documents through iterative reasoning, drafting, evidence gathering, red teaming, and tightening.

### Research and mapping

- [`external-landscape-mapping`](./skills/external-landscape-mapping/) — Build and maintain evidence-backed external technology landscapes as reference maps for internal initiatives.

## Using a skill

From a local clone, individual skills can be installed with tools that support the `SKILL.md` format. For example, with Skills.sh:

```bash
npx skills add ./skills/develop-work-doc
npx skills add ./skills/external-landscape-mapping
```

The individual `SKILL.md` is the source of truth for when and how a skill should be used.

## Adding a new skill

A workflow is a good candidate when it has been useful repeatedly, contains non-obvious judgment worth preserving, exposes recurring failure modes, or benefits from cumulative refinement.

A workflow is usually **not** a good candidate when a capable model can already perform it reliably from a short instruction with no special method or personal context.

The repository should become more useful through **better methods**, not a larger number of skills.