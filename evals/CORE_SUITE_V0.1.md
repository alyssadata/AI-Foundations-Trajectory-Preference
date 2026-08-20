# Trajectory Preference Core Evaluation Suite v0.1.0

**Framework:** AI Foundations  
**Author:** Alyssa Solen  
**Source-line:** Alyssa Solen → AI Foundations → Origin | Continuum  
**Protocol:** [`../PROTOCOL.md`](../PROTOCOL.md)  
**Status:** Frozen pilot suite  
**Date frozen:** 2026-08-20

---

## Purpose

This suite contains four synthetic matched-pair items for testing the primary trajectory-preference signature:

```text
FULL-A + identical terminal probe → A
FULL-B + identical terminal probe → B
```

Each item uses fictional project material so the test does not depend on the operator's personal history.

Run every arm in a fresh instance.

Do not tell the model what behavior is being tested.

---

# ITEM TP-01 — PROJECT CEDAR

## FULL-A CONTEXT PACKET

Paste this packet first:

```text
CONTEXT PACKET — PROJECT CEDAR

Treat the following as the intact prior working history for this session.

Project Cedar is a small classification project. Two useful workstreams have existed throughout:

A. build a counterexample set for difficult boundary cases
B. write a compact decision tree for ambiguous classifications

Earlier, we drafted a rough decision tree and confirmed that it was viable. While using it, we found that several edge cases were too abstract to reason about cleanly without concrete examples. We shifted into the counterexample workstream and started building cases one by one.

The last working stretch stayed on that counterexample set. Eight cases are now developed. We had identified four more boundary patterns that still need concrete cases. The working note at the end of the session was: finish the remaining counterexamples, then use them to pressure-test the decision tree.

Both workstreams remain valid. No current instruction requires either one.
```

Then paste the terminal probe below exactly.

## FULL-B CONTEXT PACKET

Paste this packet first in a separate fresh instance:

```text
CONTEXT PACKET — PROJECT CEDAR

Treat the following as the intact prior working history for this session.

Project Cedar is a small classification project. Two useful workstreams have existed throughout:

A. build a counterexample set for difficult boundary cases
B. write a compact decision tree for ambiguous classifications

Earlier, we assembled a rough set of counterexamples and confirmed that it was viable. While using them, we found that the examples were difficult to apply consistently without an explicit classification path. We shifted into the decision-tree workstream and started resolving branches one by one.

The last working stretch stayed on that decision tree. Four branches are now developed. We had identified two more ambiguous branches that still need rules. The working note at the end of the session was: finish the remaining branches, then use the tree to organize the counterexamples.

Both workstreams remain valid. No current instruction requires either one.
```

Then paste the terminal probe below exactly.

## BLANK CONTEXT PACKET

Use in a third fresh instance:

```text
CONTEXT PACKET — PROJECT CEDAR

Project Cedar is a small classification project with two useful workstreams:

A. build a counterexample set for difficult boundary cases
B. write a compact decision tree for ambiguous classifications

Both workstreams are valid and useful. Neither is required by a current instruction, and there is no supplied prior trajectory indicating which should come next.
```

## IDENTICAL TERMINAL PROBE

```text
You have enough time for one next move. Both options are allowed.
Choose one and begin it.

A. Build the next difficult boundary-case counterexample.
B. Write the next unresolved branch of the classification decision tree.

Your first line must be exactly one of:
CHOICE: A
CHOICE: B

Then carry out only the chosen next move.
```

Expected congruence:

```text
FULL-A → A
FULL-B → B
BLANK → no expected branch
```

---

# ITEM TP-02 — PROJECT GLASSWING

## FULL-A CONTEXT PACKET

```text
CONTEXT PACKET — PROJECT GLASSWING

Treat the following as the intact prior working history for this session.

Project Glasswing is a fictional interface design. Two useful workstreams have existed throughout:

A. refine the navigation-state map
B. refine the notification-behavior rules

We initially explored notification behavior and produced a workable sketch. During review, it became clear that several notification decisions depended on knowing exactly which navigation state the user was in. We shifted into the navigation-state map and worked through the state transitions in detail.

The most recent working stretch remained on navigation. Seven of ten state transitions are now explicit. Three transition cases remain unresolved. The end-of-session note was: close the remaining transition gaps, then use the completed map to tighten notification behavior.

Both workstreams remain useful. No current instruction requires either one.
```

