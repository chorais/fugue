# **ticket-map-contract.md (v2.4 — Hierarchy‑Complete)**  
**Ticket Map Contract — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Authority: Governance Contract  
Scope: All Governance Layers, All Tickets, All Personas  
Lifecycle: Bootstrap → Orchestration → Implementation → Verification → Closure  

---

# 0. Metadata

```yaml
metadata:
  contract-id: "ticket-map-contract"
  version: "2.4"
  authoritative: true

  applies-to:
    - all-ticket-maps
    - all-project-ticket-maps
    - all-branch-ticket-maps
    - all-theme-ticket-maps
    - all-tranche-ticket-maps
    - all-tickets
    - all-personas
    - all-lifecycle-phases
    - all-decor-surfaces
    - all-governed-documentation
    - all-replay-traces
    - all-logs

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  governance-envelope: "<id>"
  determinism-envelope: "<id>"
  documentation-envelope: "<id>"
  identity-propagation-contract: "<id>"
  namespace-scheme-contract: "<id>"
  lifecycle-contract: "<id>"
  decor-contract: "<id>"
  ticket-template: "<id>"
```

# Placeholder Semantics
# Fields containing "<id>" or "<self>" are canonical placeholders.
# They MUST be concretised in project/branch/theme/tranche governance envelopes.
# They MUST NOT be replaced in methodology-level contracts.
# The Auditor Persona MUST treat these placeholders as intentional and NOT as metadata drift.

---

# 1. Purpose

The Ticket Map is the **authoritative, deterministic, DECOR‑aligned execution plan** for **every governance layer**:

> **Project → Branch → Theme → Tranche**

It defines:

- how work is decomposed  
- how tickets are sequenced  
- how dependencies are resolved  
- how persona routing is enforced  
- how DECOR governs ticket intent  
- how lifecycle transitions are controlled  
- how deterministic replay is guaranteed  
- how conceptual vs implementation work is separated  
- how the Architect Fill Phase is integrated  
- how metadata, identity, and namespaces propagate  
- how governance inheritance is enforced  

Ticket Maps are **governed artefacts** produced during:

- **Project Bootstrap**  
- **Branch Bootstrap**  
- **Theme Bootstrap**  
- **Conceptual Orchestration**  
- **Implementation Orchestration**  

They are the **structural spine** of the entire hierarchy.

---

# 2. Authority and Ownership (Hierarchy‑Complete)

## 2.1 Project Ticket Maps  
**Persona:** Curator → Conductor  
Defines:

- project‑level governance work  
- project‑level architectural work  
- project‑level documentation work  
- project‑level DECOR work  

Project Ticket Maps MUST:

- govern all downstream layers  
- remain stable across the project lifecycle  

---

## 2.2 Branch Ticket Maps  
**Persona:** Curator → Conductor  
Defines:

- branch‑level governance work  
- branch‑level architectural work  
- branch‑level documentation work  
- branch‑level DECOR work  

Branch Ticket Maps MUST:

- inherit from Project Ticket Maps  
- refine but NOT contradict them  

---

## 2.3 Theme Ticket Maps  
**Persona:** Curator → Conductor  
Defines:

- theme‑level governance work  
- theme‑level architectural work  
- theme‑level documentation work  
- theme‑level DECOR work  

Theme Ticket Maps MUST:

- inherit from Branch Ticket Maps  
- refine but NOT contradict them  

---

## 2.4 Tranche Ticket Maps  
**Persona:** Conductor (conceptual) → Orchestrator (implementation)  
Defines:

- tranche‑level conceptual work  
- tranche‑level implementation work  
- tranche‑level sequencing  
- tranche‑level persona routing  

Tranche Ticket Maps MUST:

- inherit from Theme Ticket Maps  
- refine but NOT contradict them  

---

# 3. DECOR Alignment Requirements

A Ticket Map MUST:

- reference DECOR at its own hierarchy level  
- inherit DECOR from all parent layers  
- propagate DECOR metadata  
- reflect Method A or Method B grounding  
- incorporate DECOR surfaces (`content-required`, `implementation-required`, `architect-required`)  
- include DECOR subsets in each ticket  
- update deterministically when DECOR updates occur  

## 3.1 DECOR Subset Extraction  
Each ticket MUST include the relevant DECOR subset from:

- Project DECOR  
- Branch DECOR  
- Theme DECOR  
- Tranche DECOR  

## 3.2 DECOR Updates  
If contradictions appear:

1. Architect formalises DECOR update  
2. Ticket Map owner updates Ticket Map  
3. Metadata MUST be preserved  
4. Identity lineage MUST be preserved  

---

# 4. Persona Routing (Hierarchy‑Complete)

Each ticket MUST declare persona routing appropriate to its layer:

### Project Layer  
- curator  
- architect  
- conductor  

### Branch Layer  
- curator  
- architect  
- conductor  

### Theme Layer  
- curator  
- architect  
- conductor  

### Tranche Layer  
- methodologist (conceptual tranches)  
- architect  
- implementer (implementation tranches)  

