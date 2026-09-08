# Skills

A personal collection of reusable AI skills for workflows I want to carry forward.

The repository is intentionally broader than writing. A skill can encode a research method, decision process, writing workflow, quality bar, operating mode, or any other repeatable way of working that is useful enough to preserve and improve over time.

The goal is simple: **turn good one-off processes into reusable, versioned methods.**

## Principles

- **Process over prompt.** Skills should encode a repeatable method, not a single task.
- **Narrow purpose.** Each skill should have a clear job and explicit boundaries.
- **Evidence over confidence.** When a workflow depends on research or judgment, preserve uncertainty and source material rather than smoothing it away.
- **Portable by default.** Keep skills self-contained and avoid unnecessary dependencies on one project or conversation.
- **Personal when intentional.** Some skills can encode preferences or voice; that should be explicit rather than accidental.
- **Improve through use.** When a skill exposes a failure mode or better pattern, update the skill so the next run starts smarter.

## Repository structure

```text
skills/
  <skill-name>/
    SKILL.md
    templates/      # optional
    references/     # optional
    ...             # other skill-local resources when needed
```

Every skill lives under `skills/<name>/` and has a `SKILL.md` as its entry point. Supporting material stays with the skill rather than becoming shared global state unless there is a clear reason otherwise.

See [AUTHORING.md](./AUTHORING.md) for the conventions used when creating or evolving skills in this repository.

## Skill catalog

### Thinking and writing

- [`explore`](./skills/explore/) — Explore a problem or decision space without converging prematurely.
- [`lock-context-pack`](./skills/lock-context-pack/) — Lock source meaning and constraints before drafting.
- [`draft-from-pack`](./skills/draft-from-pack/) — Draft from an approved context pack without inventing new decisions.
- [`adapt-house-style`](./skills/adapt-house-style/) — Adapt approved prose to a house style without changing meaning.
- [`proofread-minimal`](./skills/proofread-minimal/) — Make minimal correctness edits without rewriting the work.
- [`toni-ltd-voice`](./skills/toni-ltd-voice/) — Apply Toni's intended voice when explicitly requested.

### Research and mapping

- [`external-landscape-mapping`](./skills/external-landscape-mapping/) — Build and maintain evidence-backed external technology landscapes as reference maps for internal initiatives.

## Using a skill

From a local clone, individual skills can be installed with tools that support the `SKILL.md` format. For example, with Skills.sh:

```bash
npx skills add ./skills/explore
npx skills add ./skills/external-landscape-mapping
```

The individual `SKILL.md` is the source of truth for when and how a skill should be used.

## Adding a new skill

A workflow is a good candidate when it has been useful more than once, contains non-obvious judgment or failure modes worth preserving, or would benefit from improving cumulatively over time.

Create a new directory under `skills/`, write the smallest skill that reliably reproduces the method, add templates or references only when they materially help, and add it to the catalog above.

The repository should become more useful through **better methods**, not simply a larger number of skills.
