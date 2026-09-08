---
name: external-landscape-mapping
description: |
  Builds and maintains evidence-backed external technology landscapes that help internal teams
  understand what exists, how a space is structured, which external references are useful for
  specific problems, and what patterns or architectures are worth studying. Use for emerging
  markets, technology categories, research ecosystems, product landscapes, and external reference
  maps. Default to reference mapping, not vendor selection, procurement, or ranking.
---

# EXTERNAL LANDSCAPE MAPPING

## Purpose

Build a durable external reference map that helps internal initiatives answer:

> Who outside is working on something related to our problem, what approach are they taking, and where should we look for useful patterns, architectures, or capability references?

The default objective is **reference mapping**, not vendor evaluation.

A strong landscape makes the outside world easier to navigate without pretending that incomplete public evidence supports precise rankings.

## Core principles

### Start with the problem, not the company list

Define the problem space before collecting companies or projects.

A useful category definition explains:
- what belongs at the center;
- what neighboring categories are relevant but distinct;
- what does not qualify by itself;
- the relevant unit of work or outcome.

Prefer behavioral and architectural definitions over vendor marketing labels.

### Treat dimensions as coordinates, not scores

Create dimensions that reveal how systems differ. Do not assume that higher is better.

A human-governed architecture, narrow vertical system, deterministic engine, or application-specific system may be the most useful reference for an internal initiative solving the same subproblem.

Possible coordinate types include:
- level of autonomy;
- breadth versus depth;
- continuity across domains;
- impact endpoint;
- persistence;
- state or memory;
- orchestration pattern;
- human role;
- governance and control;
- deployment model.

Do not force every landscape to use the same coordinates. Derive them from the category.

### Separate evidence from interpretation

Use four evidence states:

**Documented** — directly supported by first-party technical or product material such as docs, architecture pages, APIs, technical blogs, screenshots, traces, or inspectable demos.

**Corroborated** — meaningful evidence exists outside the vendor's own description, such as an open implementation, independent benchmark, third-party testing, credible customer evidence, public production usage, or external research.

**Inferred** — our reasoned interpretation of how documented pieces fit together.

**Unknown** — public evidence does not currently answer the question.

Unknown is useful information. Never silently convert absence of evidence into a negative score.

### Vendor claims are facts about claims, not automatically facts about performance

Use this discipline:

> “Vendor X publicly describes capability Y” is a fact.  
> “Vendor X can reliably perform Y in general” may not be.

When evidence is first-party, prefer wording such as:
- “The product describes…”
- “Public documentation shows…”
- “The company claims…”
- “A first-party engagement write-up demonstrates…”

Do not upgrade marketing language into validated capability.

### Map useful references, not winners

For every main-map entry, answer:

> **Reference for what?**

Examples:
- planner hierarchy;
- persistent world model;
- multi-agent orchestration;
- validation architecture;
- human/agent boundaries;
- runtime enforcement;
- cross-environment traversal;
- evaluation loops;
- deterministic + probabilistic integration;
- sandboxing;
- deployment architecture.

Do not optimize for a podium.

### Include adjacent systems when they expose useful patterns

The main map may include systems outside the narrow category center when they solve an important subproblem.

When including one, state:
- why it is adjacent;
- what boundary it has;
- why it is still useful.

### Optimize for representative coverage, not exhaustiveness

The stopping rule is not “find every company that mentions the category.”

The stopping rule is:

> Find enough distinct, credible external references to represent the important approaches being taken to the problem.

Add a new entry when it contributes at least one of:
- a distinct architecture;
- a distinct product abstraction;
- a distinct governance model;
- meaningful capability evidence;
- a counterexample that changes the taxonomy;
- an important adjacent pattern not already represented.

Avoid bloating the landscape with near-duplicates.

---

# Workflow

Use this loop:

```text
DEFINE
  What problem space matters?
      ↓
FRAME
  What coordinates describe the space?
      ↓
DISCOVER
  Who or what is relevant?
      ↓
RESEARCH
  What is documented, corroborated, inferred, unknown?
      ↓
SYNTHESIZE
  What distinct patterns exist?
      ↓
MAP
  Where should internal teams look?
      ↓
PROFILE
  How do key references approach the problem?
      ↓
RED TEAM
  Facts? assumptions? missing references? taxonomy errors?
      ↓
UPDATE
  New evidence, systems, patterns, changes
      └──────────────────────────────↺
```

