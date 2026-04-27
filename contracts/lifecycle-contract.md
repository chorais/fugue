# **lifecycle-contract.md (v2.4 — Hierarchy‑Complete)**  
**Lifecycle Contract — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Authority: Governance Contract  
Scope: All Personas, All Governance Layers, All Artefacts  
Lifecycle: Global (Methodology‑Level Lifecycle Rules)  

---

# 0. Metadata

```yaml
metadata:
  contract-id: "lifecycle-contract"
  version: "2.4"
  authoritative: true

  applies-to:
    - all-personas
    - all-projects
    - all-branches
    - all-themes
    - all-tranches
    - all-lifecycle-phases
    - all-ticket-maps
    - all-tickets
    - all-decor-surfaces
    - all-governed-documentation
    - all-logs
    - all-replay-traces

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  governance-envelope: "<id>"
  determinism-envelope: "<id>"
  documentation-envelope: "<id>"
  identity-propagation-contract: "<id>"
  namespace-scheme-contract: "<id>"
  ticket-map-contract: "<id>"
  ticket-template: "<id>"
```

---

# 1. Purpose

The Lifecycle Contract defines the **phases, transitions, invariants, sequencing rules, persona activation rules, and closure rules** for **all governance layers** in the Fugue Method:

> **Project → Branch → Theme → Tranche → Ticket**

The lifecycle ensures:

- deterministic execution  
- persona‑safe transitions  
- governance alignment  
- DECOR alignment  
- metadata and identity preservation  
- deterministic reconciliation  
- deterministic closure  

The lifecycle is a **governed, deterministic, persona‑scoped surface**.

---

# 2. Lifecycle Phases (v2.4)

Fugue v2.4 defines **twelve lifecycle phases**, grouped into **hierarchy bootstrap** and **execution lifecycle**.

```
Hierarchy Bootstrap:
1. Project Intake
2. Project Bootstrap
3. Branch Intake
4. Branch Bootstrap
5. Theme Intake
6. Theme Bootstrap

Execution Lifecycle:
7. Tranche Intake
8. Tranche Bootstrap
9. Conceptual Orchestration
10. Methodology Drafting (conceptual tranches only)
11. Implementation Orchestration
12. Implementation
13. Verification
14. Closure
```

Each phase is mandatory.  
No phase may be skipped, merged, or reordered.

---

# 3. Phase Definitions (Hierarchy‑Complete)

---

## **3.1 Project Intake**  
**Persona:** Curator  
**Purpose:** Establish global governance posture.  
**Outputs:**  
- project preamble  
- global governance posture  
- global acceptance criteria  

---

## **3.2 Project Bootstrap**  
**Persona:** Initiator  
**Purpose:** Create project‑level governed structure.  
**Outputs:**  
- project folder structure  
- project DECOR  
- project governance envelope  
- naming + namespace roots  
- persona map  
- identity propagation rules  
- documentation envelope  
- project bootstrap log  

---

## **3.3 Branch Intake**  
**Persona:** Curator  
**Purpose:** Define branch‑level governance posture.  
**Outputs:**  
- branch preamble  
- branch governance posture  
- branch acceptance criteria  

---

## **3.4 Branch Bootstrap**  
**Persona:** Initiator  
**Purpose:** Create branch‑level governed structure.  
**Outputs:**  
- branch folder structure  
- branch DECOR  
- branch governance envelope  
- branch naming + namespace  
- branch identity propagation  
- branch documentation envelope  
- branch bootstrap log  

---

## **3.5 Theme Intake**  
**Persona:** Curator  
**Purpose:** Define theme‑level governance posture.  
**Outputs:**  
- theme preamble  
- theme governance posture  
- theme acceptance criteria  

---

## **3.6 Theme Bootstrap**  
**Persona:** Initiator  
**Purpose:** Create theme‑level governed structure.  
**Outputs:**  
- theme folder structure  
- theme DECOR  
- theme governance envelope  
- theme naming + namespace  
- theme identity propagation  
- theme documentation envelope  
- theme bootstrap log  

---

# **Execution Lifecycle (Tranche‑Level)**

---

## **3.7 Tranche Intake**  
**Persona:** Curator  
**Purpose:** Define tranche intent, boundaries, acceptance criteria.  
**Outputs:**  
- tranche preamble  
- tranche governance posture  
- tranche acceptance criteria  

---

## **3.8 Tranche Bootstrap**  
**Persona:** Initiator  
**Purpose:** Prepare deterministic tranche workspace.  
**Outputs:**  
- tranche folder structure  
- tranche documentation envelope  
- tranche DECOR envelope  
- Ticket Map skeleton  
- tranche metadata  
- clarifications log  

---

## **3.9 Conceptual Orchestration**  
**Persona:** Conductor (Conceptual), Architect  
**Purpose:**  
- interpret preamble  
- generate conceptual Ticket Map  
- route conceptual tickets  
- enforce conceptual governance  
- ensure DECOR structural alignment  

**Outputs:**  
- conceptual Ticket Map  
- conceptual tickets  
- DECOR structural clarifications  
- conceptual lifecycle artefacts  

---

## **3.10 Methodology Drafting (conceptual tranches only)**  
**Persona:** Methodologist  
**Purpose:**  
- draft methodology artefacts  
- draft persona definitions  
- draft lifecycle rules  
- draft governance contracts  
- draft DECOR structural rules  

