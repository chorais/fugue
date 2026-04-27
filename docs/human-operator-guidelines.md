# **Human Operator Guidelines**  
**Version:** 2.4  
**Status:** Active  
**Audience:** Human sponsors, product engineering managers, governance participants  
**Location:** `/chorais/fugue/docs/human-operator-guidelines.md`

---

# 1. Purpose

The Human Operator Guidelines define **how humans participate in a Fugue‑governed orchestration system**.

Humans are:

- the source of product intent  
- the arbiters of ambiguity  
- the providers of domain knowledge  
- the reviewers of generated artefacts  
- the escalation path for contradictions  
- the final authority on business context  

But humans must **not** break:

- determinism  
- persona isolation  
- metadata routing  
- lifecycle transitions  
- governance envelopes  

These guidelines ensure that human involvement is **safe, structured, and non‑disruptive**.

---

# 2. The Role of the Human Operator

The Human Operator is **not** a persona.  
They are an **external authority** who interacts with the system at controlled points.

The Human Operator:

- defines product intent  
- clarifies ambiguities  
- approves tranche preambles  
- reviews DECOR for business alignment  
- reviews Ticket Maps for scope correctness  
- provides domain knowledge  
- escalates contradictions  
- approves tranche closure  

The Human Operator does **not**:

- write DECOR  
- write tickets  
- write implementation  
- write documentation (except product‑level docs)  
- perform reconciliation  
- classify drift  
- override governance  

---

# 3. Where the Human Operator Intervenes

Human intervention is allowed only at **governed lifecycle checkpoints**.

---

## 3.1 Intake Phase  
**Allowed:**  
- define tranche intent  
- define scope  
- define boundaries  
- define acceptance criteria  
- provide business constraints  
- refine the preamble  

**Not allowed:**  
- architectural decisions  
- implementation details  
- persona routing  
- metadata definition  

---

## 3.2 Bootstrap Phase  
**Allowed:**  
- clarify product intent  
- clarify domain concepts  
- validate Initial DECOR for business alignment  
- validate Ticket Map scope  

**Not allowed:**  
- modify DECOR  
- modify Ticket Map  
- override persona decisions  

---

## 3.3 Fill Phase  
**Allowed:**  
- clarify conceptual ambiguities  
- provide missing domain knowledge  

**Not allowed:**  
- write conceptual artefacts  
- influence architectural decisions  

---

## 3.4 Ticket Loop  
**Allowed:**  
- answer clarifying questions  
- provide domain‑specific examples  
- approve or reject ticket outcomes based on product intent  

**Not allowed:**  
- modify implementation  
- modify DECOR  
- modify metadata  
- modify Ticket Map  

---

## 3.5 Reconciliation  
**Allowed:**  
- review drift classification  
- approve tranche closure  
- validate Reconciled DECOR for business alignment  

**Not allowed:**  
- perform reconciliation  
- modify DECOR  
- modify drift classification  

---

# 4. Human Operator Responsibilities

The Human Operator MUST:

- provide clear, unambiguous intent  
- respond to clarification requests promptly  
- avoid mixing architectural and product concerns  
- avoid providing implementation details  
- avoid collapsing persona boundaries  
- escalate contradictions instead of resolving them  
- review governed artefacts for business alignment  
- approve tranche closure  

The Human Operator MUST NOT:

- override governance  
- override DECOR  
- override metadata  
- override persona routing  
- introduce undocumented requirements  
- introduce implicit state  
- introduce conversational drift  

---

# 5. How Humans Communicate With Personas

Humans communicate **through the Conductor**, not directly with other personas.

This ensures:

- persona isolation  
- metadata routing  
- lifecycle correctness  
- evaluator compatibility  

Direct communication with Architect, Implementer, or Auditor personas is **not allowed**.

---

# 6. How Humans Provide Clarifications

Clarifications must be:

- explicit  
- unambiguous  
- product‑level  
- domain‑level  
- free of architectural or implementation detail  

Examples of **allowed** clarifications:

- “This feature must support multi‑tenant usage.”  
- “The user must be able to export data.”  
- “The business rule is: X must always precede Y.”  

Examples of **not allowed** clarifications:

- “Use a queue for this.”  
- “Split this into two services.”  
- “Implement this using a decorator pattern.”  

Those are **Architect** or **Implementer** responsibilities.

---

# 7. How Humans Review Artefacts

Humans may review:

- tranche preambles  
- DECOR (for business alignment only)  
- Ticket Maps (for scope correctness only)  
- implementation outputs (for product correctness only)  
- documentation (for clarity only)  
- Reconciled DECOR (for final approval)  

Humans may NOT:

- modify governed artefacts  
- modify metadata  
- modify persona outputs  
- modify evaluator outputs  

If something is wrong, the Human Operator must **escalate**, not fix.

---

# 8. Escalation Rules

If the Human Operator identifies:

- a contradiction  
- a missing requirement  
- a misalignment  
- a governance violation  
- a metadata error  
- a persona drift event  

They MUST escalate to the Conductor.

The Conductor will:

- route to the correct persona  
- update DECOR (via Architect)  
- update Ticket Map  
- generate tickets  
- trigger evaluators  
- trigger reconciliation  

Humans do not fix governance issues directly.

---

# 9. What Humans Must Avoid

The Human Operator MUST NOT:

- collapse personas  
- provide architectural solutions  
- provide implementation solutions  
- modify governed artefacts  
- introduce implicit requirements  
- introduce conversational drift  
- bypass lifecycle phases  
- bypass metadata  
- bypass evaluators  
- bypass the Conductor  

These actions break determinism and governance.

---

# 10. Human Operator Anti‑Patterns

These are common mistakes that must be avoided:

### **10.1 “Just do it this way.”**  
This collapses Architect + Implementer boundaries.

### **10.2 “I’ll update DECOR myself.”**  
Only the Architect may formalise DECOR.

### **10.3 “I’ll fix the ticket.”**  
Only the Conductor may modify tickets.

### **10.4 “Let me rewrite the Ticket Map.”**  
Only the Conductor may update the Ticket Map.

### **10.5 “I’ll correct the documentation.”**  
Documentation is persona‑scoped and governed.

### **10.6 “I’ll decide which persona should handle this.”**  
Persona routing is metadata‑driven and governed.

---

# 11. Summary

The Human Operator:

- defines intent  
- clarifies ambiguities  
- reviews artefacts  
- approves tranche closure  
- escalates contradictions  

The Human Operator does **not**:

- design  
- implement  
- govern  
- reconcile  
- classify drift  
- modify metadata  
- modify DECOR  
- modify tickets  

Humans are essential — but their involvement must be **controlled, governed, and non‑disruptive**.

These guidelines ensure that human participation strengthens the system without breaking determinism, governance, or persona isolation.

---