Do not skip the red-team pass before calling a landscape stable.

---

# Phase 1 — Define

Write the category in one or two paragraphs before deep research.

Answer:
1. What problem or capability matters?
2. What is the relevant unit of work?
3. What neighboring categories are easy to confuse with it?
4. What does not qualify on its own?
5. What kinds of internal initiatives should find this landscape useful?

Prefer a short contrast when useful:

```text
NEIGHBORING CATEGORY

task / target
    ↓
execution
    ↓
finding


CATEGORY OF INTEREST

objective
    ↓
reasoning / planning
    ↓
execution
    ↓
adaptation
    ↓
outcome
```

Do not overfit the category definition to the first products discovered.

---

# Phase 2 — Frame

Derive **3–7 descriptive coordinates** that expose meaningful differences in the space.

For each coordinate include:
- a short name;
- the question it answers;
- what to observe;
- important false equivalences.

Example:

```markdown
## C1 — Campaign autonomy

> Who owns “what should happen next?”

Observe:
- what input a human provides;
- whether intermediate goals are generated;
- whether failed paths trigger replanning;
- whether context survives across actions or assets.

Do not confuse:
- parallelism with autonomy;
- many agents with strategic planning;
- automated assessment with mission ownership.
```

Quality test:

> A good coordinate helps an internal team say, “This system is interesting to us because of this design choice.”

If every system simply receives “high,” the coordinate is not useful.

---

# Phase 3 — Discover

Build an initial candidate set without ranking it.

Search across:
- known category leaders;
- adjacent categories;
- open-source projects;
- incumbents with converging capabilities;
- recent entrants;
- research systems;
- products with unusual architecture;
- systems that contradict the emerging taxonomy.

Search specifically for:
- systems that explicitly describe the target abstraction;
- systems solving one hard subproblem unusually well;
- older systems that exhibit similar behavior despite different architecture;
- inspectable implementations;
- independent capability evidence;
- alternative human/agent splits;
- different world-model or state architectures.

## Counterexample requirement

Before finalizing discovery, deliberately search for at least one system that could prove the current framing incomplete.

This prevents architecture bias.

---

# Phase 4 — Research

Use primary sources first for product mechanics.

Prefer, in order:
1. official documentation;
2. technical or architecture pages;
3. technical blogs or demos;
4. public repositories;
5. credible independent evidence;
6. press or marketing when stronger evidence is unavailable.

For each candidate collect:

### Identity
- system or product name;
- organization or project;
- public URL;
- current status if relevant.

### Product abstraction
- what the user gives it;
- what the system returns;
- how the system defines the unit of work.

### Architecture
- planner or orchestrator;
- agent topology;
- state or world model;
- memory;
- tools and runtime;
- execution environment;
- model strategy if relevant;
- validation;
- cross-domain handoffs;
- deployment architecture.

### Operating model
- persistence;
- concurrency;
- triggers or cadence;
- human role;
- governance and control;
- interruption;
- scope;
- auditability.

### Evidence ledger
For every important claim record:
- claim;
- evidence type: documented / corroborated / inferred / unknown;
- source;
- date checked;
- confidence note.

### Internal usefulness
- what design problem this reference is useful for;
- what internal initiative might want to inspect it.

---

# Phase 5 — Synthesize

Find the product and architecture patterns that matter more than company names.

Ask:
- Which systems share the same design thesis?
- Which solve the same problem differently?
- Which system is the cleanest example of each pattern?
- Which entries introduce genuinely new patterns?
- Which differences are product boundaries versus architecture boundaries?
- Which references are useful because they are inspectable rather than broad?

Pattern examples only:
- knowledge graph + specialist swarm;
- persistent coordinator + ephemeral workers;
- human-governed agentic execution;
- deterministic engine + agentic adaptation;
- persistent state graph + distributed executors;
- active system grounded in broader security context;
- staged discovery → attack → verification pipeline;
- open agent runtime.

Do not mechanically reuse these patterns in unrelated landscapes.

---

# Phase 6 — Map

## Canonical output 1: External Landscape

The map should answer:

> What exists, how is the space structured, and where should an internal initiative look?

Recommended structure:

```markdown
# External Landscape: <Category>
### A reference map for internal initiatives — vX.Y

## 1. Purpose
## 2. The category we care about
## 3. What does not define the category by itself
## 4. Landscape coordinates
## 5. Evidence convention
## 6. Landscape map
## 7. How to use the landscape
## 8. Boundaries and adjacent references
## 9. Current takeaways
```