**Outputs:**  
- methodology drafts  
- conceptual artefacts  
- updated specifications  

---

## **3.11 Implementation Orchestration**  
**Persona:** Orchestrator (Practical)  
**Purpose:**  
- generate implementation tickets  
- enforce DECOR metadata  
- enforce governance envelopes  
- enforce persona routing  
- enforce sequencing  

**Outputs:**  
- implementation Ticket Map  
- implementation tickets  
- orchestration log  

---

## **3.12 Implementation**  
**Persona:** Implementer  
**Purpose:**  
- execute tickets  
- produce code, tests, logs, traces  
- surface technical truths  
- generate concerns  

**Outputs:**  
- implementation logs  
- replay traces  
- documentation  
- concerns  

---

## **3.13 Verification**  
**Persona:** Auditor → Verifier  
**Purpose:**  
- detect drift  
- classify drift  
- validate corrections  
- validate determinism  
- validate DECOR alignment  
- validate documentation  
- validate identity propagation  
- validate namespace correctness  

**Outputs:**  
- drift classification  
- auditor notes  
- verification report  
- reconciliation log updates  

---

## **3.14 Closure**  
**Persona:** Conductor (Conceptual), Curator  
**Purpose:**  
- validate tranche completeness  
- validate governance alignment  
- validate reconciled DECOR  
- validate reconciled artefacts  
- approve closure  

**Outputs:**  
- closure report  
- reconciled artefacts  
- updated tranche registry  

---
# 4. Lifecycle Invariants (Hierarchy‑Complete)

### **4.1 Phase Invariants**  
- All phases MUST execute in order.  
- No phase may be skipped.  
- No phase may be merged.  
- No persona may act outside its phase.  
- Project → Branch → Theme MUST complete before any tranche begins.  

### **4.2 Metadata Invariants**  
- Metadata MUST propagate across phases.  
- Metadata MUST NOT be mutated implicitly.  

### **4.3 Identity Invariants**  
- Identity MUST propagate across phases.  
- Identity lineage MUST be preserved.  

### **4.4 DECOR Invariants**  
- DECOR MUST remain stable within a tranche.  
- DECOR updates MUST follow DECOR rules.  
- DECOR inheritance MUST follow hierarchy rules.  

### **4.5 Determinism Invariants**  
- All phases MUST be deterministic.  
- All transitions MUST be deterministic.  

### **4.6 Documentation Invariants**  
- Documentation MUST be updated only via tickets.  
- Documentation MUST follow the Documentation Envelope.  

---

# 5. Lifecycle Transition Rules

Lifecycle transitions MUST be:

- deterministic  
- metadata‑preserving  
- identity‑preserving  
- governance‑aligned  
- DECOR‑aligned  
- evaluator‑aligned  

Transitions MUST NOT:

- introduce drift  
- mutate metadata implicitly  
- reorder artefacts implicitly  

Transitions MUST follow:

- Governance Envelope  
- Determinism Envelope  
- Documentation Envelope  
- Identity Propagation Contract  
- Namespace Scheme Contract  

---


# 6. Persona Activation Rules (Hierarchy‑Complete)

| Phase | Personas |
|-------|----------|
| Project Intake | Curator |
| Project Bootstrap | Initiator |
| Branch Intake | Curator |
| Branch Bootstrap | Initiator |
| Theme Intake | Curator |
| Theme Bootstrap | Initiator |
| Tranche Intake | Curator |
| Tranche Bootstrap | Initiator |
| Conceptual Orchestration | Conductor (Conceptual), Architect |
| Methodology Drafting | Methodologist |
| Implementation Orchestration | Orchestrator (Practical) |
| Implementation | Implementer |
| Verification | Auditor → Verifier |
| Closure | Conductor (Conceptual), Curator |

No persona may activate outside its phase.

---

# 7. Lifecycle Drift Classification

Lifecycle drift MUST be classified as:

### **Critical**
- skipped phases  
- reordered phases  
- persona acting outside lifecycle  
- missing lifecycle metadata  
- corrupted lifecycle logs  

### **Major**
- incomplete lifecycle artefacts  
- incorrect persona routing  
- incorrect sequencing  

### **Minor**
- formatting issues  
- non‑blocking metadata issues  

All lifecycle drift MUST be recorded in:

- auditor notes  
- reconciliation log  
- reconciled DECOR  

---

# 8. Lifecycle Correction (Epilogue Workflow)

If lifecycle drift exists:

1. **Orchestrator** MUST generate an epilogue ticket  
2. **Responsible persona** MUST correct lifecycle artefacts  
3. **Auditor** MUST validate corrections  
4. **Verifier** MUST validate final lifecycle correctness  
5. **Conductor** MUST validate conceptual alignment  
6. **Curator** MUST approve lifecycle correction  
7. **Orchestrator** MUST update reconciliation lineage  

Lifecycle corrections MUST NOT occur outside persona boundaries.

---

# 9. Lifecycle and DECOR

Lifecycle MUST align with:

- DECOR invariants  
- DECOR constraints  
- DECOR metadata  
- DECOR identity lineage  
- Reconciled DECOR  

Lifecycle MUST NOT:

- override DECOR  
- weaken invariants  
- contradict governance envelopes  

---
