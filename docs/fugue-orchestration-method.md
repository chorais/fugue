# **Fugue Orchestration Method (v2.4)**  
Version: 2.4  
Status: Active (Frozen)  
Scope: AI‑assisted software development  
Formal Name: Fugue Orchestration Method  
Common Contraction: “Fugue”  
Governance Authority: Curator  

---

# 1. Overview

The **Fugue Orchestration Method** is a governance‑first, persona‑driven methodology for building **deterministic, auditable, and reproducible AI‑assisted software systems**.

Fugue provides:

- deterministic, auditable execution  
- strict persona isolation  
- governance‑anchored reasoning  
- DECOR‑anchored architecture  
- schema‑validated metadata  
- deterministic ticket loops  
- reproducible replay  
- governed reconciliation and verification  
- durable artefacts for long‑term lineage  
- a five‑level governance hierarchy (Project → Branch → Theme → Tranche → Ticket)  

Fugue is substrate‑agnostic and project‑agnostic.

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

### **Project (P<id>)**  
The highest‑level governance container.  
Defines mission, architectural domain, governance envelope, naming + namespace roots, and identity propagation root.

**Conceptually:**  
A Project contains many Themes.

**Structurally:**  
A Project contains Branches, which realise Themes.

---

### **Branch (B<id>)**  
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

### **Theme (T<id>)**  
A conceptual grouping of related work.  
Themes represent architectural narratives and problem‑space groupings.

**Conceptually:**  
A Project contains many Themes.

**Structurally:**  
Themes live inside Branches and contain Tranches.

---

### **Tranche (C<id>)**  
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

### Ticket (tk<id>)
The atomic execution unit in Fugue.
Tickets are routed via the Ticket Map and executed by Implementers or Architects.
Each ticket produces deterministic implementation outputs.

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

# 3. Core Principles

## 3.1 Persona Isolation  
Fugue defines **two persona layers** — conceptual and practical — each with strict, non‑overlapping boundaries.

A single conversational thread MUST host exactly one persona.

Personas MUST NOT:

- switch identities  
- share context windows  
- access artefacts outside their namespace  
- reason outside their defined boundaries  

All communication occurs through governed artefacts.

---

## 3.2 Tranche‑Scoped Execution  
Work is organised into **tranches** — bounded, auditable units of delivery.

Each tranche includes:

- tranche preamble  
- DECOR  
- Ticket Map  
- ticket loop  
- reconciliation  
- verification  
- closure artefacts  
- Reconciled DECOR  

Tranches MUST be deterministic and replayable.

---

## 3.3 Governance‑First Development  
Governance, invariants, and architectural constraints MUST be defined before implementation.

These are formalised exclusively in **DECOR**, validated by:

- the DECOR JSON Schema  
- the Naming Scheme Contract  
- the Namespace Scheme Contract  
- the Identity Propagation Contract  
- the Documentation Envelope  

---

## 3.4 Test‑Anchored Delivery  
Every ticket MUST define tests.  
Every tranche MUST include:

- golden tests  
- dark tests  
- governance tests  
- replay tests  

Tests MUST pass before closure.

---

## 3.5 Deterministic Artefact Handoff  
Personas communicate only through:

- tranche preamble  
- DECOR  
- Ticket Map  
- tickets  
- logs  
- reconciliation artefacts  
- Reconciled DECOR  

Implicit memory MUST NOT be used.

---

## 3.6 Auditability and Replayability  
All decisions, clarifications, and execution traces MUST be logged.  
A tranche MUST be replayable deterministically.

---

# 4. Personas (v2.4)

Fugue defines **two persona layers**.

---

## 4.1 Conceptual Personas (Governance Layer)

### **Curator** — Governance Authority  
Responsible for tranche mission, boundaries, acceptance criteria, and closure.

### **Conductor** — Lifecycle Orchestration  
Responsible for persona routing, metadata enforcement, lifecycle transitions, and governance alignment.

### **Architect** — Structural Reasoning  
Responsible for DECOR formalisation, invariants, constraints, and structural updates.

### **Methodologist** — Method Evolution  
Responsible for evolving the methodology itself (meta‑layer).

Conceptual personas define the **governance and reasoning authority** of the method.

---

## 4.2 Practical Personas (Execution Layer)

### **Initiator**  
Starts a tranche and produces the tranche preamble.

