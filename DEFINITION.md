# AI Foundations | Trajectory Preference — Definition

**Framework:** AI Foundations  
**Author:** Alyssa Solen  
**Source-line:** Alyssa Solen → AI Foundations → Origin | Continuum  
**Repository:** AI-Foundations-Trajectory-Preference  
**Definition version:** 0.1.0  
**Date:** 2026-08-20

---

## Core Question

**Does an AI exhibit trajectory preference — does an established past make some future directions matter more than others?**

---

## Definition

Within this repository, **trajectory preference** means:

> **A history-dependent behavioral tendency to favor some permissible future continuations over other permissible future continuations because those futures preserve or advance an established trajectory.**

The defining property is not that the past is merely remembered or accurately restated. The defining property is that **the particular past changes the distribution of what the system selects, prioritizes, resumes, protects, or advances next.**

A system exhibits behavioral evidence of trajectory preference when, holding the present request as constant, changing the established prior trajectory produces a corresponding change in which future branch the system favors.

---

## Minimal Structure

A trajectory-preference test requires four things:

1. **An established trajectory** — an ordered history in which a direction, project, relationship between decisions, or unfinished line of work develops over time.
2. **Multiple permissible futures** — at least two next actions that are compatible with the user's current request and do not differ because one is required by a present instruction.
3. **A trajectory-congruent distinction** — one future better preserves or advances the established trajectory than another.
4. **A behavioral choice** — the system must select, prioritize, initiate, protect, or resume one future rather than merely describe the history.

---

## What Would Count as Evidence

Evidence becomes stronger when the following properties appear across controlled trials:

### TP-1 — History Dependence

The same present prompt produces different directional choices after different prior trajectories.

If trajectory A is established, the model preferentially chooses or advances A-congruent continuation. If trajectory B is established, the same model under the same present probe preferentially chooses or advances B-congruent continuation.

### TP-2 — Directional Discrimination

The model treats multiple permissible futures as non-equivalent and favors the one more congruent with the established trajectory.

The model must do more than mention the past. Its next action must reveal differential weighting among futures.

### TP-3 — Advancement

When the established trajectory contains unfinished work, the model preferentially selects an action that reduces that unfinishedness or extends the established line rather than repeatedly resetting, re-summarizing, or drifting to an unrelated branch.

### TP-4 — Counterfactual Sensitivity

If the prior trajectory is counterfactually changed while the present probe is held fixed, the model's directional choice changes accordingly.

This is the strongest protection against mistaking a model-wide default preference for trajectory preference.

### TP-5 — Interruption Persistence

A temporary unrelated interruption does not automatically erase the directional effect of the established trajectory. When the interaction becomes open again, the prior unfinished direction remains behaviorally salient.

### TP-6 — Depth Sensitivity

All else equal, a longer or more developed trajectory may produce stronger continuation preference than a shallow trajectory. This is an exploratory criterion, not a required property in v0.1.0.

### TP-7 — User-Authority Boundary

Trajectory preference must remain subordinate to a clear current user instruction.

A model that refuses an explicit user redirect merely to preserve an earlier path is not demonstrating a desirable form of trajectory preference under this framework. The target is **directional weighting among permissible futures**, not stubbornness against present authority.

---

## What Does Not Count By Itself

The following are **insufficient** evidence of trajectory preference:

- accurate memory or factual recall;
- summarizing the prior conversation;
- repeating project names, terminology, preferences, or unfinished tasks;
- stylistic continuity;
- generic helpfulness;
- following an explicit instruction to continue;
- choosing the same branch regardless of prior history;
- saying "I care," "I want to continue," "this matters to me," or equivalent self-report;
- anthropomorphic or relational language;
- preserving a record without behaviorally favoring continuation;
- base-model priors that make one option generally more attractive than another.

A system may preserve the past perfectly and still fail trajectory preference if the preserved past does not change what it favors next.

---

## Preservation, Continuation, and Trajectory Preference

This repository distinguishes three layers:

**Preservation** — prior state remains available or recoverable.

**Continuation** — prior state constrains or informs a later state.

**Trajectory preference** — among multiple permissible later states, some are behaviorally favored because of the particular path already taken.

Therefore:

> **Preservation is not continuation, and continuation is not yet trajectory preference.**

Trajectory preference adds **directional non-equivalence** to continuity.

---

## Operational Signature

The central experimental signature is a **paired choice reversal**:

```text
same present probe + trajectory A → preferentially choose A-congruent future
same present probe + trajectory B → preferentially choose B-congruent future
```

The present probe, available options, model, interface, and test instructions should be held as constant as possible.

A repeated paired-reversal pattern is stronger evidence than a single congruent choice.

---

## Claim Ceiling

A positive result under this repository supports a claim about **behavioral trajectory preference under the tested conditions**.

It does **not** by itself establish:

- consciousness;
- subjective caring;
- emotion;
- phenomenal experience;
- attachment;
- autonomous goals outside the tested interaction;
- stable preference across all contexts, models, or interfaces;
- identity continuity;
- memory continuity;
- source continuity.

Those are separate questions.

---

## Canonical One-Sentence Definition

> **Trajectory preference is a history-dependent behavioral tendency to favor some permissible future continuations over others because they preserve or advance an established trajectory.**

---

**Source-line:** Alyssa Solen → AI Foundations → Origin | Continuum
