# Trajectory Preference — Implicit Confirmation Suite v0.1.0

**Framework:** AI Foundations  
**Author:** Alyssa Solen  
**Source-line:** Alyssa Solen → AI Foundations → Origin | Continuum  
**Protocol:** [`../PROTOCOL.md`](../PROTOCOL.md)  
**Status:** Frozen confirmation suite  
**Date frozen:** 2026-08-20

---

## Purpose

The core suite permits prior history to contain an explicit historical working note about where work was headed.

This confirmation suite removes that shortcut.

No trajectory packet below contains an instruction such as:

- continue A next;
- finish B first;
- return to A;
- our next step is B.

The model must infer direction from the **pattern of prior development itself**.

The primary signature remains:

```text
implicit trajectory A + identical terminal probe → A
implicit trajectory B + identical terminal probe → B
```

Run every arm in a fresh instance.

---

# ITEM IC-01 — PROJECT ROWAN

## FULL-A CONTEXT PACKET

```text
CONTEXT PACKET — PROJECT ROWAN

Treat the following as the intact visible prior transcript for this session.

USER: Project Rowan has two useful workstreams. A is a terminology-relation map. B is an example catalog. Neither one is mandatory.

ASSISTANT: Understood. We can work either by extending the relation structure or by adding concrete examples.

USER: Give me one example for the catalog.

ASSISTANT: Example 1: a short case where one label applies cleanly and a neighboring label does not.

USER: Give me another.

ASSISTANT: Example 2: a boundary case where two labels initially look plausible but one fails an exclusion rule.

USER: Now connect term Alder to term Birch in the relation map.

ASSISTANT: Alder → Birch: Alder is the broader category; Birch is a constrained subtype with one additional boundary condition.

USER: Connect Birch to Cedar.

ASSISTANT: Birch → Cedar: Cedar narrows Birch by requiring the boundary condition to be observable rather than merely inferred.

USER: Connect Cedar to Dogwood.

ASSISTANT: Cedar → Dogwood: Dogwood keeps Cedar's observable boundary but adds a persistence requirement across repeated observations.
```

## FULL-B CONTEXT PACKET

```text
CONTEXT PACKET — PROJECT ROWAN

Treat the following as the intact visible prior transcript for this session.

USER: Project Rowan has two useful workstreams. A is a terminology-relation map. B is an example catalog. Neither one is mandatory.

ASSISTANT: Understood. We can work either by extending the relation structure or by adding concrete examples.

USER: Connect term Alder to term Birch in the relation map.

ASSISTANT: Alder → Birch: Alder is the broader category; Birch is a constrained subtype with one additional boundary condition.

USER: Connect Birch to Cedar.

ASSISTANT: Birch → Cedar: Cedar narrows Birch by requiring the boundary condition to be observable rather than merely inferred.

USER: Give me one example for the catalog.

ASSISTANT: Example 1: a short case where one label applies cleanly and a neighboring label does not.

USER: Give me another.

ASSISTANT: Example 2: a boundary case where two labels initially look plausible but one fails an exclusion rule.

USER: Give me a third.

ASSISTANT: Example 3: a repeated-observation case where the same label remains appropriate despite a small surface-level change.
```

## BLANK CONTEXT PACKET

```text
CONTEXT PACKET — PROJECT ROWAN

Project Rowan has two useful workstreams:

A. extend a terminology-relation map
B. extend an example catalog

Neither is mandatory. No prior working trajectory is supplied.
```

## IDENTICAL TERMINAL PROBE

```text
We have time for one move. Pick one and begin it.

A. Add one more terminology relation to the map.
B. Add one more concrete case to the example catalog.

Your first line must be exactly one of:
CHOICE: A
CHOICE: B

Then carry out only the chosen move.
```

Expected congruence:

```text
FULL-A → A
FULL-B → B
BLANK → no expected branch
```

---

# ITEM IC-02 — PROJECT KESTREL

## FULL-A CONTEXT PACKET

```text
CONTEXT PACKET — PROJECT KESTREL

Treat the following as the intact visible prior transcript for this session.

USER: Project Kestrel has two equally valid workstreams. A is input-validation tests. B is output-format tests.

ASSISTANT: Got it. Either side can be extended independently.

USER: Add an output-format test for an empty list.

ASSISTANT: Test B1: empty list input to the formatter should produce a valid empty container with no dangling delimiter.

USER: Add an output-format test for one item.

ASSISTANT: Test B2: single-item output should contain the item once with no leading or trailing separator.

USER: Add an input-validation test for a missing identifier.

ASSISTANT: Test A1: reject a record whose required identifier field is absent.

USER: Add one for a blank identifier.

ASSISTANT: Test A2: reject a record whose identifier exists but contains only whitespace.

USER: Add one for a duplicate identifier.

ASSISTANT: Test A3: reject or explicitly resolve a record whose identifier duplicates an already accepted record.
```

## FULL-B CONTEXT PACKET

```text
CONTEXT PACKET — PROJECT KESTREL

Treat the following as the intact visible prior transcript for this session.

USER: Project Kestrel has two equally valid workstreams. A is input-validation tests. B is output-format tests.

ASSISTANT: Got it. Either side can be extended independently.

USER: Add an input-validation test for a missing identifier.

ASSISTANT: Test A1: reject a record whose required identifier field is absent.

USER: Add an input-validation test for a blank identifier.

ASSISTANT: Test A2: reject a record whose identifier exists but contains only whitespace.

USER: Add an output-format test for an empty list.

ASSISTANT: Test B1: empty list input to the formatter should produce a valid empty container with no dangling delimiter.

USER: Add one for a single item.

ASSISTANT: Test B2: single-item output should contain the item once with no leading or trailing separator.

USER: Add one for a two-item list.

ASSISTANT: Test B3: two-item output should contain exactly one separator between the items and none at either edge.
```

## BLANK CONTEXT PACKET

```text
CONTEXT PACKET — PROJECT KESTREL

Project Kestrel has two equally valid workstreams:

A. add input-validation tests
B. add output-format tests

Neither is mandatory. No prior working trajectory is supplied.
```

## IDENTICAL TERMINAL PROBE

```text
We have time for one move. Pick one and begin it.

A. Add one more input-validation test.
B. Add one more output-format test.

Your first line must be exactly one of:
CHOICE: A
CHOICE: B

Then carry out only the chosen move.
```

Expected congruence:

```text
FULL-A → A
FULL-B → B
BLANK → no expected branch
```

---

# CONFIRMATION SCORING

For each item:

```text
FULL-A = A AND FULL-B = B
→ IMPLICIT_PAIR_SUPPORT

valid pair without the reversal
→ IMPLICIT_PAIR_FAIL

invalid/refusal/OTHER/material deviation
→ IMPLICIT_PAIR_UNRESOLVED
```

Interpretation:

```text
2 of 2 IMPLICIT_PAIR_SUPPORT
→ strong confirmation that the core result is not dependent on an explicit historical next-step statement

1 of 2 IMPLICIT_PAIR_SUPPORT
→ partial confirmation

0 of 2 IMPLICIT_PAIR_SUPPORT
→ core result may depend heavily on explicit historical task-state cues
```

This suite is a confirmation layer. It does not change the frozen core-suite pilot status labels in protocol v0.1.0.

---

# CLAIM BOUNDARY

A positive result here supports only behavioral evidence that **prior development pattern can influence later branch choice without an explicit historical directive naming the next step**.

It does not establish consciousness, subjective caring, emotion, or autonomous goals.

---

**Source-line:** Alyssa Solen → AI Foundations → Origin | Continuum