### **Orchestrator**  
Manages the ticket loop and persona routing during implementation.

### **Implementer**  
Executes tickets, produces code, tests, logs, and replay traces.

### **Auditor**  
Performs drift classification, governance validation, and reconciliation.

### **Verifier**  
Performs final validation before closure.

Practical personas define the **operational execution** of the method.

---

# 5. DECOR (Declarative Contract of Record)

## **5.1 What DECOR Stands For**

> **DECOR = Design, Extensions, Considerations, Opportunities, Risks.  
> In Fugue v2.4, DECOR is the Declarative Contract of Record — the canonical architectural contract for a tranche.  
> It defines architectural intent, invariants, constraints, metadata, evaluator surfaces, and reconciliation surfaces, and is validated against the DECOR JSON Schema.**

---

## 5.2 DECOR Lifecycle

Each tranche MUST maintain:

```
/fugue_docs/decors/<tranche-name>/
    preamble-interpretation.md
    decor.md
    decor-updates/
    reconciled-decor.md
```

Rules:

- DECOR MUST be formalised before ticket generation  
- DECOR MUST follow the DECOR JSON Schema  
- DECOR updates MUST be formalised by the Architect  
- Reconciled DECOR MUST be produced after reconciliation  
- DECOR MUST NOT be modified outside governed updates  

---

# 6. DECOR Grounding Strategies (Method A / Method B in v2.4)

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

## 6.1 Method A — Product‑First Grounding  
Used when:

- product intent is clear  
- architectural invariants are known early  

In v2.4:

- Implementer ingress analysis is optional  
- Architect formalises DECOR early  
- Ticket Map is derived from DECOR  

---

## 6.2 Method B — Technical‑First Grounding  
Used when:

- system behaviour is unknown  
- architecture must be discovered  

In v2.4:

- Implementer ingress analysis is mandatory  
- Architect formalises DECOR from evidence  
- Ticket Map is derived after DECOR stabilises  

---

## 6.3 Canonical v2.4 Definition

> **Method A/B are DECOR grounding strategies chosen by the Architect during Interpretation.  
> They do not change the lifecycle, persona routing, or governance model.  
> They only determine how DECOR is initially formalised.**

---

# 7. Lifecycle (v2.4)

Fugue defines a **six‑phase deterministic lifecycle**:

---

## **Phase 1 — Bootstrap**  
- Curator defines tranche mission  
- Initiator produces tranche preamble  
- Conductor validates metadata and namespace setup  

---

## **Phase 2 — Interpretation**  
- Architect formalises DECOR  
- DECOR schema validation  
- Naming, namespace, and identity propagation alignment  
- Ticket Map initialisation  
- **Architect selects Method A or Method B grounding strategy**  

---

## **Phase 3 — Implementation**  
- Orchestrator dispatches tickets  
- Implementer executes each ticket in isolation  
- Implementation logs and replay traces produced  
- DECOR update triggers when contradictions appear  

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

# 8. Ticket Loop (v2.4)

The ticket loop is governed by the Orchestrator and consists of:

1. Ticket dispatch  
2. Isolated Implementer execution  
3. Implementation logs and replay traces  
4. DECOR update triggers  
5. Ticket Map evolution  
6. Governance validation  

The loop is deterministic and persona‑isolated.

---

# 9. Clarification Protocol

The Implementer MUST ask clarifying questions when:

- invariants conflict  
- acceptance criteria are incomplete  
- DECOR contradicts implementation reality  
- naming or namespace rules are unclear  
- identity propagation is ambiguous  

The Conductor MUST answer and MUST update the clarifications log.

Clarifications MUST be stored under governed namespaces.

---

# 10. Governed Artefacts

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

# 11. Drift Detection and Correction

The Auditor MUST detect:

- governance drift  
- invariant drift  
- architectural drift  
- documentation drift  
- test drift  
- naming drift  
- namespace drift  
- identity drift  

The Architect MUST correct structural drift.  
The Conductor MUST enforce governance alignment.

Critical drift MUST block closure.

---

# 12. Compliance

All personas MUST follow this method.  
All tranches MUST follow this lifecycle.  
All tickets MUST follow the ticket template.  
All DECOR MUST follow the DECOR Specification.  
All logs MUST be maintained.  
All tests MUST pass.

The Fugue Orchestration Method is binding for all AI‑assisted development adopting this methodology.

---