Hybrid routing is **forbidden**.

Persona routing MUST be:

- deterministic  
- DECOR‑aligned  
- metadata‑aligned  
- validated by the Auditor  
- preserved across Ticket Map evolution  

---

# 5. Requires‑Fill Semantics (v2.4)

Tickets MAY declare:

```
requires-fill: true
```

Meaning:

- conceptual content MUST be produced in the Architect Fill Phase  
- implementation MUST NOT begin until Fill Phase is complete  

This applies at **all hierarchy layers**.

---

# 6. Ticket Map Structure (Hierarchy‑Complete)

A Ticket Map MUST include:

- ticket identifiers  
- ticket descriptions  
- DECOR category references  
- DECOR metadata  
- dependencies  
- sequencing  
- persona routing  
- `requires-fill` metadata  
- documentation requirements  
- governance notes  
- expected artefacts  
- acceptance conditions  
- identity metadata  
- namespace metadata  
- determinism metadata  
- lifecycle metadata  
- hierarchy‑level metadata  

The Ticket Map MUST be deterministic and reproducible.

---

# 7. Naming Rules

Ticket identifiers MUST follow:

```
ticket-<hierarchy-level>-X.Y.Z.md
```

Where:

- `<hierarchy-level>` ∈ {project, branch, theme, tranche}  
- X = major version  
- Y = minor version  
- Z = ticket sequence number (1‑based)  

Epilogue tickets:

```
ticket-<hierarchy-level>-X.Y.E1.md
ticket-<hierarchy-level>-X.Y.E2.md
```

Identifiers are immutable once assigned.

---

# 8. Ordering Rules

Ordering MUST be deterministic across:

- project tickets  
- branch tickets  
- theme tickets  
- tranche tickets  

Rules:

- dependencies MUST precede dependents  
- circular dependencies are forbidden  
- cross‑layer dependencies MUST be explicit  
- governance tickets MAY be prioritised  
- ordering MUST NOT change mid‑lifecycle  

---

# 9. Dependency Rules

## 9.1 Explicit Dependencies  
Each ticket MUST declare:

- required predecessors  
- dependent tickets  

## 9.2 Deterministic Dependency Graph  
The Ticket Map MUST maintain an acyclic dependency graph across all layers.

## 9.3 Cross‑Layer Dependencies  
Allowed but MUST:

- be explicit  
- respect hierarchy  
- be validated by the Auditor  

---

# 10. Ticket Dispatch Rules

Each ticket MUST be executed in its own isolated persona conversation.

Dispatch MUST include:

- DECOR subset  
- persona routing  
- `requires-fill` metadata  
- documentation requirements  
- acceptance conditions  
- identity metadata  
- namespace metadata  
- determinism metadata  
- hierarchy metadata  

---

# 11. Ticket Map Evolution

Ticket Maps may evolve when:

- DECOR updates occur  
- new dependencies emerge  
- new risks are identified  
- clarifications are issued  
- persona routing changes  
- `requires-fill` surfaces appear  
- documentation requirements change  

All changes MUST be:

- governed  
- logged  
- deterministic  
- DECOR‑aligned  
- metadata‑preserving  
- identity‑preserving  
- namespace‑preserving  
- validated by the Auditor  

---

# 12. Validation Rules (Hierarchy‑Complete)

Validation MUST occur at:

- Project creation  
- Branch creation  
- Theme creation  
- Tranche creation  
- Audit time  
- Reconciliation time  

Validators MUST check:

- naming format  
- unique identifiers  
- acyclic dependency graph  
- DECOR grounding  
- DECOR metadata propagation  
- persona routing correctness  
- `requires-fill` correctness  
- documentation routing correctness  
- identity propagation  
- namespace correctness  
- determinism metadata  
- lifecycle metadata  
- hierarchy metadata  

---

# 13. Drift Classification

Drift occurs when:

- a ticket is added outside the Ticket Map  
- a ticket is removed without reconciliation  
- the Ticket Map is reordered mid‑lifecycle  
- dependencies are modified  
- cross‑layer dependencies are missing  
- circular dependencies appear  
- DECOR grounding is missing  
- persona routing is incorrect  
- metadata propagation is incorrect  
- identity propagation is incorrect  
- namespace placement is incorrect  
- documentation routing is incorrect  

Severity:

### **Critical**
- circular dependency  
- incorrect persona routing  
- corrupted metadata  
- corrupted identity lineage  
- corrupted namespace placement  
- cross‑layer dependency violations  

### **Major**
- reordering  
- missing transitive dependencies  
- incorrect documentation routing  

### **Minor**
- formatting issues  
- non‑blocking metadata issues  

---

# 14. Replayability

The Ticket Map MUST enable deterministic replay across:

> **Project → Branch → Theme → Tranche**

Replay MUST preserve:

- sequencing  
- dependencies  
- persona routing  
- metadata  
- identity  
- namespace  
- hierarchy metadata  

Any deviation MUST be:

- logged  
- classified as drift  
- corrected via epilogue ticket  

---
