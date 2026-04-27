# **ticket-template-contract.md (v2.4)**  
**Ticket Template Contract — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Authority: Governance Contract  
Scope: All Tickets, All Tranches, All Personas  
Lifecycle: Orchestration → Implementation → Verification → Reconciliation  

---

# 0. Metadata

```yaml
metadata:
  contract-id: "ticket-template-contract"
  version: "2.4"
  authoritative: true

  applies-to:
    - ticket-template
    - all-tickets
    - all-ticket-maps
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
  ticket-map-contract: "<id>"
  evaluator-contract: "<id>"
  replay-trace-contract: "<id>"
```

# Placeholder Semantics
# Fields containing "<id>" or "<self>" are canonical placeholders.
# They MUST be concretised in project/branch/theme/tranche governance envelopes.
# They MUST NOT be replaced in methodology-level contracts.
# The Auditor Persona MUST treat these placeholders as intentional and NOT as metadata drift.

---

# 1. Purpose

The Ticket Template Contract defines the **mandatory structure, metadata, persona routing, determinism rules, identity rules, namespace rules, evaluator rules, documentation rules, and lifecycle rules** for all tickets in the Fugue Orchestration Method.

The ticket template is the **canonical governed interface** between:

- Conductor → Implementer  
- Conductor → Architect  
- Implementer → Auditor  
- Auditor → Verifier  

It ensures that every ticket is:

- deterministic  
- persona‑safe  
- DECOR‑aligned  
- metadata‑aligned  
- identity‑aligned  
- namespace‑aligned  
- evaluator‑aligned  
- documentation‑aligned  
- lifecycle‑aligned  
- replayable  

Tickets MUST NOT:

- introduce new reasoning  
- violate persona boundaries  
- violate governance envelopes  
- violate DECOR  
- violate determinism  
- violate identity propagation  
- violate namespace rules  

---

# 2. Ticket Template Structure (v2.4)

The ticket template MUST contain the following sections:

1. Metadata  
2. Ticket Summary  
3. Intent  
4. DECOR Subset  
5. Acceptance Criteria  
6. Implementation Requirements  
7. Conceptual Requirements  
8. Documentation Requirements  
9. Evaluator Metadata  
10. Dependencies  
11. Clarifications Needed  
12. Implementation Notes  
13. Architect Notes  
14. Auditor Notes  
15. Change Log  

No section may be removed.  
Sections may be empty only when persona routing or lifecycle rules allow.

---

# 3. Metadata Rules

The metadata block MUST include:

- ticket ID  
- tranche ID  
- DECOR lineage  
- persona routing  
- governance envelopes  
- determinism envelope  
- documentation envelope  
- identity propagation contract  
- namespace scheme contract  
- evaluator contract  
- replay trace contract  
- lifecycle metadata  
- dependencies  
- status  
- last‑updated  

Metadata MUST be:

- complete  
- deterministic  
- identity‑aligned  
- namespace‑aligned  
- governance‑aligned  

Metadata MUST NOT:

- be omitted  
- be mutated implicitly  
- be inferred  

---

# 4. Persona Routing Rules

Persona routing MUST be one of:

- `implementer`  
- `architect`  

Hybrid routing is **forbidden** in v2.4.

Persona routing MUST:

- be deterministic  
- be DECOR‑aligned  
- be metadata‑aligned  
- be validated by the Auditor  
- be preserved across the lifecycle  

Persona routing MUST NOT:

- change implicitly  
- be inferred  
- violate persona boundaries  

---

# 5. DECOR Subset Rules

Each ticket MUST include:

- design references  
- considerations  
- risks  
- opportunities  
- open questions  
- constraints  
- invariants  

DECOR subsets MUST:

- be extracted deterministically  
- be metadata‑aligned  
- be identity‑aligned  
- be namespace‑aligned  

DECOR subsets MUST NOT:

- introduce new DECOR  
- reinterpret DECOR  
- omit required DECOR surfaces  

---

# 6. Acceptance Criteria Rules

Acceptance criteria MUST include:

- required criteria  
- determinism criteria  
- evaluator behaviour criteria  
- replay trace requirements  

Acceptance criteria MUST be:

- deterministic  
- testable  
- replayable  
- identity‑aligned  
- metadata‑aligned  

Acceptance criteria MUST NOT:

- contain narrative drift  
- contain persona drift  

---

# 7. Implementation Requirements Rules

Implementation requirements MUST appear when:

- persona‑routing = implementer  

They MUST include:

- behaviour  
- state transitions  
- outputs  
- logs  
- replay traces  
- metadata propagation  
- identity propagation  
- naming rules  
- namespace rules  

Implementation requirements MUST NOT:

- include conceptual reasoning  
- include DECOR derivation  

---

# 8. Conceptual Requirements Rules

Conceptual requirements MUST appear when:

- persona‑routing = architect  
- OR requires‑fill = true  

They MUST include:

- invariants  
- constraints  
- governance envelopes  
- identity propagation rules  
- naming rules  
- namespace rules  
- documentation envelope rules  
- determinism envelope rules  

Conceptual requirements MUST NOT:

- include implementation detail  
- include evaluator behaviour  

---

# 9. Documentation Requirements Rules

Documentation requirements MUST include:

- required surfaces  
- placement rules  
- metadata rules  
- naming rules  
- namespace rules  
- evaluator documentation rules  

Documentation requirements MUST follow the Documentation Envelope Contract.

Documentation MUST NOT:

- be embedded in the ticket  
- be stored outside governed namespaces  

---

# 10. Evaluator Metadata Rules

Evaluator metadata MUST include:

- evaluator categories  
- evaluator diagnostics  
- evaluator determinism rules  

Evaluator metadata MUST follow the Evaluator Contract.

Evaluator metadata MUST NOT:

- be omitted  
- be inferred  

---

# 11. Dependency Rules

Dependencies MUST include:

- explicit dependencies  
- transitive dependencies  
- governance dependencies  
- determinism dependencies  
- identity propagation dependencies  

Dependencies MUST:

- be deterministic  
- be acyclic  
- be validated by the Auditor  

Dependencies MUST NOT:

- be inferred  
- be mutated implicitly  

---

# 12. Clarifications Rules

Clarifications MUST include:

- general clarifications  
- DECOR clarifications  
- governance clarifications  

Clarifications MUST NOT:

- introduce new DECOR  
- introduce new governance rules  

---

# 13. Implementation Notes Rules

Implementation notes MUST include:

- logs  
- replay traces  
- surfaced contradictions  
- metadata propagation notes  
- identity propagation notes  

Implementation notes MUST NOT:

- modify DECOR  
- modify metadata  
- modify identity  

---

# 14. Architect Notes Rules

Architect notes MUST include:

- conceptual output  
- DECOR updates  
- identity updates  
- governance envelope updates  

Architect notes MUST NOT:

- introduce new DECOR surfaces  
- contradict DECOR  

---

# 15. Auditor Notes Rules

Auditor notes MUST include:

- drift  
- naming/namespace/identity drift  
- evaluator drift  
- reconciliation notes  
- validated surfaces  

Auditor notes MUST NOT:

- reinterpret drift  
- introduce new drift  

---

# 16. Change Log Rules

The change log MUST:

- record all changes  
- include persona identity  
- include date  
- include version  

The change log MUST NOT:

- be rewritten  
- be collapsed  

---