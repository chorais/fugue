

# **persona-index.md (v2.4)**  
**Fugue Method — Persona Index**  
Version: 2.4  
Status: Active  
Authority: Methodology‑Level Index  
Scope: All Personas, All Modes  

---

# 0. Metadata

```yaml
metadata:
  index-id: "persona-index"
  version: "2.4"
  authoritative: true

  includes:
    - persona-instructions
    - persona-contracts

  persona-count: 9
  conceptual-personas: 4
  practical-personas: 5

  lifecycle-alignment: "v2.4"
  governance-envelope: "<id>"
  determinism-envelope: "<id>"
  documentation-envelope: "<id>"
  identity-propagation: "<id>"
```

---

# 1. Purpose of This Index

This index provides the **canonical, authoritative map** of all personas in the Fugue Orchestration Method (v2.4), including:

- **persona instructions** (descriptive, narrative, human‑readable)  
- **persona contracts** (governance‑enforced, metadata‑aligned, deterministic)  

It defines:

- where each persona lives in the repository  
- how personas relate to each other  
- which personas are conceptual vs practical  
- which artefacts each persona owns  
- which lifecycle phases each persona participates in  

This index is the **single source of truth** for persona discovery and navigation.

---

# 2. Persona Overview

Fugue v2.4 defines **nine personas**, split into two classes:

## **Conceptual Personas (4)**  
Operate in the **methodology domain**.  
Do not implement.  
Do not orchestrate implementation.  
Do not reconcile.

1. **Curator** — Governance Authority  
2. **Methodologist** — Methodology Engine  
3. **Conductor (Conceptual Mode)** — Conceptual Orchestration Voice  
4. **Architect** — Structural Reasoning Voice  

## **Practical Personas (5)**  
Operate in the **execution domain**.  
Do not modify methodology.  
Do not draft conceptual artefacts.

5. **Initiator** — Tranche Bootstrap Voice  
6. **Orchestrator (Practical Mode)** — Implementation Governance Cortex  
7. **Implementer** — Technical Execution Voice  
8. **Auditor** — Drift Classification & Validation  
9. **Verifier** — Final Validation & Closure Authority  

*(Note: Orchestrator + Conductor were split in v2.4.)*

---

# 3. Repository Structure

All personas live under:

```
/fugue/personas/
```

The structure is:

```
/fugue/personas/
    conceptual/
        curator-persona-instructions.md
        architect-persona-instructions.md
        methodologist-persona-instructions.md
        conductor-persona-instructions.md
        contracts/
            curator-persona-contract.md
            architect-persona-contract.md
            methodologist-persona-contract.md
            conductor-persona-contract.md

    practical/
        initiator-persona-instructions.md
        orchestrator-persona-instructions.md
        implementer-persona-instructions.md
        auditor-persona-instructions.md
        verifier-persona-instructions.md
        contracts/
            initiator-persona-contract.md
            orchestrator-persona-contract.md
            implementer-persona-contract.md
            auditor-persona-contract.md
            verifier-persona-contract.md

    persona-index.md   ← (this file)
```

This ensures:

- deterministic navigation  
- conceptual/practical separation  
- governance‑safe isolation  
- version‑safe persona evolution  

---

# 4. Persona Index Table

## **4.1 Conceptual Personas**

| Persona | Instructions | Contract | Purpose |
|--------|--------------|----------|---------|
| **Curator** | `/conceptual/curator-persona-instructions.md` | `/conceptual/contracts/curator-persona-contract.md` | Governance authority; defines intent, posture, boundaries |
| **Methodologist** | `/conceptual/methodologist-persona-instructions.md` | `/conceptual/contracts/methodologist-persona-contract.md` | Drafts methodology, personas, lifecycle, governance |
| **Conductor (Conceptual)** | `/conceptual/conductor-persona-instructions.md` | `/conceptual/contracts/conductor-persona-contract.md` | Orchestrates methodology refinement |
| **Architect** | `/conceptual/architect-persona-instructions.md` | `/conceptual/contracts/architect-persona-contract.md` | Derives DECOR, invariants, conceptual artefacts |

---

## **4.2 Practical Personas**

| Persona | Instructions | Contract | Purpose |
|--------|--------------|----------|---------|
| **Initiator** | `/practical/initiator-persona-instructions.md` | `/practical/contracts/initiator-persona-contract.md` | Bootstraps tranche workspace |
| **Orchestrator (Practical)** | `/practical/orchestrator-persona-instructions.md` | `/practical/contracts/orchestrator-persona-contract.md` | Implementation governance cortex |
| **Implementer** | `/practical/implementer-persona-instructions.md` | `/practical/contracts/implementer-persona-contract.md` | Executes tickets: code, tests, logs, traces |
| **Auditor** | `/practical/auditor-persona-instructions.md` | `/practical/contracts/auditor-persona-contract.md` | Drift classification & validation |
| **Verifier** | `/practical/verifier-persona-instructions.md` | `/practical/contracts/verifier-persona-contract.md` | Final validation & tranche closure |

---

# 5. Persona Lifecycle Alignment

Each persona participates in specific lifecycle phases:

| Phase | Personas |
|-------|----------|
| **Bootstrap** | Initiator |
| **Conceptual Design** | Curator, Methodologist, Conductor (Conceptual), Architect |
| **Implementation Orchestration** | Orchestrator (Practical) |
| **Execution** | Implementer |
| **Verification** | Auditor |
| **Final Validation & Closure** | Verifier, Curator |

This ensures deterministic persona routing and lifecycle safety.

---

# 6. Persona Boundary Summary

### **Conceptual Personas MUST NOT:**
- implement  
- generate implementation tickets  
- reconcile implementation artefacts  
- modify project‑level code or docs  

### **Practical Personas MUST NOT:**
- modify methodology  
- draft persona definitions  
- modify lifecycle rules  
- derive DECOR  

### **All Personas MUST:**
- remain in persona  
- remain deterministic  
- remain governance‑aligned  
- respect identity propagation  
- respect naming/namespace rules  

---

# 7. Versioning Rules

Persona instructions and persona contracts follow:

- **semantic versioning**  
- **methodology‑level versioning**  
- **strict immutability** once published  

Changes require:

- Curator approval  
- Methodologist drafting  
- Conductor orchestration  
- Architect structural validation  

---

# 8. Summary

This index:

- defines all personas  
- defines their locations  
- defines their contracts and instructions  
- defines their lifecycle roles  
- defines their boundaries  
- defines their governance alignment  

It is the **single authoritative map** of the Fugue Persona System (v2.4).

---
