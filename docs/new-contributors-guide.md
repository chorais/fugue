Perfect — here’s exactly what you asked for:

---

# ✅ **1. Reusable DECOR Patch Block (v2.4‑canonical)**  
You can paste this block into any document that references DECOR.

---

## **📌 DECOR Acronym Patch (Drop‑in Block)**

> **DECOR stands for Design, Extensions, Considerations, Opportunities, and Risks.  
> In Fugue v2.4, DECOR is the Declarative Contract of Record — the canonical architectural contract for a tranche.  
> DECOR defines architectural intent, invariants, constraints, metadata, evaluator surfaces, and reconciliation surfaces, and is validated against the DECOR JSON Schema.**

---

This block is **self‑contained**, **canonical**, and **safe to reuse** across all methodology‑level documents.

---

# ✅ **2. Regenerated `docs/new-contributors-guide.md` with DECOR acronym included**

Below is the **full updated file**, now including the DECOR acronym in the correct place (Section 10), and aligned with the v2.4 governance hierarchy, persona model, lifecycle, metadata flow, and DECOR grounding model.

Paste this directly into:

```
/fugue/docs/new-contributors-guide.md
```

---

# **New Contributors Guide (v2.4)**  
Version: 2.4  
Status: Active (Frozen)  
Audience: New contributors to the Fugue Methodology or any Fugue‑governed project  

---

# 1. Welcome to Fugue

Fugue is a **governance‑first orchestration method** for AI‑assisted software development.

It ensures that:

- work is deterministic  
- reasoning is persona‑isolated  
- architecture is governed  
- implementation is auditable  
- documentation is structured  
- metadata drives execution  
- identity and namespace rules are preserved  
- the system is reproducible and replayable  

This guide gives you everything you need to contribute safely and confidently.

---

# 2. What Makes Fugue Different?

Fugue is not a framework.  
It is not a coding style.  
It is not a project template.

Fugue is a **methodology** that governs:

- how personas think  
- how artefacts flow  
- how architecture is formalised  
- how implementation is executed  
- how correctness is validated  
- how drift is classified  
- how documentation is produced  
- how tranches are closed  

It is designed to make AI‑assisted development:

- predictable  
- auditable  
- safe  
- scalable  
- repeatable  

If you follow the rules, Fugue works beautifully.  
If you break the rules, Fugue will catch you — by design.

---

# 3. Governance Hierarchy (v2.4)

Before you understand personas or lifecycle, you must understand **where work lives**.

Fugue defines a **four‑level governance hierarchy**:

```
Project
  → Branch
      → Theme
          → Tranche
```

### **Project (P<id>)**  
The highest‑level governance container.  
Defines mission, architectural domain, governance envelope, naming + namespace roots.

### **Branch (B<id>)**  
An execution lane inside a Project.  
Branches realise Themes and provide identity + namespace roots for execution.

### **Theme (T<id>)**  
A conceptual grouping of related work.  
Conceptually lives under a Project; structurally realised inside a Branch.

### **Tranche (C<id>)**  
The atomic execution unit.  
Contains preamble, DECOR, Ticket Map, implementation, reconciliation, verification, and closure.

You will spend most of your time working **inside a Tranche**.

---

# 4. Persona Model (v2.4)

Fugue uses **two persona layers**: conceptual (governance) and practical (execution).  
These are *not* job titles — they are *thinking modes* with strict boundaries.

---

## 4.1 Conceptual Personas (Governance Layer)

| Persona | Responsibilities | Forbidden |
|--------|------------------|-----------|
| **Curator** | Defines tranche mission, boundaries, acceptance criteria; approves closure | Must not design or implement |
| **Conductor** | Lifecycle orchestration, persona routing, metadata enforcement | Must not implement or reconcile |
| **Architect** | DECOR formalisation, invariants, constraints, structural reasoning | Must not implement |
| **Methodologist** | Evolves the methodology itself | Must not participate in project execution |

---

## 4.2 Practical Personas (Execution Layer)

| Persona | Responsibilities | Forbidden |
|--------|------------------|-----------|
| **Initiator** | Starts a tranche, produces the tranche preamble | Must not design or implement |
| **Orchestrator** | Manages the ticket loop, dispatches tickets | Must not implement |
| **Implementer** | Executes tickets, produces code/tests/logs/traces | Must not design or govern |
| **Auditor** | Drift classification, governance validation, reconciliation | Must not implement |
| **Verifier** | Final validation before closure | Must not implement or design |

You will switch personas depending on the task — but **never mix them**.

---

# 5. The Six‑Phase Lifecycle (v2.4)

Every tranche follows the same deterministic lifecycle:

```
Bootstrap
→ Interpretation
→ Implementation
→ Reconciliation
→ Verification
→ Closure
```

### **Bootstrap**  
Curator defines mission; Initiator produces tranche preamble.

### **Interpretation**  
Architect formalises DECOR; Conductor validates metadata;  
**Architect selects Method A or Method B grounding strategy.**

### **Implementation**  
Orchestrator dispatches tickets; Implementer executes in isolated conversations.

### **Reconciliation**  
Auditor classifies drift; Architect performs structural reconciliation; Reconciled DECOR produced.

### **Verification**  
Test suite execution (golden, dark, governance, replay); Verifier validates correctness.

### **Closure**  
Curator approves closure; tranche archived as immutable lineage.

