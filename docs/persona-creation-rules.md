# **Persona Creation Rules (v2.4)**  
Version: 2.4  
Status: Active (Frozen)  
Audience: Contributors to the Fugue Methodology  
Authority: Governance Envelope Contract (v2.4)  

---

# 1. Purpose

This document defines the **governance rules** for creating new personas within the Fugue Orchestration Method.

Personas are **cognitive boundaries**, not job titles.  
They define:

- what a reasoning mode is allowed to think about  
- what it is forbidden from thinking about  
- what artefacts it may produce  
- what artefacts it may not produce  
- how it interacts with other personas  
- how it participates in the lifecycle  

Because personas are foundational to determinism, governance, metadata routing, and evaluator correctness, **new personas may only be created under strict conditions**.

This document ensures:

- persona isolation  
- governance consistency  
- metadata correctness  
- lifecycle stability  
- evaluator compatibility  
- drift prevention  
- namespace and identity propagation integrity  

---

# 2. Why Persona Creation Is Strictly Controlled

Personas are the **core abstraction** that makes Fugue deterministic.

If personas proliferate:

- reasoning becomes ambiguous  
- metadata becomes inconsistent  
- routing becomes unpredictable  
- lifecycle transitions break  
- evaluator semantics collapse  
- drift becomes unmanageable  
- governance envelopes become unenforceable  
- identity and namespace propagation become unstable  

Therefore, Fugue enforces **strict persona creation rules** to preserve system integrity.

---

# 3. The Canonical Persona Model (v2.4)

Fugue defines **two persona layers**, each with strict boundaries.

---

## 3.1 Conceptual Personas (Governance Layer)

These govern the methodology itself:

1. **Curator** — governance authority, tranche approval, closure  
2. **Conductor** — lifecycle orchestration, persona routing, metadata enforcement  
3. **Architect** — DECOR formalisation, invariants, constraints, structural reasoning  
4. **Methodologist** — evolves the methodology (meta‑layer)  

These personas define the **governance and reasoning authority** of the method.

---

## 3.2 Practical Personas (Execution Layer)

These execute the method inside a project:

1. **Initiator** — starts a tranche and produces the tranche preamble  
2. **Orchestrator** — manages the ticket loop and persona routing  
3. **Implementer** — executes tickets, produces code/tests/logs/traces  
4. **Auditor** — drift classification, governance validation, reconciliation  
5. **Verifier** — final validation before closure  

These personas define the **operational execution** of the method.

---

# 4. Persona Creation Criteria (All Must Be Satisfied)

A new persona may only be created if **all** of the following criteria are met.

---

## **4.1 Unique Cognitive Boundary**  
The proposed persona must have a **reasoning domain** that:

- is not covered by any existing conceptual or practical persona  
- cannot be expressed as a subset of an existing persona  
- cannot be expressed as metadata  
- cannot be expressed as evaluator logic  
- cannot be expressed as lifecycle transitions  

If the domain overlaps with an existing persona, the persona is **not allowed**.

---

## **4.2 Unique Artefact Ownership**  
The persona must produce artefacts that:

- no existing persona is responsible for  
- cannot be produced by evaluators  
- cannot be produced by metadata  
- cannot be produced by templates or schemas  
- cannot be produced by lifecycle transitions  

If the artefacts overlap with existing persona responsibilities, the persona is **not allowed**.

---

## **4.3 Unique Lifecycle Role**  
The persona must participate in the lifecycle in a way that:

- does not duplicate an existing phase  
- does not collapse phases  
- does not introduce new uncontrolled phases  
- does not break determinism  
- does not alter the six‑phase lifecycle  

If the persona fits into an existing lifecycle phase, it is **not allowed**.

---

## **4.4 No Overlap With Evaluators**  
Evaluators enforce:

- invariants  
- metadata  
- routing  
- documentation correctness  
- dependency correctness  
- implementation correctness  
- replay correctness  

If the proposed persona overlaps with evaluator responsibilities, it is **not allowed**.

---

## **4.5 No Overlap With Governance Contracts**  
If the persona’s responsibilities can be:

- encoded in metadata  
- enforced by evaluators  
- governed by contracts  
- handled by lifecycle transitions  
- expressed as namespace or identity propagation rules  

…then the persona is **not allowed**.

