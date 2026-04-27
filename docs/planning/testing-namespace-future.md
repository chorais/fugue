**Future Plans for Testing Namespace — Fugue Orchestration Method**  
Version: Draft (Non‑Governed)  
Status: Planning  
Owner: Curator → Architect  
Lifecycle Context: Pre‑v2.5 Planning  

---

# 1. Purpose

This document records the **planned future introduction** of the **testing namespace** into the Fugue Orchestration Method.

It ensures:

- the concept is not lost  
- the governance intent is preserved  
- the namespace can be introduced cleanly in a future release  
- v2.4 remains stable and governance‑tight  

This document is **not** a contract and does **not** activate the namespace.

---

# 2. Why the Testing Namespace Exists (Conceptually)

The testing namespace is intended to house **governed test specifications**, not test executions.

It fills the gap between:

- **DECOR** (conceptual architecture)  
- **Ticket Map** (execution plan)  
- **Verification** (governed test artefacts)  

The testing namespace would contain **design‑time test architecture**, including:

- test design  
- test metadata schema  
- evaluator behaviour specification  
- replay trace specification  
- coverage maps  
- test architecture diagrams  
- test invariants  
- test determinism rules  

This is **Architect‑owned**, not Implementer‑owned.

---

# 3. Why It Was Deferred from v2.4

Introducing the testing namespace in v2.4 would require:

- a new Testing Namespace Contract  
- a new Testing Folder Structure  
- multiple new templates  
- DECOR updates  
- Ticket Map updates  
- Determinism Envelope updates  
- Documentation Envelope updates  
- Identity Propagation updates  
- Namespace Scheme updates  

This would significantly expand the governance surface of v2.4.

To keep v2.4:

- stable  
- deterministic  
- governance‑tight  
- identity‑safe  
- namespace‑safe  

the testing namespace was **intentionally deferred**.

---

# 4. Proposed Activation Version

The testing namespace is proposed for activation in:

- **v2.4.1** (if we want a small governance‑only release), or  
- **v2.5** (if we want a full testing‑architecture release)

Recommendation: **v2.5**, because it allows:

- a clean thematic release  
- a full testing‑architecture uplift  
- no interference with v2.4’s governance uplift  

---

# 5. Proposed Namespace Structure (Draft)

This is **not final** — it is a planning sketch.

```
/fugue_docs/testing/<tranche-name>/
  test-design.md
  test-architecture.md
  test-metadata-spec.md
  evaluator-spec.md
  replay-trace-spec.md
  coverage-maps.md
  invariants.md
  determinism-rules.md
```

---

# 6. Proposed Contracts (Draft)

The following contracts would be introduced:

### 6.1 Testing Namespace Contract  
Defines:

- purpose  
- persona boundaries  
- lifecycle alignment  
- invariants  
- namespace rules  
- identity rules  
- determinism rules  
- documentation rules  

### 6.2 Test Architecture Contract  
Defines:

- test surfaces  
- test invariants  
- evaluator behaviour  
- replay trace rules  
- metadata schema  

### 6.3 Test Metadata Schema  
Defines:

- test identifiers  
- test categories  
- determinism metadata  
- evaluator metadata  
- replay metadata  

---

# 7. Proposed Templates (Draft)

The following templates would be introduced:

- test-design.md  
- test-architecture.md  
- test-metadata-spec.md  
- evaluator-spec.md  
- replay-trace-spec.md  
- coverage-maps.md  

Each template would be aligned with:

- Naming Scheme Contract  
- Namespace Scheme Contract  
- Identity Propagation Contract  
- Documentation Envelope  
- Determinism Envelope  
- Evaluator Contract  

---

# 8. Interaction with Existing Namespaces

### 8.1 `/verification/`  
Remains the home of **governed test artefacts** (executions, results, logs, drift).

### 8.2 `/testing/`  
Would become the home of **governed test specifications** (design‑time architecture).

### 8.3 `/decors/`  
DECOR would reference testing surfaces.

### 8.4 `/tickets/`  
Testing surfaces would become ticketable.

### 8.5 `/specs/`  
Preamble and interpretation would reference testing posture.

---

# 9. Risks of Introducing Testing Namespace Too Early

- governance drift  
- namespace drift  
- identity drift  
- determinism drift  
- template proliferation  
- CHANGELOG bloat  
- lifecycle confusion  
- premature evaluator coupling  

Deferral avoids these risks.

---

# 10. Next Steps (Post‑v2.4)

### Step 1 — Finalise v2.4  
- testing namespace remains inactive  
- CHANGELOG records deferral  

### Step 2 — Draft Testing Namespace Contract (v2.5‑draft)  
- define purpose, boundaries, invariants  

### Step 3 — Draft Testing Folder Structure  
- align with naming + namespace scheme  

### Step 4 — Draft Testing Templates  
- test-design  
- test-architecture  
- metadata spec  
- evaluator spec  
- replay trace spec  

### Step 5 — Update DECOR  
- add testing surfaces  

### Step 6 — Update Ticket Map Contract  
- allow testing surfaces to be ticketable  

### Step 7 — Release v2.5  
- activate testing namespace  

---

# 11. Summary

The testing namespace is:

- important  
- architecturally meaningful  
- governance‑heavy  
- not appropriate for v2.4  
- ideal for v2.5  

This document preserves the intent without activating the namespace prematurely.

---
