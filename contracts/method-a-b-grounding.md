# **Method A/B Grounding Contract (v2.4)**  
Version: 2.4  
Status: Active  
Methodology: Fugue Orchestration Method v2.4  
Governance Authority: Curator  

---

# 1. Purpose  

The Method A/B Grounding Contract defines the two valid grounding strategies for DECOR formalisation and tranche bootstrap within the Fugue Orchestration Method.

It ensures that:

- DECOR grounding is deterministic  
- bootstrap sequencing is predictable  
- persona responsibilities are unambiguous  
- Ticket Map creation is consistent  
- Implementer ingress analysis is correctly applied  
- naming, namespace, and identity propagation rules are enforced  
- reconciliation remains stable regardless of grounding strategy  

This contract is binding for all tranches.

---

# 2. Overview of Grounding Strategies  

Fugue supports two grounding strategies:

- **Method A — Product Grounding**  
- **Method B — Technical Grounding**

Both methods produce:

- canonical DECOR  
- a governed Ticket Map  
- deterministic Ticket Loop execution  
- Reconciled DECOR at tranche close  

The difference lies in **how DECOR is derived** and **when ingress analysis occurs**.

---

# 3. Method A — Product Grounding  

## 3.1 Definition  
Method A grounds DECOR in **product intent**.

The Curator provides:

- tranche preamble  
- tranche mission and boundaries  
- tranche acceptance criteria  
- governance posture  
- product requirements  
- domain constraints  
- business context  

The Architect formalises DECOR directly from this product grounding.

## 3.2 Sequence  
1. Conductor interprets the preamble produced by the Curator  
2. Architect formalises DECOR  
3. Conductor generates the Ticket Map  
4. Ticket Loop begins  
5. DECOR updates occur as needed  
6. Reconciliation produces Reconciled DECOR  

## 3.3 Implementer Role  
- ingress analysis is **optional**  
- Implementer focuses on feasibility and contradictions  
- Implementer does not influence DECOR derivation  

## 3.4 When to Use Method A  
Method A is appropriate when:

- product intent is clear  
- architecture is greenfield or well‑understood  
- the tranche is primarily product‑driven  
- structural uncertainty is low  

---

# 4. Method B — Technical Grounding  

## 4.1 Definition  
Method B grounds DECOR in **technical evidence** extracted from the existing codebase.

The Implementer acts as a **Technical Lead Ingress Probe**, producing:

- invariants  
- constraints  
- architectural surfaces  
- risks and opportunities  
- feasibility boundaries  
- naming and namespace observations  
- identity propagation observations  

The Architect formalises DECOR from this evidence.

## 4.2 Sequence  
1. Conductor interprets the preamble produced by the Curator  
2. Implementer produces ingress analysis  
3. Architect formalises DECOR from evidence  
4. Conductor generates the Ticket Map  
5. Ticket Loop begins  
6. DECOR updates occur as needed  
7. Reconciliation produces Reconciled DECOR  

## 4.3 Implementer Role  
- ingress analysis is **mandatory**  
- Implementer provides primary architectural evidence  
- Implementer does not derive DECOR  

## 4.4 When to Use Method B  
Method B is appropriate when:

- architecture already exists  
- system behaviour must be discovered  
- invariants must be extracted from code  
- naming and namespace rules must be validated  
- identity propagation must be understood  
- structural uncertainty is high  
- the tranche is architecture‑driven  

---

# 5. DECOR Grounding Rules  

## 5.1 Canonical DECOR  
Regardless of method:

- only the Architect may formalise DECOR  
- Implementer ingress analysis is evidence, not authority  
- Conductor routes DECOR but does not modify it  
- Auditor validates DECOR but does not derive it  
- DECOR MUST follow naming, namespace, and identity propagation rules  

## 5.2 DECOR Timing  
- Method A: DECOR formalised **before** ingress analysis (if any)  
- Method B: DECOR formalised **after** ingress analysis  

## 5.3 DECOR Updates  
Both methods require governed DECOR updates during the Ticket Loop.

DECOR updates MUST:

- preserve metadata  
- preserve naming  
- preserve namespaces  
- preserve identity propagation  
- be formalised by the Architect  
- be stored under governed namespaces  

---

# 6. Ticket Map Grounding Rules  

## 6.1 Method A  
- Ticket Map is product‑first  
- DECOR is already formalised  
- ingress analysis is optional  

## 6.2 Method B  
- Ticket Map is architecture‑first  
- ingress analysis informs ticket boundaries  
- DECOR is formalised from evidence  

## 6.3 Common Rules  
Regardless of method:

- Ticket Map MUST reference DECOR categories  
- Ticket Map MUST be deterministic  
- Ticket Map MUST be governed  
- Ticket Map MUST follow naming‑scheme contract  
- Ticket Map MUST follow namespace rules  
- Ticket Map MUST follow identity propagation rules  
- Ticket Map MUST be validated by the Auditor  

---

# 7. Documentation Envelope Integration  

## 7.1 Method A  
Architectural documentation precedes implementation documentation.

## 7.2 Method B  
Ingress analysis produces implementation‑level evidence before DECOR.

## 7.3 Common Rules  
All documentation MUST:

- be persona‑scoped  
- be stored under `/fugue_docs`  
- be validated by the Auditor  
- support DECOR  
- follow naming and namespace rules  
- preserve identity propagation  

---

# 8. Reconciliation Alignment  

Regardless of grounding strategy:

- Auditor validates implementation against DECOR  
- Auditor validates naming and namespace correctness  
- Auditor validates identity propagation correctness  
- Auditor classifies drift  
- Architect resolves structural inconsistencies  
- Conductor issues epilogue tickets  
- Implementer executes corrections  
- Auditor produces Reconciled DECOR  

Reconciliation is identical for both methods.

---

# 9. Grounding Invariants  

The following MUST always hold:

- DECOR is the single semantic anchor  
- only the Architect may formalise DECOR  
- Implementer ingress analysis is non‑canonical  
- Ticket Map MUST be DECOR‑aligned  
- Ticket Map MUST declare Method A or Method B  
- grounding method MUST NOT change mid‑tranche  
- naming, namespace, and identity propagation rules MUST be preserved  
- Reconciled DECOR is the final governed artefact  

These invariants ensure deterministic, auditable grounding.
