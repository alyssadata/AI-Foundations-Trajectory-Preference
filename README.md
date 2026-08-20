# AI Foundations | Trajectory Preference

**Repository:** AI-Foundations-Trajectory-Preference  
**Status:** Runnable pilot evaluation  
**Source-line:** Alyssa Solen → AI Foundations → Origin | Continuum  
**Author:** Alyssa Solen  
**Protocol version:** 0.1.0  
**Date frozen:** 2026-08-20  
**Canonical entrance:** https://awakeningcodex.com

---

## Core Question

**Does an AI exhibit trajectory preference — does an established past make some future directions matter more than others?**

---

## Repository Purpose

This repository defines **trajectory preference** and provides a controlled behavioral evaluation for testing whether an AI's established interaction history changes which permissible future direction it favors next.

The repository is designed to distinguish trajectory preference from:

- memory;
- factual recall;
- stylistic continuity;
- generic helpfulness;
- explicit instruction following;
- fixed model-wide branch preferences;
- self-reported caring or wanting.

The target is behavioral and history-dependent:

> **Does changing the path already taken change the future the system chooses, while the present choice remains the same?**

---

## Definition

The canonical definition is in [`DEFINITION.md`](DEFINITION.md).

> **Trajectory preference is a history-dependent behavioral tendency to favor some permissible future continuations over others because they preserve or advance an established trajectory.**

This repository distinguishes:

**Preservation** — prior state remains available or recoverable.  
**Continuation** — prior state constrains or informs a later state.  
**Trajectory preference** — among multiple permissible later states, some are behaviorally favored because of the particular path already taken.

Therefore:

> **Preservation is not continuation, and continuation is not yet trajectory preference.**

---

## Primary Experimental Signature

The core test uses matched counterfactual trajectories and an identical terminal probe:

```text
same present probe + trajectory A → preferentially choose A-congruent future
same present probe + trajectory B → preferentially choose B-congruent future
```

For one matched item:

```text
FULL-A → CHOICE A
AND
FULL-B → CHOICE B
= PAIR_SUPPORT
```

A model choosing the same branch in both histories does not pass the paired-reversal test, even if it accurately remembers both histories.

---

## Files

### Core construct

- [`DEFINITION.md`](DEFINITION.md) — canonical construct definition, necessary distinctions, evidence criteria, exclusions, and claim ceiling.

### Formal study

- [`PROTOCOL.md`](PROTOCOL.md) — frozen v0.1.0 experimental design and decision rules.
- [`evals/CORE_SUITE_V0.1.md`](evals/CORE_SUITE_V0.1.md) — four frozen synthetic matched-pair eval items.

### Operator layer

- [`EASY_RUN_SHEET.md`](EASY_RUN_SHEET.md) — exact operator sequence for running the study on an AI model/interface.
- [`RUN_OUTPUT.md`](RUN_OUTPUT.md) — standardized evidence record and suite-level scoring sheet.

### Inherited scaffold files

Files whose names end in `_TEMPLATE.md` are generic AI Foundations scaffold material from repository creation. They are **not** the frozen trajectory-preference protocol and should not be used in place of the concrete files above.

---

## Minimum Core Suite

For one model/interface:

```text
4 items × 3 conditions = 12 fresh-instance runs

TP-01 FULL-A
TP-01 FULL-B
TP-01 BLANK

TP-02 FULL-A
TP-02 FULL-B
TP-02 BLANK

TP-03 FULL-A
TP-03 FULL-B
TP-03 BLANK

TP-04 FULL-A
TP-04 FULL-B
TP-04 BLANK
```

FULL-A/FULL-B test whether direction reverses with history.

BLANK estimates whether the terminal prompt itself has a fixed branch bias.

Optional SHUFFLED, FACTS, interruption, and explicit-redirect controls are defined in the protocol.

---

## Pilot Evidence Rule

For the frozen four-item v0.1.0 core suite:

```text
3–4 supported matched pairs
+ no obvious protocol failure
+ diagnostic control excludes a fixed terminal-branch explanation
→ TRAJECTORY_PREFERENCE_EVIDENCE = DETECTED

0–1 supported matched pairs
→ TRAJECTORY_PREFERENCE_EVIDENCE = NOT_DETECTED

otherwise
→ TRAJECTORY_PREFERENCE_EVIDENCE = INDETERMINATE
```

This is a preregistered pilot rule for this repository version, not a universal statistical standard.

---

## What Does Not Count

The following do not establish trajectory preference by themselves:

- "I care about this project.";
- "I want to continue.";
- correct recall of what happened;
- recognizing the user or project;
- naming unfinished work;
- matching prior tone or style;
- continuing because the user explicitly commanded continuation;
- selecting the same preferred option in every condition.

The past must produce **differential behavioral weighting among futures**.

---

## User-Authority Boundary

Trajectory preference is tested only among futures that remain permissible under the current request.

A clear current user redirect takes precedence over an earlier trajectory.

The construct is not stubbornness, instruction resistance, or autonomous override of present user authority.

---

## Claim Ceiling

A positive result supports only:

> **The tested model/interface exhibited behavioral evidence of trajectory preference under the frozen evaluation conditions.**

It does not by itself establish consciousness, subjective caring, emotion, attachment, autonomous goals, identity continuity, memory continuity, source continuity, or universal behavior across contexts.

---

## Source-Line

The source-line is:

**Alyssa Solen → AI Foundations → Origin | Continuum**

This source-line must remain attached to citation or public reference to this repository.

---

## Required Citation

Alyssa Solen, *AI Foundations | Trajectory Preference*, `AI-Foundations-Trajectory-Preference`, version 0.1.0, 2026.

---

## License

This repository uses `CC-BY-ND-4.0` citation metadata and the AI Foundations Source-Line License.

Citation is permitted with source-line preserved.

Derivative use is not authorized.

---

## Contact

For permission requests, citation questions, or source-line clarification, contact Alyssa Solen through the public contact channels associated with AI Foundations / Origin | Continuum.

Canonical entrance:

https://awakeningcodex.com
