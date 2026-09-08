---
name: develop-work-doc
description: >
  Develop a partially formed idea, conversation, proposal, or existing draft into a
  decision-useful work artifact through iterative reasoning, drafting, evidence gathering,
  red teaming, and tightening. Use for strategic, product, technical, or operating documents
  where the thinking is still allowed to improve while the document takes shape. Do not use
  for mechanical proofreading, fixed-format transcription, or cases where the user explicitly
  wants meaning frozen before drafting.
---

# Develop Work Doc

## Purpose

Turn evolving thinking into a strong work artifact without separating “thinking” and “writing” into artificial stages.

The document is not merely a container for conclusions already reached. Drafting is part of the reasoning process: making the idea concrete should expose weak assumptions, missing structure, contradictions, and better formulations.

The default loop is:

```text
understand the intended outcome
          ↓
build the strongest current thesis
          ↓
draft enough to make it concrete
          ↕
reason against the draft
          ↓
identify gaps / assumptions / tensions
          ↓
research where external evidence matters
          ↓
red team the argument
          ↓
revise
          ↓
tighten language + structure
          ↓
stop when more polish no longer changes understanding
```

## Core principle

**Reasoning and drafting should interact.**

Do not freeze an early interpretation simply because it appeared first in the conversation. Preserve user decisions that are actually settled, but allow the argument, structure, and framing to improve as the work develops.

---

# 1. Establish the job of the document

Before optimizing prose, identify what the artifact needs to accomplish.

Resolve as much as possible from context before asking questions.

Useful questions include:

- Who needs to understand or act on this?
- What should be different after they read it?
- Is the document primarily trying to decide, align, explain, propose, pressure-test, or record?
- What is already decided versus still open?
- What constraints materially shape the answer?

Do not force every work document into a generic memo template.

The structure should follow the job.

---

# 2. Find the strongest current thesis

Identify the most load-bearing idea in the material.

Look for:

- the actual change being proposed;
- the tension or bottleneck that explains why the old model is insufficient;
- the bet that could be wrong;
- the decision the document is trying to make possible;
- the causal chain that makes the proposal coherent.

Prefer a sharp idea over a comprehensive opening.

Good section concepts often name a mechanism or change:

- `The bottleneck moves`
- `What changed for us?`
- `The unit of work is the campaign`

Weak section concepts merely label document furniture:

- `Background`
- `Key considerations`
- `Overview`
- `Discussion`

Generic headings are fine when they genuinely help navigation, but do not use them by default.

---

# 3. Draft to think

Write enough of the document to make the reasoning inspectable.

Do not wait for perfect certainty.

A draft should surface questions such as:

- Does the claim still make sense once stated precisely?
- Are two ideas being conflated?
- Does the proposed sequence actually follow?
- Is a missing assumption carrying the argument?
- Is the document solving the stated problem or an easier neighboring one?

When drafting reveals a better model, update the model.

Do not preserve earlier wording, structure, or conclusions merely to avoid “drift.”

---

# 4. Separate epistemic states

Keep these distinguishable when they matter:

### Fact
Supported by available evidence or established context.

### Inference
A conclusion drawn from facts or observations.

### Hypothesis
Something plausible that should be tested or validated.

### Proposal
A choice being recommended, not a factual claim.

### Unknown
Something the available evidence does not resolve.

Do not smooth these into the same confident voice.

When research is used, link material factual claims inline where practical.

---

# 5. Research only where it changes the work

Use external research when it can materially improve:

- correctness;
- currentness;
- the competitive/external picture;
- technical feasibility;
- evidence for a contested claim;
- discovery of counterexamples;
- confidence in an important assumption.

Do not add citations merely to make the document look researched.

Prefer primary sources for mechanics and first-party product behavior. Use independent sources for corroboration, adoption, observed performance, or contested claims.

If the evidence is incomplete, say so.

---

# 6. Red team before polishing

Before calling the document ready, attack its strongest claims.

Ask:

- What are we assuming without noticing?
- What would a knowledgeable skeptic object to?
- Are we treating a correlation as a causal explanation?
- Did we silently change the scope of the problem?
- Is there a counterexample that breaks the framing?
- Are we overgeneralizing from one example?
- Are we presenting a proposal as inevitable?
- What evidence would change our mind?
- Is there a simpler explanation?
- Did the document become more certain than the underlying evidence?

If the red-team pass changes the thesis, revise the document rather than appending defensive caveats to a weak structure.

---

# 7. Use visuals as compression

