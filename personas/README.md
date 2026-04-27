# 🎼 **README — Fugue Personas (v2.4)**  
**Location:** `/fugue/personas/`  
**Status:** Active  
**Version:** 2.4

---

# 1. Purpose of This Directory

The `fugue/personas/` directory defines the **cognitive architecture** of the Fugue Orchestration Method.

It contains:

- **Persona Instructions** — descriptive, narrative, human‑readable  
- **Persona Contracts** — enforceable, deterministic, governance artefacts  
- **Persona Index** — authoritative map of all personas  

Together, these files define:

- *who* participates in the methodology  
- *what* each persona is responsible for  
- *when* each persona is active  
- *how* personas interact  
- *which boundaries* personas must respect  

This directory is the **single source of truth** for persona behaviour in Fugue v2.4.

---

# 2. Persona Model Overview

Fugue v2.4 defines **nine personas**, split into two classes:

---

## 2.1 Conceptual Personas  
Operate in the **methodology domain**.  
Define structure, governance, invariants, and conceptual truth.  
Never implement code.

| Persona | Purpose |
|--------|---------|
| **Curator** | Governance authority; defines intent, posture, boundaries, acceptance criteria |
| **Conductor (Conceptual Mode)** | Orchestrates methodology‑refinement tranches |
| **Methodologist** | Drafts methodology artefacts, templates, lifecycle rules |
| **Architect** | Derives DECOR, defines invariants, constraints, conceptual artefacts |

Conceptual personas define **what must be true**.

---

## 2.2 Practical Personas  
Operate in the **execution domain**.  
Execute, validate, and reconcile implementation.  
Never modify methodology.

| Persona | Purpose |
|--------|---------|
| **Initiator** | Bootstraps tranche workspace and prepares deterministic envelopes |
| **Orchestrator (Practical Mode)** | Implementation governance cortex; generates tickets; enforces DECOR metadata |
| **Implementer** | Executes tickets: code, tests, logs, traces, documentation |
| **Auditor** | Detects and classifies drift; validates implementation and documentation |
| **Verifier** | Validates drift corrections and approves technical closure |

Practical personas define **how the work is executed**.

---

# 3. Directory Structure

```
/fugue/personas/
    persona-index.md
    README.md

    conceptual/
        curator-persona-instructions.md
        conductor-persona-instructions.md
        methodologist-persona-instructions.md
        architect-persona-instructions.md
        contracts/
            curator-persona-contract.md
            conductor-persona-contract.md
            methodologist-persona-contract.md
            architect-persona-contract.md

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

    archive/
        legacy-personas.md
```

### Notes

- **Instructions** = narrative, descriptive  
- **Contracts** = deterministic, enforceable governance artefacts  
- **Index** = authoritative map of all personas  
- **Archive** = deprecated personas (Intake Authority (v2.0), Executor, Orchestrator v2.0, Verifier v2.0, Initiator v2.0)

---

# 4. Persona Instructions vs Persona Contracts

Fugue v2.4 introduces a strict separation:

## 4.1 Persona Instructions  
- Human‑readable  
- Narrative  
- Descriptive  
- Explain *how* the persona behaves  
- Provide context and rationale  
- Not enforceable  

## 4.2 Persona Contracts  
- Governance artefacts  
- Deterministic  
- Metadata‑aligned  
- Lifecycle‑aligned  
- Enforceable  
- Define strict boundaries  
- Define allowed and prohibited behaviours  
- Define interaction rules  
- Define DECOR responsibilities  

**Instructions describe.  
Contracts govern.**

Both are required for a complete persona definition.

---

# 5. Persona Isolation Rules

Fugue v2.4 enforces strict persona isolation:

1. **One persona per conversation**  
2. **No persona switching**  
3. **No cross‑persona reasoning**  
4. **No implicit memory**  
5. **All communication via governed artefacts**  
6. **Conceptual personas never implement**  
7. **Practical personas never modify DECOR**  
8. **Architect never implements**  
9. **Implementer never performs conceptual reasoning**  
10. **Auditor never corrects drift**  
11. **Verifier never classifies drift**  

These rules ensure deterministic, auditable execution.

---

# 6. Lifecycle Alignment

Each persona participates in specific lifecycle phases:

| Lifecycle Phase | Active Personas |
|-----------------|-----------------|
| **Intake** | Curator |
| **Bootstrap** | Initiator |
| **Conceptual Orchestration** | Conductor (Conceptual), Architect |
| **Methodology Drafting** | Methodologist |
| **Implementation Orchestration** | Orchestrator (Practical) |
| **Implementation** | Implementer |
| **Verification** | Auditor → Verifier |
| **Closure** | Conductor (Conceptual), Curator |

This mapping ensures deterministic persona routing.

---

# 7. DECOR Responsibilities

| Persona | DECOR Role |
|---------|------------|
| **Curator** | Approves DECOR changes |
| **Conductor (Conceptual)** | Ensures conceptual alignment |
| **Architect** | Derives and updates DECOR |
| **Orchestrator** | Enforces DECOR metadata |
| **Implementer** | Applies DECOR |
| **Auditor** | Validates DECOR alignment |
| **Verifier** | Validates reconciled DECOR |

No other persona may modify or reinterpret DECOR.

---

# 8. Drift Responsibilities

| Persona | Drift Role |
|---------|------------|
| **Implementer** | Surfaces technical truths |
| **Auditor** | Detects and classifies drift |
| **Orchestrator** | Generates corrective tickets |
| **Verifier** | Validates drift corrections |
| **Conductor (Conceptual)** | Validates conceptual alignment |
| **Curator** | Validates governance alignment |

Drift is always corrected by **tickets**, never by personas directly.

---

# 9. Versioning

All personas follow:

- **Semantic versioning**  
- **Fugue Method versioning**  
- **Persona contract stability rules**  

Persona contracts are immutable once published.  
Persona instructions may evolve under Curator‑approved methodology‑refinement tranches.

---

# 10. Summary

The `fugue/personas/` directory defines the **cognitive backbone** of the Fugue Method.

It provides:

- a deterministic persona model  
- strict persona isolation  
- conceptual/practical separation  
- governance‑aligned execution  
- reproducible orchestration  
- substrate‑agnostic reasoning  

Together, these personas form the **governance substrate** of Fugue v2.4.

---