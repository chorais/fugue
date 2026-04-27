# **Methodology Overview (v2.4)**  
Version: 2.4  
Status: Active (Frozen)  
Methodology: Fugue Orchestration Method  
Governance Authority: Curator  

---

# 1. Overview

The **Fugue Orchestration Method** is a governance‑first, persona‑driven methodology for building **deterministic, auditable, and reproducible AI‑assisted software systems**.

It defines:

- the **governance hierarchy** (Project → Branch → Theme → Tranche → Ticket)  
- the **personas** that govern and execute work  
- the **lifecycle phases** that structure execution  
- the **envelopes** that enforce correctness  
- the **contracts** that define behaviour  
- the **templates** and **schemas** that structure artefacts  
- the **test suite** and **test engine** that validate determinism  
- the **DECOR** that anchors architectural intent  

Fugue ensures that:

- execution is deterministic  
- governance is enforced  
- identity and namespace propagation are correct  
- documentation is complete  
- replay is reproducible  
- evaluator behaviour is validated  
- drift is detected, classified, and reconciled  

---

# 2. Governance Hierarchy (v2.4)

Fugue defines a **five‑level governance hierarchy**:

```
Project
  → Branch
      → Theme
          → Tranche
              → Ticket
```

## 2.1 Project (P<id>)  
The highest‑level governance container.  
Defines mission, architectural domain, governance envelope, naming + namespace roots, and identity propagation root.

**Conceptually:**  
A Project contains many Themes.

**Structurally:**  
A Project contains Branches, which realise Themes.

---

## 2.2 Branch (B<id>)  
An execution lane inside a Project.  
Branches define:

- execution direction  
- governance envelope subset  
- naming + namespace subset  
- identity propagation root  
- persona routing subset  

A Branch **realises Themes**.  
A Theme may span multiple Branches over the life of a Project.

---

## 2.3 Theme (T<id>)  
A conceptual grouping of related work.  
Themes represent architectural narratives and problem‑space groupings.

**Conceptually:**  
A Project contains many Themes.

**Structurally:**  
Themes live inside Branches and contain Tranches.

---

## 2.4 Tranche (C<id>)  
The atomic **lifecycle unit** in Fugue.  
A tranche executes the full 6‑phase lifecycle and contains multiple Tickets.  
Contains:

- tranche preamble  
- DECOR  
- Ticket Map  
- ticket loop  
- reconciliation  
- verification  
- closure artefacts  

Tranches are the only units that execute the lifecycle.

## 2.5 Ticket (tk<id>)
The atomic **execution unit** in Fugue.
Assigned to Implementers or Architects via the Ticket Map.
Contains:
- ticket specification
- acceptance criteria
- test requirements
- DECOR references
Tickets produce implementation outputs (code, tests, logs, traces).

## Important Distinction: Tranche vs. Ticket

Fugue distinguishes between **lifecycle units** and **execution units**:

- **Tranche = Atomic Lifecycle Unit**
  - Executes the complete 6‑phase lifecycle
  - Produces DECOR, Ticket Map, reconciliation, closure
  - Managed by the Orchestrator

- **Ticket = Atomic Execution Unit**
  - Executes a single piece of work
  - Produces code, tests, logs, traces
  - Assigned to Implementers or Architects

A single tranche may contain many tickets.

---

# 3. Persona Model (v2.4)

Fugue defines **two persona layers**, each with strict boundaries.

---

## 3.1 Conceptual Personas  
These govern the methodology itself:

- **Curator** — governance authority, tranche approval, closure  
- **Conductor** — lifecycle orchestration, persona routing, metadata enforcement  
- **Architect** — DECOR formalisation, invariants, constraints, structural reasoning  
- **Methodologist** — evolves the methodology (meta‑layer)  

Conceptual personas define the **governance and reasoning authority** of the method.

---

## 3.2 Practical Personas  
These execute the method inside a project:

- **Initiator** — starts a tranche and establishes intent  
- **Orchestrator** — manages the ticket loop and persona routing  
- **Implementer** — performs implementation work  
- **Auditor** — validates governance, metadata, drift, and envelopes  
- **Verifier** — performs final validation before closure  

Practical personas define the **operational execution** of the method.

Personas MUST NOT cross boundaries.

---

# 4. Lifecycle (v2.4)

Fugue defines a **six‑phase deterministic lifecycle**:

---

## **Phase 1 — Bootstrap**  
- Curator establishes tranche intent  
- Initiator produces the tranche preamble  
- Conductor validates metadata and namespace setup  

---

## **Phase 2 — Interpretation**  
- Architect formalises DECOR  
- DECOR schema validation  
- Naming, namespace, and identity propagation alignment  
- Ticket Map initialisation  
- **Method A/B grounding strategy selected here**  

---

## **Phase 3 — Implementation**  
- Orchestrator dispatches tickets  
- Implementer executes each ticket in isolation  
- Implementation logs and replay traces produced  
- DECOR updates triggered when contradictions appear  

---

## **Phase 4 — Reconciliation**  
- Auditor performs drift classification  
- Architect performs structural reconciliation  
- DECOR updates formalised  
- Reconciled DECOR produced  

---

## **Phase 5 — Verification**  
- Test suite execution (dark, golden, governance, replay)  
- Evaluator behaviour validation  
- Metadata, identity, and namespace validation  
- Verifier performs final validation  

