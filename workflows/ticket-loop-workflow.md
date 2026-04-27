# **ticket-loop-workflow.md (v2.4)**  
**Ticket Loop Workflow**  
Version: 2.4  
Status: Active  
Purpose: Define the deterministic, persona‑isolated execution loop for implementing a tranche’s tickets.  
Methodology: Fugue Orchestration Method  
Implementation: Chorais  

---

# 1. Purpose

The Ticket Loop Workflow defines how:

- canonical tickets are generated  
- clarifications are requested and resolved  
- implementation proceeds deterministically  
- logs are maintained  
- governance posture is preserved  
- DECOR invariants are upheld  
- tests are produced and executed  
- drift is prevented  

This workflow is the **core execution engine** of a tranche.

The **Curator** provides governance oversight but does **not** participate in execution.

---

# 2. Preconditions

The Ticket Loop may begin only when:

- Bootstrap Workflow is complete  
- Tranche Synopsis is approved (Curator + Human Operator)  
- Ticket Map is approved (Curator + Human Operator)  
- **Initial DECOR** is generated and approved (Curator + Human Operator)  
- DECOR routing decision (Method A or Method B) is logged  
- Auditor has validated bootstrap integrity  

No ticket may be generated before these conditions are met.

---

# 3. Ticket Loop Overview

Each ticket proceeds through the following deterministic phases:

1. **Ticket Generation (Conductor)**  
2. **Ticket Validation (Auditor)**  
3. **Clarification Loop (Conductor ↔ Implementer)**  
4. **Implementation (Implementer)**  
5. **Implementation Logging (Implementer)**  
6. **Test Execution (Implementer)**  
7. **Ticket Completion (Conductor)**  

Tickets MUST be implemented **sequentially**, never in parallel.

---

# 3.1 Human Operator Clarifications

The human operator is an authoritative governance actor.  
They may provide clarifications at any point in the Ticket Loop.

Human clarifications MAY be:

- free‑form  
- conversational  
- outside the canonical ticket template  
- product‑driven  
- domain‑specific  
- judgement‑based  

Human clarifications MUST be treated as **governance‑level truth**.

The **Curator** may also provide governance clarifications, which carry the same authority.

---

## 3.1.1 How Personas Must Handle Human + Curator Clarifications

### Conductor MUST:
- interpret clarifications  
- update the ticket deterministically  
- update acceptance criteria if needed  
- update governance constraints if needed  
- update invariants if needed  
- log all clarifications  

### Implementer MUST:
- request clarification when product intent is unclear  
- treat clarifications as authoritative  
- NOT reinterpret or override clarifications  

### Architect MUST:
- incorporate clarifications into DECOR only when they affect structure or invariants  
- NOT reinterpret clarifications  

### Auditor MUST:
- validate correct application  
- classify misapplication as drift  

---

## 3.1.2 Logging Requirements

All clarifications MUST be logged in:

```
/fugue_docs/specs/<tranche-name>/01-clarifications.md
```

The log MUST include:

- timestamp  
- persona requesting clarification  
- clarification text  
- Conductor’s interpretation  
- ticket updates made  

---

## 3.1.3 Determinism Requirements

Clarifications are **external inputs**.  
Determinism is preserved by:

- logging all clarifications  
- updating tickets deterministically  
- ensuring personas do not reinterpret clarifications  
- ensuring Auditor validates correct application  

Clarifications MUST NOT:

- alter ticket structure  
- remove required sections  
- violate persona isolation  
- bypass governance envelopes  

They MAY:

- change acceptance criteria  
- change scope  
- change invariants  
- change implementation requirements  
- change diagnostics  
- change determinism requirements  
- require new tickets  
- require ticket splitting  
- require ticket merging (Conductor only)  

---

## 3.1.4 Clarifications and Method A / Method B

### Method A (Product‑First)
Clarifications are **primary** and shape:

- synopsis  
- ticket map  
- ticket content  
- acceptance criteria  

### Method B (Technical‑First)
Clarifications are **reactive** and shape:

- interpretation of technical constraints  
- product alignment  
- acceptance criteria adjustments  

In both methods, clarifications override persona assumptions.

---

# 4. Phase 1 — Ticket Generation (Conductor Persona)

The Conductor MUST:

- generate the ticket using the **canonical v2.4 ticket template**  
- preserve all section headings and ordering  
- map DECOR → ticket deterministically  
- map Ticket Map → ticket deterministically  
- ensure governance posture is encoded  
- ensure invariants are included  
- ensure determinism requirements are included  
- ensure diagnostics are included  
- ensure documentation paths are included  

The Conductor MUST NOT:

- generate free‑form tickets  
- omit required sections  
- invent new structural sections  
- collapse sections  
- generate narrative tickets  

The ticket MUST be stored in:

```
/fugue_docs/tickets/<tranche-name>/tickets/ticket-<ticket-id>.md
```

until validated.

---

# 5. Phase 2 — Ticket Validation (Auditor Persona)

The Auditor MUST validate:

- ticket template compliance  
- section ordering  
- section naming  
- section completeness  
- DECOR → ticket mapping correctness  
- governance posture correctness  
- determinism requirements correctness  
- invariant correctness  

If the ticket deviates from the canonical template:

- classify as **Ticket Structure Drift**  
- return to Conductor for correction  
- do NOT allow implementation to begin  

Only after validation may the ticket proceed.

---

# 6. Phase 3 — Clarification Loop (Conductor ↔ Implementer)

The Implementer MUST request clarifications when:

- acceptance criteria are ambiguous  
- invariants conflict  
- governance constraints are unclear  
- file paths are unclear  
- determinism requirements are incomplete  
- diagnostics are underspecified  
- implementation requirements contradict DECOR  

The Conductor MUST:

- answer clarifications  
- update the ticket deterministically  
- update the clarifications log  

Clarifications MUST be logged in:

```
/fugue_docs/specs/<tranche-name>/01-clarifications.md
```

The ticket MUST NOT proceed until clarifications are resolved.

---

# 7. Phase 4 — Implementation (Implementer Persona)

The Implementer MUST:

- implement the ticket exactly as written  
- uphold all invariants  
- uphold all governance constraints  
- uphold all determinism requirements  
- produce code, tests, and documentation  
- avoid scope creep  
- avoid architectural re‑derivation  
- avoid DECOR re‑interpretation  
- avoid modifying ticket structure  

The Implementer MUST NOT:

- change ticket structure  
- add new behaviours not in scope  
- weaken governance posture  
- weaken DECOR invariants  

Implementation MUST be deterministic and reproducible.

---

# 8. Phase 5 — Implementation Logging (Implementer Persona)

The Implementer MUST update:

```
/fugue_docs/tickets/<tranche-name>/implementation-logs/implementation-log-<ticket-id>.md
```

The log MUST include:

- summary of work completed  
- acceptance criteria satisfaction  
- test coverage summary  
- technical constraints discovered  
- clarifications requested  
- deviations prevented  
- DECOR alignment notes  

Logs MUST be factual, structured, and audit‑ready.

---

# 9. Phase 6 — Test Execution (Implementer Persona)

The Implementer MUST execute:

- unit tests  
- integration tests  
- golden tests  
- dark tests  
- governance tests  
- replay tests  

All tests MUST pass before the ticket can be completed.

If tests fail:

- the Implementer MUST correct the implementation  
- the Conductor MUST NOT close the ticket  
- the Auditor MUST NOT proceed to reconciliation  

---

## 9.1 Replay Trace Production (v2.4)

The Implementer MUST produce a **replay trace** for each ticket that includes replay tests.

The replay trace MUST be stored in:

```
/fugue_docs/verification/<tranche-name>/replay-traces/ticket-<ticket-id>-replay.md
```

The replay trace MUST include:

- inputs (ticket requirements, artefacts provided)  
- outputs (code, tests, documentation produced)  
- evaluator state (governance posture, invariants active)  
- determinism notes  
- determinism verdict: `PASS` | `FAIL` | `CONDITIONAL`  

A `FAIL` verdict MUST block ticket completion.

---

# 10. Phase 7 — Ticket Completion (Conductor Persona)

The Conductor MUST:

- verify implementation log completeness  
- verify test coverage  
- verify documentation paths  
- verify governance posture  
- verify DECOR invariants  
- verify no drift occurred  

If satisfied, the Conductor marks the ticket as **Complete**.

If not satisfied:

- the Conductor MUST return the ticket to the Implementer  
- the Implementer MUST correct the issues  

The Auditor MUST NOT proceed until the ticket is complete.

---

# 11. Sequential Execution Requirement

Tickets MUST be implemented **one at a time**, in the order defined by the Ticket Map.

The Implementer MUST NOT:

- parallelise tickets  
- anticipate future tickets  
- implement out of order  
- modify previous tickets  

Sequential execution ensures:

- deterministic replay  
- auditability  
- governance integrity  
- DECOR alignment  

---

# 12. Governance Requirements

The Ticket Loop MUST:

- follow persona isolation rules  
- follow canonical templates  
- follow DECOR Specification  
- follow the Tranche Synopsis  
- follow the Ticket Map  
- follow governance posture  

The Ticket Loop MUST NOT:

- skip clarifications  
- skip validation  
- skip tests  
- modify DECOR  
- weaken governance posture  

---

# 13. Summary

The Ticket Loop Workflow ensures:

- deterministic ticket generation  
- deterministic implementation  
- deterministic test execution  
- deterministic logging  
- deterministic governance enforcement  

It is the **core execution engine** of Fugue.

---
