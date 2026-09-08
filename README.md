# Toni Writing Skills (bounded-me safe)

This repository contains a modular writing system encoded as Skills.sh skills.

These skills are designed to:
- Preserve authorship and agency
- Prevent drift and hallucination
- Separate thinking, structuring, drafting, and styling
- Make AI use explicit, scoped, and reversible

This is not a single writing style.
It is a **writing system with enforced phases**.

## Design Principles

- Meaning is locked before prose exists
- Style is a surface transformation, never a decision-maker
- Every skill has a narrow purpose and strict scope
- Skills must never infer intent or invent content

## How to use

Install individual skills using skills.sh:

```bash
npx skills add ./skills/explore
npx skills add ./skills/lock-context-pack
npx skills add ./skills/draft-from-pack
npx skills add ./skills/adapt-house-style
npx skills add ./skills/proofread-minimal
npx skills add ./skills/toni-ltd-voice
```

Use them explicitly via your prompts.

## Research and mapping skills

`external-landscape-mapping` is a reusable method for building and maintaining evidence-backed external technology landscapes for internal reference, without drifting into vendor ranking or procurement.

```bash
npx skills add ./skills/external-landscape-mapping
```
