# **Why Fugue Does Not Have a QA Persona**  
**Version:** 2.4  
**Status:** Active  
**Audience:** Contributors to the Fugue Methodology  
**Location:** `/chorais/fugue/docs/qa-persona-explanation.md`

---

# 1. Purpose

This document explains **why the Fugue Orchestration Method does not define a QA persona**, and why introducing one would violate:

- persona boundaries  
- governance envelopes  
- metadata‑driven lifecycle rules  
- evaluator semantics  
- deterministic execution  

It also clarifies **how quality is achieved in Fugue** without a QA persona.

---

# 2. The Core Reason: QA Is Not a Persona — It Is a *Property of the System*

In Fugue, **quality is not the responsibility of a single persona**.

Instead, quality is:

- **distributed across personas**,  
- **enforced by metadata**,  
- **validated by evaluators**, and  
- **certified by the Auditor**.

A QA persona would:

- collapse persona boundaries  
- duplicate responsibilities already governed elsewhere  
- introduce non‑deterministic reasoning  
- break evaluator semantics  
- violate the Conductor and Auditor contracts  
- create an ungoverned reasoning surface  

Fugue avoids this by embedding QA into the **methodology**, not into a **persona**.

---

# 3. What a QA Persona *Would* Do — and Why That’s a Problem

A hypothetical QA persona would:

- inspect implementation  
- validate correctness  
- check invariants  
- check documentation  
- check metadata  
- check routing  
- check DECOR alignment  

But these responsibilities are already **governed**:

| Responsibility | Already Owned By |
|----------------|------------------|
| Implementation correctness | Implementer + Evaluators |
| Architectural correctness | Architect |
| Metadata correctness | Conductor + Evaluators |
| Routing correctness | Conductor + Auditor |
| Drift classification | Auditor |
| Documentation correctness | Auditor + Documentation Envelope |
| Lifecycle correctness | Conductor + Evaluators |

A QA persona would **overlap with every persona**, violating the Persona Creation Rules (coming next).

---

# 4. How Fugue Ensures Quality Without a QA Persona

Quality in Fugue is achieved through **four governance mechanisms**:

---

## 4.1 DECOR (Declarative Contract of Record)

DECOR defines:

- invariants  
- constraints  
- evaluator semantics  
- risks  
- opportunities  
- metadata  

Quality begins with **correct architecture**, not post‑hoc inspection.

---

## 4.2 Metadata (The Governance Engine)

Metadata enforces:

- persona routing  
- documentation requirements  
- Fill Phase requirements  
- evaluator execution  
- lifecycle transitions  

Quality is **encoded**, not inspected.

---

## 4.3 Evaluators (Deterministic Governance Logic)

Evaluators enforce:

- invariants  
- metadata correctness  
- routing correctness  
- dependency correctness  
- documentation correctness  
- implementation correctness  

Evaluators are **pure governance logic**, not personas.

They *are* the QA system.

---

## 4.4 Auditor (Final Governance Authority)

The Auditor:

- validates all artefacts  
- classifies drift  
- requests epilogue tickets  
- produces Reconciled DECOR  

The Auditor is the **final quality gate**.

A QA persona would duplicate the Auditor’s role and break governance.

---

# 5. Why QA Cannot Be a Persona (Governance Argument)

A persona must:

- have a unique cognitive boundary  
- own a unique reasoning domain  
- not overlap with other personas  
- not duplicate evaluator logic  
- not collapse lifecycle phases  
- not break determinism  

A QA persona would violate all six rules.

### **5.1 No Unique Cognitive Boundary**  
QA is not a reasoning domain — it is a property of artefacts.

### **5.2 Overlaps With All Personas**  
QA touches architecture, implementation, governance, documentation, metadata.

### **5.3 Duplicates Evaluator Logic**  
Evaluators already enforce correctness deterministically.

### **5.4 Collapses Lifecycle Phases**  
QA would sit between Implementer and Auditor, breaking the lifecycle.

### **5.5 Breaks Determinism**  
QA introduces subjective reasoning, which Fugue forbids.

### **5.6 Violates Metadata‑Driven Governance**  
QA would require new metadata surfaces that contradict existing ones.

---

# 6. What People *Think* QA Means — and Where It Actually Lives in Fugue

| Traditional QA Activity | Fugue Equivalent |
|-------------------------|------------------|
| Test correctness | Implementer + Evaluators |
| Validate architecture | Architect + Evaluators |
| Validate implementation | Implementer + Evaluators |
| Validate documentation | Documentation Envelope + Auditor |
| Validate requirements | DECOR + Conductor |
| Validate sequencing | Ticket Map + Evaluators |
| Validate completeness | Auditor |
| Validate governance | Auditor + Evaluators |

Quality is **systemic**, not persona‑based.

---

# 7. What Happens If Someone Tries to Introduce a QA Persona?

It would immediately trigger:

- **Critical Drift** (Auditor Contract)  
- **Persona Routing Violation** (Conductor Contract)  
- **Metadata Drift** (Evaluator Model Contract)  
- **Governance Envelope Violation** (Documentation Envelope Contract)  
- **Lifecycle Violation** (Tranche Lifecycle Contract)  
- **Persona Creation Rule Violation** (next document)  

A QA persona is **not allowed** under Fugue governance.

---

# 8. Summary

Fugue does not have a QA persona because:

- QA is not a reasoning domain  
- QA is not a persona boundary  
- QA is a property of the system  
- QA is enforced by metadata  
- QA is enforced by evaluators  
- QA is validated by the Auditor  
- QA is distributed across personas  
- QA as a persona would violate governance  

Quality in Fugue is **designed in**, not inspected in.

---