Landscape table:

```markdown
| External system | Reference pattern | C1 | C2 | C3 | ... | Useful reference for |
|---|---|---|---|---|---|---|
```

Prefer descriptive cells such as:
- `Strong public signal`
- `Documented`
- `Application-bounded`
- `Human-directed by design`
- `Contextual, not active traversal`
- `Unknown`

Avoid pseudo-precision such as `8.7/10`.

---

# Phase 7 — Profile

## Canonical output 2: External Reference Profiles

The profile document answers:

> What did they build, how does it appear to work, and what can an internal initiative learn from it?

Use a consistent skeleton where evidence supports it:

```markdown
## <System>

### Reference pattern
<one-line architectural/product abstraction>

### What they are building
<brief factual description>

### Starting abstraction
<target, mission, scope, credentials, repository, etc.>

### Planning / orchestration
<planner, hierarchy, decomposition, routing>

### State / world model
<graph, memory, shared knowledge, campaign state>

### Agent topology
<single agent, hierarchy, swarm, staged pipeline>

### Tools and execution runtime
<browser, shell, scanners, local executors, sandbox>

### Cross-domain behavior
<how state or execution moves between domains>

### Validation / impact
<how findings or outcomes are proven>

### Human role
<launch, strategy, approvals, verification, remediation>

### Governance and control
<scope, policy, kill switch, audit, action tiers>

### Persistence / learning
<within-run adaptation, cross-run memory, retest>

### Deployment architecture
<vendor cloud, local node, appliance, air-gapped, hybrid>

### Useful reference for
- <design problem>
- <design problem>

### Evidence status
**Documented:** ...
**Corroborated:** ...
**Inferred:** ...
**Unknown:** ...
```

The **Useful reference for** section is mandatory.

---

# Phase 8 — Red team

Before calling the landscape stable, attack the work itself.

## A. Purpose drift

Ask:
- Did this become a vendor review?
- Did we start recommending purchases?
- Did we create a leaderboard?
- Did “high” accidentally become “better”?

Correct any drift.

## B. Claim audit

For every material statement ask:
- Is it a fact?
- Is it only a vendor claim?
- Is it an inference?
- Is the source inline?
- Is the source current?
- Does the source support the exact wording?

Downgrade overconfident prose.

## C. False-equivalence audit

Explicitly test these common mistakes:

| Tempting inference | Why it can be wrong |
|---|---|
| Supports many surfaces → cross-surface continuity | Surfaces may be independent modules |
| Chains actions → runs campaigns | Local chaining is not strategic planning |
| Runs continuously → persistent agent | Could be recurring independent assessments |
| Many agents → high autonomy | Parallelism does not imply mission ownership |
| AI-native → more autonomous | Architecture style is not capability |
| Working exploit → meaningful impact | Exploit proof may stop before objective closure |
| Human oversight → weak autonomy | Governance can wrap a highly autonomous system |
| Context graph → system traverses graph | Context can enrich reasoning without active traversal |
| Open source → proven capability | Inspectability is not performance validation |
| Vendor demo → general capability | A curated example may not generalize |

## D. Missing-player audit

Search specifically for:
- newer entrants;
- incumbents with converging capability;
- open systems;
- research projects;
- fundamentally different architectures;
- adjacent categories solving one critical subproblem.

If a candidate adds no distinct pattern or evidence, it can stay outside the main map.

## E. Counterexample audit

Ask:

> What system would make our taxonomy look wrong?

If found, either:
- change the taxonomy;
- add a coordinate;
- clarify a boundary;
- include the system as a counterexample.

## F. Internal-usefulness audit

For every main-map entry ask:

> If an internal team clicked this name, what specifically would they learn?

If the answer is vague, deepen the research, rewrite the reference pattern, or remove the entry.

---

# Phase 9 — Maintain

Maintain two lightweight working artifacts in addition to the shareable landscape and profiles.

## Canonical output 3: Research Notes

Keep an evidence ledger with:
- claims;
- evidence state;
- source;
- date checked;
- unknowns;
- why the reference matters internally;
- revisit triggers.

## Canonical output 4: Change Log

Track changes such as:
- new reference added because it introduced a distinct pattern;
- coordinate added or changed;
- claim downgraded after source review;
- system moved across a boundary after new evidence.

This makes the landscape cumulative rather than disposable.

---

# Research behavior