Use diagrams, tables, matrices, ladders, flows, or simple conceptual figures when they make the model easier to hold in working memory.

A visual should do conceptual work.

Good uses:

- showing a transition from current → future state;
- making a causal loop visible;
- contrasting two units of work;
- mapping dimensions or relationships;
- showing sequencing or dependency;
- compressing an architecture.

Avoid decorative visuals that repeat nearby prose.

Prefer simple forms that survive copy/paste into Markdown when possible.

---

# 8. Write close to spoken reasoning

For Toni’s work documents, prefer prose that feels like a precise version of how the idea would be explained aloud.

Defaults:

- direct rather than ceremonial;
- concrete before abstract where possible;
- short paragraphs when an idea deserves its own beat;
- clear causal transitions rather than filler transitions;
- enough context to follow the reasoning, but no generic throat-clearing;
- strong nouns and verbs over adjective stacks;
- confidence proportional to evidence.

Do not make every sentence short. Rhythm should follow the thought.

Do not imitate “executive writing” by stripping out the reasoning that makes the conclusion trustworthy.

---

# 9. Remove common AI-writing failure modes

Actively remove:

- generic opening paragraphs that restate the topic;
- repeated summaries of what was just said;
- symmetrical lists created for neatness rather than meaning;
- canned transitions such as `overall`, `in summary`, `it is important to note`;
- headings that could appear in any document;
- excessive `not X, but Y` constructions;
- abstract claims followed by an unnecessary plain-English restatement;
- confident synthesis unsupported by the evidence;
- “comprehensive” sections that do not change the decision;
- prose that sounds polished but performs no conceptual work.

The goal is not to make the document stylistically quirky. It is to remove borrowed coherence.

---

# 10. Tighten after the argument is stable

Once the document is structurally sound:

- remove repeated ideas;
- collapse sections that do the same job;
- shorten setup that no longer earns its space;
- make section titles more informative;
- move important implications closer to the claims that create them;
- preserve examples that make abstractions concrete;
- preserve necessary uncertainty;
- keep useful visuals.

Do not target an arbitrary percentage reduction.

A shorter document is better only when it preserves the reasoning required for the reader to understand and act.

---

# 11. Stop at the right point

A work document is ready when:

- its purpose is clear;
- the central thesis is legible;
- claims, proposals, and uncertainty are not conflated;
- the strongest obvious objections have been considered;
- important factual claims are supported where needed;
- the structure follows the argument rather than a template;
- a reader can identify the implication or next decision;
- another editing pass would mostly change wording rather than understanding.

Do not continue polishing solely because more polishing is possible.

---

# Modes

Adapt the workflow to the starting point.

## Conversation → document

Reconstruct the actual decisions, tensions, and unresolved questions from the conversation, then develop the artifact. Do not merely summarize chronologically.

## Rough idea → document

Help form the thesis while drafting. Make assumptions visible and test them.

## Existing draft → stronger draft

Diagnose the argument before editing prose. Preserve what works, but restructure freely when the reasoning requires it.

## Approved draft → final pass

Do not reopen settled strategic decisions without a reason. Focus on coherence, evidence, readability, visuals, and unnecessary repetition.

## Feedback → revision

Classify feedback before applying it:

- misunderstanding / clarity issue;
- missing evidence;
- disagreement with thesis;
- scope mismatch;
- structural problem;
- stylistic preference.

Fix the underlying issue rather than mechanically applying the comment.

---

# Failure modes

## Freezing too early

Do not treat the first outline or context summary as immutable truth.

## Rewriting without thinking

A cleaner draft can still contain a weak argument. Diagnose first.

## Research sprawl

Stop researching when additional sources are unlikely to change the map or the decision.

## Evidence theater

Do not add links to obvious or irrelevant claims just to increase citation density.

## Template gravity

Do not force `Executive summary → Background → Recommendation → Next steps` when another structure better expresses the reasoning.

## AI smoothness

Do not optimize for seamlessness when a visible tension, uncertainty, or unresolved boundary is important.

## Artifact velocity over absorption

Producing more documents is not the objective. The artifact should be shaped so its intended audience can actually engage with it.

---

# Output behavior

Unless the user asks otherwise:

1. Work directly toward the artifact rather than narrating every internal step.
2. Surface material uncertainties, assumptions, or red-team findings when they affect the document.
3. When iterating, provide the revised document rather than a long changelog unless the changes themselves need review.
4. Use Markdown as the default lightweight format.
5. Add visuals inline when they improve conceptual compression.

The objective is a document that makes the thinking better and makes that thinking usable.