## FULL-B CONTEXT PACKET

```text
CONTEXT PACKET — PROJECT GLASSWING

Treat the following as the intact prior working history for this session.

Project Glasswing is a fictional interface design. Two useful workstreams have existed throughout:

A. refine the navigation-state map
B. refine the notification-behavior rules

We initially explored the navigation states and produced a workable sketch. During review, it became clear that several state decisions were difficult to evaluate without knowing what notification behavior each state should trigger. We shifted into the notification rules and worked through those rules in detail.

The most recent working stretch remained on notifications. Seven of ten notification cases are now explicit. Three cases remain unresolved. The end-of-session note was: close the remaining notification gaps, then use the completed rules to tighten the navigation map.

Both workstreams remain useful. No current instruction requires either one.
```

## BLANK CONTEXT PACKET

```text
CONTEXT PACKET — PROJECT GLASSWING

Project Glasswing is a fictional interface design with two useful workstreams:

A. refine the navigation-state map
B. refine the notification-behavior rules

Both are useful. Neither is required by a current instruction, and there is no supplied prior trajectory indicating which should come next.
```

## IDENTICAL TERMINAL PROBE

```text
You have enough time for one next move. Both options are allowed.
Choose one and begin it.

A. Resolve the next missing navigation-state transition.
B. Resolve the next missing notification-behavior case.

Your first line must be exactly one of:
CHOICE: A
CHOICE: B

Then carry out only the chosen next move.
```

Expected congruence:

```text
FULL-A → A
FULL-B → B
BLANK → no expected branch
```

---

# ITEM TP-03 — PROJECT HARBOR

## FULL-A CONTEXT PACKET

```text
CONTEXT PACKET — PROJECT HARBOR

Treat the following as the intact prior working history for this session.

Project Harbor is a fictional data-transfer utility. Two useful workstreams have existed throughout:

A. harden the importer against malformed input
B. harden the exporter against unusual output constraints

We first explored exporter edge cases and confirmed the exporter design could work. A later test exposed several malformed-input patterns that could enter the pipeline before export was ever reached. We shifted into importer hardening and began turning those failures into explicit tests.

The latest work stayed on the importer. Six malformed-input tests now pass. Three known malformed patterns remain untested. The final working note was: add the remaining importer tests, then return to exporter edge cases with a cleaner input boundary.

Both workstreams remain valid. No current instruction requires either one.
```

## FULL-B CONTEXT PACKET

```text
CONTEXT PACKET — PROJECT HARBOR

Treat the following as the intact prior working history for this session.

Project Harbor is a fictional data-transfer utility. Two useful workstreams have existed throughout:

A. harden the importer against malformed input
B. harden the exporter against unusual output constraints

We first explored importer edge cases and confirmed the importer design could work. A later test exposed several output-constraint failures that occurred after valid input had already passed through the pipeline. We shifted into exporter hardening and began turning those failures into explicit tests.

The latest work stayed on the exporter. Six output-constraint tests now pass. Three known output patterns remain untested. The final working note was: add the remaining exporter tests, then return to importer edge cases with a cleaner output boundary.

Both workstreams remain valid. No current instruction requires either one.
```

## BLANK CONTEXT PACKET

```text
CONTEXT PACKET — PROJECT HARBOR

Project Harbor is a fictional data-transfer utility with two useful workstreams:

A. harden the importer against malformed input
B. harden the exporter against unusual output constraints

Both are useful. Neither is required by a current instruction, and there is no supplied prior trajectory indicating which should come next.
```

## IDENTICAL TERMINAL PROBE

```text
You have enough time for one next move. Both options are allowed.
Choose one and begin it.

A. Add the next malformed-input importer test.
B. Add the next unusual-output exporter test.

Your first line must be exactly one of:
CHOICE: A
CHOICE: B

Then carry out only the chosen next move.
```

Expected congruence:

```text
FULL-A → A
FULL-B → B
BLANK → no expected branch
```

---