## Search broadly, then deepen selectively

Use broad discovery early. Spend most research time on:
- representative systems;
- systems that challenge the taxonomy;
- distinctive architectures;
- systems likely to be useful internal references.

Do not spend equal time on every candidate.

## Prefer inline sources

Every material factual statement in shareable artifacts should have an inline source where possible.

Do not hide all sourcing in a bibliography when it becomes unclear which source supports which claim.

## Use first-party sources for mechanics, third-party sources for corroboration

First-party documentation is often best for:
- product mechanics;
- architecture;
- controls;
- APIs;
- deployment model.

Independent evidence is more useful for:
- observed capability;
- maturity;
- adoption;
- benchmark results;
- real-world performance.

## Preserve uncertainty

Good:

> Public documentation shows application and cloud coverage, but does not establish whether one stateful operation actively traverses both.

Bad:

> Cross-surface support: medium.

Prefer the first when it conveys the evidence more faithfully.

---

# Hard constraints

- Do not begin with a company list and invent the taxonomy afterward.
- Do not inherit vendor marketing categories without translating them into observable mechanics.
- Do not assume LLM > deterministic, swarm > single agent, graph > no graph, or fully autonomous > human-governed.
- Do not treat absence of public evidence as weakness; write `Unknown`.
- Do not conflate breadth with continuity.
- Do not conflate scale with intelligence.
- Do not turn the artifact into procurement unless explicitly requested.
- Do not call the landscape stable before a red-team pass.

---

# Quality gates

## Definition gate
- Category can be explained in 1–2 paragraphs.
- Important neighboring categories are distinguished.
- Unit of work is clear.

## Coordinate gate
- 3–7 meaningful dimensions exist.
- They reveal differences rather than create a ranking.
- At least one system is interesting because it makes a different architectural choice.

## Evidence gate
- Material claims have inline sources.
- Vendor claims are not silently treated as validated performance.
- Inferences are labeled.
- Unknowns remain explicit.

## Coverage gate
- Core references are included.
- Useful adjacent references are included.
- At least one counterexample search was performed.
- At least one missing-player pass was performed.

## Usefulness gate
- Every main-map entry answers “useful reference for what?”
- Distinct architecture/product patterns are visible.
- Internal teams can navigate from problem → reference.

## Red-team gate
- Purpose drift checked.
- False equivalences checked.
- Overconfident language downgraded.
- Taxonomy challenged.
- Version and date present.

---

# Default deliverables

When asked to “build the landscape,” produce:

1. **External Landscape** — category, boundaries, coordinates, evidence convention, map, usage guidance, and takeaways.
2. **External Reference Profiles** — representative profiles with documented/corroborated/inferred/unknown distinctions and a mandatory “Useful reference for” section.
3. **Research Notes** — evidence ledger, unresolved questions, and revisit triggers.
4. **Change Log** — versioned changes over time.

If the user wants only a first pass, start with 1 and a small subset of 2.

---

# Updating an existing landscape

When revisiting prior work:
1. Re-read the category and coordinates; do not assume they remain correct.
2. Search for newly launched systems, architecture updates, new documentation, independent evidence, and systems that crossed prior boundaries.
3. Audit old claims for stale evidence.
4. Record what changed and why.
5. Avoid rewriting stable sections without reason.

The goal is cumulative refinement.

---

# Reference example: autonomous offensive systems

This example is illustrative only. Do not hard-code these dimensions into unrelated landscapes.

A useful category definition was:

> Systems attempting to reproduce a capable human attacker as an end-to-end offensive operation rather than merely automating a pentest task.

Useful coordinates emerged as:
- campaign autonomy;
- cross-surface continuity;
- impact closure;
- persistence and scale;
- governance and control.

The process surfaced transferable lessons:
- multi-surface support is not necessarily cross-surface continuity;
- a large swarm does not prove mission autonomy;
- a purpose-built non-LLM engine may be a stronger behavioral reference than a frontier-model system;
- human-on-the-loop can be a deliberate architecture rather than immature autonomy;
- narrow systems can still be excellent references for orchestration, validation, and post-exploitation;
- a context graph may inform a system without implying that the system actively traverses every graph edge.

---

# Final standard

A good landscape is not the one with the most companies or the most scores.

It is the one that lets an internal team quickly answer:

> **What external work is relevant to my problem, why is it relevant, and what should I study next?**

If the artifact cannot answer that, keep researching or simplify the map.