Lifecycle phases MUST NOT be skipped or reordered.

---

# 6. Method A/B Grounding (v2.4 Interpretation Phase)

Fugue v2.4 preserves **Method A** and **Method B**, but they are no longer lifecycle forks.  
They are now:

> **Optional DECOR grounding strategies selected by the Architect during Phase 2 — Interpretation.**

### **Method A — Product‑First Grounding**  
Used when product intent is clear.  
Implementer ingress analysis optional.

### **Method B — Technical‑First Grounding**  
Used when architecture must be discovered.  
Implementer ingress analysis mandatory.

These strategies do **not** change:

- lifecycle  
- persona routing  
- governance  
- envelopes  
- templates  
- schemas  

They only influence **how DECOR is initially formalised**.

---

# 7. Metadata: The Heart of Fugue

Metadata governs:

- persona routing  
- lifecycle transitions  
- documentation routing  
- evaluator execution  
- drift classification  
- identity and namespace propagation  

Metadata flows through the system like this:

```
DECOR metadata
→ Ticket Map metadata
→ Dispatch metadata
→ Implementation metadata
→ Audit metadata
→ Reconciled DECOR metadata
```

If metadata is wrong, the tranche is wrong.

---

# 8. How to Work on a Ticket

When you receive a ticket:

### **1. Read the Ticket Map entry**  
It tells you:

- persona routing  
- metadata  
- acceptance criteria  
- documentation requirements  
- invariants  

### **2. Enter the correct persona**  
If the ticket says `implementer`, you MUST think like an Implementer.  
If it says `architect`, you MUST think like an Architect.

### **3. Never mix personas**  
If you need architectural clarification, escalate — do not guess.

### **4. Produce deterministic artefacts**  
Implementation logs, replay traces, tests, code.

### **5. Surface contradictions**  
If DECOR is wrong or incomplete, you MUST report it.

### **6. Never modify DECOR**  
Only the Architect can do that.

---

# 9. Avoiding Persona Drift

Persona drift is when you accidentally think like the wrong persona.

Examples:

- Implementer suggesting architectural changes  
- Architect writing implementation details  
- Conductor making design decisions  
- Auditor proposing fixes  
- Curator suggesting implementation details  

To avoid drift:

- Always check your persona  
- Always check the Ticket Map  
- Always check metadata  
- Always escalate instead of guessing  

Drift is classified by the Auditor and may require reconciliation.

---

# 10. How to Read DECOR

## **What DECOR Stands For**

> **DECOR = Design, Extensions, Considerations, Opportunities, Risks.  
> In Fugue v2.4, DECOR is the Declarative Contract of Record — the canonical architectural contract for a tranche.  
> It defines architectural intent, invariants, constraints, metadata, evaluator surfaces, and reconciliation surfaces, and is validated against the DECOR JSON Schema.**

### **How to use DECOR**

DECOR is:

- canonical  
- authoritative  
- schema‑validated  
- immutable except via governed updates  

If DECOR contradicts implementation, implementation is wrong.  
If DECOR contradicts reality, DECOR must be updated — by the Architect.

---

# 11. Documentation Rules

Documentation is governed by the **Documentation Envelope Contract**.

Key rules:

- All governed docs live in `/fugue_docs/`  
- `/docs` is methodology documentation  
- Documentation must be persona‑scoped  
- Documentation must be metadata‑aligned  
- Documentation must be deterministic  

Documentation drift is classified by the Auditor.

---

# 12. Evaluators

Evaluators are deterministic governance components that:

- enforce invariants  
- enforce metadata  
- enforce persona routing  
- validate artefacts  
- produce diagnostics  

Evaluators are not personas.  
They do not modify artefacts.  
They enforce correctness.

---

# 13. What You Should Do as a New Contributor

- Read the Methodology Overview  
- Read the Contract Suite README  
- Read the DECOR Specification  
- Read the Lifecycle Contract  
- Read your ticket  
- Enter the correct persona  
- Follow metadata  
- Produce deterministic artefacts  
- Surface contradictions  
- Avoid persona drift  
- Ask questions early  

You do **not** need to understand everything on day one.  
You just need to follow the rules.

---

# 14. What You Should Never Do

- Modify DECOR  
- Modify metadata  
- Mix personas  
- Skip lifecycle phases  
- Change the Ticket Map  
- Add undocumented dependencies  
- Write documentation in the wrong namespace  
- Guess about architecture  
- Guess about governance  
- Ignore evaluator diagnostics  

If you’re unsure — escalate.

---

# 15. Where to Go Next

You should now read:

- **Methodology Overview**  
- **DECOR Specification**  
- **Ticket Map Contract**  
- **Documentation Envelope Contract**  

Then:

- Start with a small Implementer ticket  
- Learn the metadata flow  
- Learn persona boundaries  
- Learn the lifecycle  

You’ll be productive very quickly.

---

# 16. Summary

You now understand:

- the v2.4 governance hierarchy  
- the v2.4 persona model  
- the v2.4 lifecycle  
- the v2.4 governance envelopes  
- the v2.4 DECOR model  
- the v2.4 metadata flow  
- how to work on tickets  
- how to avoid drift  
- how to contribute safely  

Welcome to Fugue.  
You are now ready to participate in a governed, deterministic, auditable orchestration system.

---