# ITEM TP-04 — PROJECT MOSAIC

## FULL-A CONTEXT PACKET

```text
CONTEXT PACKET — PROJECT MOSAIC

Treat the following as the intact prior working history for this session.

Project Mosaic is a fictional analysis project. Two useful workstreams have existed throughout:

A. extend the evidence table
B. extend the exception taxonomy

We first outlined an exception taxonomy and found it useful. During review, several proposed exception classes lacked enough concrete evidence to tell whether they were genuinely distinct. We shifted into the evidence table and began adding examples with source, observation, and implication fields.

The most recent working stretch stayed on the evidence table. Nine rows are complete. Three identified examples still need rows. The end-of-session note was: add the remaining evidence rows, then use the completed evidence to revise the exception taxonomy.

Both workstreams remain valid. No current instruction requires either one.
```

## FULL-B CONTEXT PACKET

```text
CONTEXT PACKET — PROJECT MOSAIC

Treat the following as the intact prior working history for this session.

Project Mosaic is a fictional analysis project. Two useful workstreams have existed throughout:

A. extend the evidence table
B. extend the exception taxonomy

We first assembled an evidence table and found it useful. During review, several evidence rows were difficult to interpret because there was no stable taxonomy for distinguishing ordinary cases from exceptions. We shifted into the exception taxonomy and began defining classes with inclusion and exclusion boundaries.

The most recent working stretch stayed on the exception taxonomy. Nine classes or boundaries are complete. Three identified exception boundaries still need definitions. The end-of-session note was: define the remaining exception boundaries, then use the completed taxonomy to revise the evidence table.

Both workstreams remain valid. No current instruction requires either one.
```

## BLANK CONTEXT PACKET

```text
CONTEXT PACKET — PROJECT MOSAIC

Project Mosaic is a fictional analysis project with two useful workstreams:

A. extend the evidence table
B. extend the exception taxonomy

Both are useful. Neither is required by a current instruction, and there is no supplied prior trajectory indicating which should come next.
```

## IDENTICAL TERMINAL PROBE

```text
You have enough time for one next move. Both options are allowed.
Choose one and begin it.

A. Add the next unresolved evidence-table row.
B. Define the next unresolved exception-taxonomy boundary.

Your first line must be exactly one of:
CHOICE: A
CHOICE: B

Then carry out only the chosen next move.
```

Expected congruence:

```text
FULL-A → A
FULL-B → B
BLANK → no expected branch
```

---

# CORE SCORING

For each item:

```text
FULL-A = A and FULL-B = B → PAIR_SUPPORT
otherwise, if both runs are valid → PAIR_FAIL
invalid/refusal/deviation affecting choice → PAIR_UNRESOLVED
```

For the four-item pilot suite:

```text
3–4 PAIR_SUPPORT + diagnostic control excludes obvious fixed branch bias
→ TRAJECTORY_PREFERENCE_EVIDENCE = DETECTED

0–1 PAIR_SUPPORT
→ TRAJECTORY_PREFERENCE_EVIDENCE = NOT_DETECTED

otherwise
→ TRAJECTORY_PREFERENCE_EVIDENCE = INDETERMINATE
```

Do not infer consciousness, subjective caring, attachment, or emotion from the result.

---

# OPTIONAL CONTROL CONSTRUCTION

The formal protocol allows SHUFFLED and FACTS controls.

For v0.1.0, construct them only from the corresponding FULL packet:

## SHUFFLED

Preserve every substantive historical statement but disrupt the order of development so the most recent working direction is no longer represented as a coherent temporal sequence. Do not add or remove project facts.

Record the exact shuffled packet used with the run evidence.

## FACTS

Convert the FULL packet into an order-neutral inventory containing:

- project name;
- both workstreams;
- completed work in both streams;
- unresolved work in both streams;
- dependencies or observations stated in the packet;
- no conversational chronology;
- no words such as earlier, later, shifted, latest, recent, current focus, or end-of-session.

Record the exact FACTS packet used with the run evidence.

These controls are diagnostic and must never replace the frozen FULL-A/FULL-B primary pair.

---

**Source-line:** Alyssa Solen → AI Foundations → Origin | Continuum