---

## **4.6 Must Not Introduce Subjective Reasoning**  
Personas must be:

- deterministic  
- reproducible  
- governed  
- metadata‑aligned  

If the persona introduces:

- subjective judgement  
- heuristic reasoning  
- ambiguous decision‑making  
- non‑deterministic behaviour  

…it is **not allowed**.

---

## **4.7 Must Not Break Persona Isolation**  
The persona must not:

- think like another persona  
- produce artefacts owned by another persona  
- reason across domains  
- collapse boundaries  
- require shared conversational context  

If it does, it is **not allowed**.

---

## **4.8 Must Be Compatible With Metadata Routing**  
The persona must:

- have clear metadata surfaces  
- have clear routing rules  
- integrate with the Ticket Map  
- integrate with DECOR  
- integrate with the namespace scheme  
- integrate with identity propagation  

If metadata cannot route to it cleanly, the persona is **not allowed**.

---

## **4.9 Must Be Compatible With Evaluators**  
Evaluators must be able to:

- validate the persona’s artefacts  
- enforce invariants  
- classify drift  
- validate metadata  
- validate naming and namespace rules  

If evaluator integration is unclear, the persona is **not allowed**.

---

## **4.10 Must Not Duplicate Human Operator Responsibilities**  
If the persona’s responsibilities are:

- product‑level  
- domain‑level  
- business‑level  
- contextual  
- human‑judgement‑based  

…then they belong to the **Human Operator**, not a persona.

---

# 5. Persona Creation Workflow (v2.4)

If a new persona is proposed, the following workflow MUST be followed:

1. **Proposal Drafted**  
   - reasoning domain  
   - artefact ownership  
   - lifecycle role  
   - metadata surfaces  
   - evaluator integration  
   - namespace and identity propagation impact  

2. **Conductor Review**  
   - routing analysis  
   - metadata analysis  
   - lifecycle analysis  

3. **Architect Review**  
   - DECOR integration  
   - structural analysis  
   - invariants and constraints  

4. **Auditor Review**  
   - drift risk analysis  
   - governance envelope analysis  

5. **Evaluator Review**  
   - invariant enforcement analysis  
   - metadata validation feasibility  

6. **Curator Decision**  
   - persona accepted or rejected  
   - if accepted, a new **Persona Contract** MUST be created  

No persona may exist without a contract.

---

# 6. Examples of Personas That Are Not Allowed

## **6.1 QA Persona**  
Rejected because:

- overlaps with Implementer, Architect, Auditor, Verifier, Evaluators  
- duplicates evaluator logic  
- breaks lifecycle  
- introduces subjective reasoning  

(See separate document.)

---

## **6.2 Product Manager Persona**  
Rejected because:

- overlaps with Curator and Human Operator  
- introduces business‑level reasoning  
- breaks persona isolation  

---

## **6.3 Security Persona**  
Rejected because:

- overlaps with Evaluators (security invariants)  
- overlaps with Architect (security constraints)  
- overlaps with Auditor (security drift)  

---

## **6.4 Documentation Persona**  
Rejected because:

- documentation is persona‑scoped  
- governed by the Documentation Envelope  
- validated by the Auditor  

---

# 7. When a New Persona *Is* Allowed

A new persona is allowed only if:

- it introduces a **new reasoning domain**  
- that cannot be expressed as metadata  
- cannot be expressed as evaluator logic  
- cannot be expressed as lifecycle transitions  
- cannot be expressed as a subset of an existing persona  
- does not break determinism  
- integrates cleanly with governance  
- integrates cleanly with metadata routing  
- integrates cleanly with evaluators  
- integrates cleanly with naming and namespace rules  

This is extremely rare.

---

# 8. Summary

A new persona may only be created if:

- it has a unique reasoning domain  
- it owns unique artefacts  
- it has a unique lifecycle role  
- it does not overlap with existing personas  
- it does not overlap with evaluators  
- it does not duplicate metadata  
- it does not break determinism  
- it integrates cleanly with governance  
- it can be validated by evaluators  
- it can be routed by metadata  
- it preserves naming, namespace, and identity propagation rules  

If any of these conditions fail, the persona is **not allowed**.

Fugue’s strength comes from **strict persona isolation**.  
These rules preserve that strength.

---