---

## **Phase 6 — Closure**  
- Curator approves closure  
- Epilogue actions executed  
- Tranche archived as immutable lineage  

Lifecycle phases MUST NOT be skipped or reordered.

---

# 5. DECOR Grounding Strategies (Method A / Method B in v2.4)

Fugue v2.4 preserves **Method A** and **Method B**, but they are no longer lifecycle forks.  
They are now:

> **Optional DECOR grounding strategies selected by the Architect during Phase 2 — Interpretation.**

They do **not** alter:

- lifecycle  
- persona routing  
- governance  
- envelopes  
- templates  
- schemas  

They only influence **how DECOR is initially formalised**.

---

## 5.1 Method A — Product‑First Grounding  
Used when:

- product intent is clear  
- architectural invariants are known early  
- DECOR can be formalised with minimal ingress analysis  

In v2.4:

- Implementer ingress analysis is optional  
- Architect formalises DECOR early  
- Ticket Map is derived from DECOR  
- DECOR stabilises earlier in the lifecycle  

---

## 5.2 Method B — Technical‑First Grounding  
Used when:

- system behaviour is unknown  
- architecture must be discovered  
- ingress analysis is required  

In v2.4:

- Implementer ingress analysis is mandatory  
- Architect formalises DECOR from evidence  
- Ticket Map is derived after DECOR stabilises  
- DECOR evolves more during Interpretation  

---

## 5.3 Canonical v2.4 Definition

> **Method A/B are DECOR grounding strategies chosen by the Architect during Interpretation.  
> They do not change the lifecycle, persona routing, or governance model.  
> They only determine how DECOR is initially formalised.**

---

# 6. DECOR (Declarative Contract of Record)

## **What DECOR Stands For**

> **DECOR = Design, Extensions, Considerations, Opportunities, Risks.  
> In Fugue v2.4, DECOR is the Declarative Contract of Record — the canonical architectural contract for a tranche.  
> It defines architectural intent, invariants, constraints, metadata, evaluator surfaces, and reconciliation surfaces, and is validated against the DECOR JSON Schema.**

### **How to use DECOR**

DECOR is the **canonical architectural contract** for a tranche.

It defines:

- architectural intent  
- invariants  
- constraints  
- metadata  
- naming and namespace rules  
- identity propagation rules  
- evaluator metadata  
- reconciliation surfaces  

DECOR MUST:

- follow the DECOR JSON Schema  
- follow naming and namespace rules  
- follow identity propagation rules  
- be formalised by the Architect  
- be reconciled before closure  

Reconciled DECOR is the **final authoritative baseline** for the tranche.

---

# 7. Envelopes

Fugue defines **five envelopes** that enforce correctness:

- **Governance Envelope**  
- **Determinism Envelope**  
- **Documentation Envelope**  
- **Identity Propagation Contract**  
- **Namespace Scheme Contract**  

Envelopes enforce:

- persona boundaries  
- lifecycle boundaries  
- determinism  
- documentation completeness  
- identity lineage  
- namespace invariants  
- evaluator metadata alignment  

Envelopes MUST NOT be bypassed.

---

# 8. Templates & Schemas

Fugue provides deterministic templates for:

- Projects  
- Branches  
- Themes  
- Tranches  
- DECOR  
- reconciled DECOR  
- tickets  
- ticket maps  
- implementation logs  
- reconciliation logs  
- epilogue actions  
- test templates  
- drift surfaces  
- test run logs  

Templates MUST NOT be modified.

Schemas validate:

- DECOR structure  
- metadata correctness  
- drift surfaces  
- test results  

Schemas MUST be applied during reconciliation and verification.

---

# 9. Ticket Loop (v2.4)

The ticket loop is governed by the Orchestrator and consists of:

1. Ticket dispatch  
2. Isolated Implementer execution  
3. Implementation logs and replay traces  
4. DECOR update triggers  
5. Ticket Map evolution  
6. Governance validation  

The loop is deterministic and persona‑isolated.

---

# 10. Reconciliation & Drift

Drift is classified as:

- **Minor**  
- **Major**  
- **Critical**  

Reconciliation includes:

- drift classification  
- structural correction  
- DECOR updates  
- reconciled DECOR publication  
- tranche closure preparation  

Critical drift MUST block closure.

---

# 11. Governed Artefacts

Each tranche produces:

- tranche preamble  
- DECOR  
- DECOR updates  
- Ticket Map  
- implementation logs  
- replay traces  
- drift surfaces  
- reconciliation logs  
- Reconciled DECOR  
- epilogue actions  
- tranche closure report  

All artefacts MUST be stored under:

```
/fugue_docs/
```

All artefacts MUST be preserved for audit.

---

# 12. Methodology Invariants

The following MUST always hold:

- DECOR is the single semantic anchor  
- DECOR may only be formalised by the Architect  
- Implementer conversations are isolated per ticket  
- naming, namespace, and identity propagation rules MUST be preserved  
- DECOR updates occur only in Interpretation or Reconciliation  
- Reconciled DECOR is the final tranche baseline  
- all governed artefacts MUST be preserved  
- lifecycle phases MUST NOT be skipped  

These invariants ensure deterministic, auditable orchestration.

---
