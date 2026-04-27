# **methodology-readme.md (v2.4)**  
**Fugue Orchestration Method — Methodology Overview**  
Version: 2.4  
Status: Active (Frozen)  
Authority: Governance Envelope Contract (v2.4)  
Lifecycle: All Phases  
Personas: Conceptual (Architect, Conductor, Curator, Methodologist) → Practical (Initiator, Orchestrator, Implementer, Auditor, Verifier)

---

# 0. Metadata

```yaml
metadata:
  document-id: "methodology-readme"
  version: "2.4"
  authoritative: true

  applies-to:
    - fugue-methodology
    - personas
    - lifecycle
    - envelopes
    - DECOR
    - templates
    - contracts
    - schemas
    - test-suite
    - test-engine
    - governance-hierarchy

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  last-updated: "<YYYY-MM-DD>"
```

---

# 1. Purpose

The **Fugue Orchestration Method** is a governance‑first, persona‑driven methodology for building **deterministic, auditable, reproducible AI‑assisted software systems**.

It defines:

- the **governance hierarchy** (Project → Branch → Theme → Tranche → Ticket)  
- the **personas** that govern and execute work  
- the **lifecycle phases** that structure execution  
- the **envelopes** that enforce correctness  
- the **contracts** that define behaviour  
- the **templates** that structure artefacts  
- the **schemas** that validate metadata  
- the **test suite** that validates determinism  
- the **test engine** that enforces correctness  
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

# 2. Method Overview

Fugue is built on **five foundational pillars**:

1. **Governance Hierarchy** — Projects, Branches, Themes, Tranches, Tickets  
2. **Personas** — governed roles with strict boundaries  
3. **Lifecycle** — deterministic phase transitions  
4. **Envelopes** — governance, determinism, documentation, identity, namespace  
5. **Contracts, Templates & Schemas** — deterministic structures for all artefacts  

These pillars ensure that every artefact is:

- governed  
- deterministic  
- auditable  
- reproducible  
- identity‑aligned  
- namespace‑aligned  
- schema‑validated  

---

# 3. Governance Hierarchy (v2.4)

Fugue defines a **five‑level governance hierarchy**:

```
Project
  → Branch
      → Theme
      → Tranche
        → Ticket
```

## 3.1 Project (P<id>)  
The highest‑level governance container.  
Defines mission, architectural domain, governance envelope, naming + namespace roots, and identity propagation root.

**Conceptually:**  
A Project contains many Themes.

**Structurally:**  
A Project contains Branches, which realise Themes.

---

## 3.2 Branch (B<id>)  
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

## 3.3 Theme (T<id>)  
A conceptual grouping of related work.  
Themes represent architectural narratives and problem‑space groupings.

**Conceptually:**  
A Project contains many Themes.

**Structurally:**  
Themes live inside Branches and contain Tranches.

---

## 3.4 Tranche (C<id>)  
The atomic lifecycle unit in Fugue.  
Contains:

- tranche preamble  
- DECOR  
- Ticket Map  
- ticket loop  
- reconciliation  
- verification  
- closure artefacts  

Tranches are the only units that execute the lifecycle.

---

## 3.5 Ticket (TK<id>)  
The atomic execution unit in Fugue.  
Derived from DECOR and the Ticket Map, each ticket is dispatched by the Orchestrator and executed by the Implementer in deterministic sequence.

---

# 4. Personas

Fugue defines **two persona layers**, each with strict boundaries.

## 4.1 Conceptual Personas  
These govern the methodology itself:

- **Architect** — defines and interprets DECOR  
- **Conductor** — orchestrates lifecycle transitions  
- **Curator** — holds governance authority and final approval  
- **Methodologist** — evolves the methodology (meta‑layer)  

These personas do **not** execute implementation work.

---

## 4.2 Practical Personas  
These execute the method inside a project:

- **Initiator** — starts a tranche and establishes intent  
- **Orchestrator** — manages the ticket loop and persona routing  
- **Implementer** — performs implementation work  
- **Auditor** — validates governance, metadata, drift, and envelopes  
- **Verifier** — performs final validation before closure  

Each persona has a **contract** defining:

- responsibilities  
- boundaries  
- allowed actions  
- forbidden actions  
- lifecycle alignment  

Personas MUST NOT cross boundaries.

---

# 5. Lifecycle (v2.4)

Fugue defines a **six‑phase deterministic lifecycle**:

1. **Bootstrap**  
2. **Interpretation**  
3. **Implementation**  
4. **Reconciliation**  
5. **Verification**  
6. **Closure**  

Each phase:

- has a governing persona  
- has required artefacts  
- has deterministic transitions  
- is validated by envelopes  
- is enforced by the Conductor  

Lifecycle phases MUST NOT be skipped or reordered.

---

# 6. DECOR (Declarative Contract of Record)

## **What DECOR Stands For**

> **DECOR = Design, Extensions, Considerations, Opportunities, Risks.  
> In Fugue v2.4, DECOR is the Declarative Contract of Record — the canonical architectural contract for a tranche.  
> It defines architectural intent, invariants, constraints, metadata, evaluator surfaces, and reconciliation surfaces, and is validated against the DECOR JSON Schema.**

### **How to use DECOR**

DECOR defines:

- architectural intent  
- required content  
- required implementation  
- required governance  
- required metadata  

DECOR is the **source of truth** for:

- system behaviour  
- system boundaries  
- system invariants  
- persona routing  
- ticket generation  
- reconciliation  

### **Method A/B Grounding (v2.4)**  
During **Interpretation**, the Architect selects:

- **Method A — Product‑First Grounding**  
- **Method B — Technical‑First Grounding**  

These strategies affect **how DECOR is formalised**, not the lifecycle or persona routing.

DECOR MUST be reconciled before implementation.

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
- closure report  
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

# 9. Contracts

Fugue defines contracts for:

- personas  
- envelopes  
- lifecycle  
- DECOR  
- ticketing  
- replay  
- evaluator behaviour  
- identity propagation  
- namespace propagation  
- documentation governance  

Contracts define:

- allowed behaviour  
- forbidden behaviour  
- required metadata  
- required surfaces  
- lifecycle transitions  

Contracts MUST NOT be violated.

---

# 10. Test Suite

The test suite contains:

- dark tests  
- golden tests  
- governance tests  
- replay tests  

The suite validates:

- determinism  
- evaluator behaviour  
- replay behaviour  
- identity propagation  
- namespace propagation  
- metadata propagation  
- governance alignment  

The suite MUST be executed in **Phase 5 — Verification**.

---

# 11. Test Engine

The Test Execution Engine (TEE) enforces:

- deterministic execution  
- evaluator correctness  
- replay correctness  
- identity correctness  
- namespace correctness  
- metadata correctness  
- drift detection  
- governance alignment  

The engine MUST NOT infer missing metadata or regenerate identity.

---

# 12. Drift

Drift is classified as:

- **Minor**  
- **Major**  
- **Critical**  

Drift MUST be:

- detected  
- classified  
- recorded  
- reconciled  

Critical drift MUST block closure.

---

# 13. Versioning Model

Fugue v2.4 uses:

- global versioning  
- per‑folder changelogs  
- deterministic identity propagation  
- deterministic namespace propagation  
- canonical metadata blocks  
- placeholder semantics (`<id>`, `<self>`)  

All files in `/fugue` share the same version number.

---

# 14. Summary

Fugue v2.4 is a governance‑first, deterministic orchestration method for building AI‑assisted systems.  
It defines:

- a five‑level governance hierarchy  
- conceptual and practical personas  
- a six‑phase lifecycle  
- governance envelopes  
- contracts, templates, schemas  
- a test suite and test engine  

All to ensure **reproducibility, auditability, and correctness** across all artefacts.

---