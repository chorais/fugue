# **reconciliation-workflow.md (v2.4)**  
**Reconciliation Workflow**  
Version: 2.4  
Status: Active  
Purpose: Define the deterministic, persona‑isolated reconciliation process for validating implementation against **Initial DECOR**.  
Methodology: Fugue Orchestration Method  
Implementation: Chorais  

---

# 1. Purpose

Reconciliation is the phase where:

- implementation is compared to **Initial DECOR**  
- drift is identified and classified  
- governance posture is validated  
- determinism is validated  
- ticket template fidelity is validated  
- documentation and tests are validated  
- human and Curator clarifications are incorporated  
- corrective action is defined  

Reconciliation determines whether:

- the tranche can close, or  
- further tickets are required  

The **Curator** acts as the governance authority for reconciliation outcomes.

---

# 2. Preconditions

Reconciliation may begin only when:

- all tickets in the tranche are marked complete  
- all tests pass  
- implementation logs are complete  
- clarifications log is complete  
- no open clarifications remain  
- the Conductor has approved ticket completion  

Reconciliation MUST NOT begin mid‑ticket.

---

# 3. Reconciliation Overview

Reconciliation proceeds through the following deterministic phases:

1. **Preparation (Conductor)**  
2. **Structural Comparison (Auditor)**  
3. **Drift Classification (Auditor)**  
4. **Clarification Integration (Conductor ↔ Human Operator ↔ Curator)**  
5. **DECOR Alignment Review (Architect)**  
6. **Reconciliation Log Production (Auditor)**  
7. **Epilogue Ticket Decision (Conductor)**  
8. **Curator Approval (v2.4)**  

Each phase MUST be completed in order.

---

# 4. Phase 1 — Preparation (Conductor Persona)

The Conductor MUST:

- assemble all tranche artefacts  
- ensure logs are complete  
- ensure ticket structure is canonical  
- ensure all tests have passed  
- ensure no clarifications are pending  
- prepare the reconciliation context  

The Conductor MUST NOT modify DECOR or implementation.

---

# 5. Phase 2 — Structural Comparison (Auditor Persona)

The Auditor MUST compare:

- **Initial DECOR** → implementation  
- **Ticket requirements** → implementation  
- **Invariants** → implementation  
- **Governance envelopes** → implementation  
- **Determinism requirements** → implementation  
- **Diagnostics requirements** → implementation  
- **Documentation requirements** → produced documentation  
- **Test requirements** → test suite  
- **Ticket template** → ticket structure  

The Auditor MUST NOT:

- rewrite tickets  
- rewrite DECOR  
- rewrite implementation  
- reinterpret clarifications  

The Auditor MUST classify all findings.

---

## 5.1 Documentation Validation

The Auditor MUST validate that documentation:

- satisfies ticket requirements  
- is stored in the correct folder under `/fugue_docs/`  
- aligns with DECOR invariants  
- aligns with governance envelopes  
- is deterministic and reproducible  
- is complete, unambiguous, and audit‑ready  

Documentation drift MUST be classified accordingly.

---

## 5.2 Replay Trace Validation

The Auditor MUST validate all replay traces:

- inputs  
- outputs  
- evaluator state  
- determinism notes  
- determinism verdict  

A `FAIL` verdict MUST be classified as **determinism drift** and block closure.

---

# 6. Phase 3 — Drift Classification (Auditor Persona)

The Auditor MUST classify drift into:

- **Governance Drift**  
- **Invariant Drift**  
- **Architectural Drift**  
- **Implementation Drift**  
- **Test Drift**  
- **Documentation Drift**  
- **Scope Drift**  
- **Ticket Structure Drift**  
- **Determinism Drift**  
- **Clarification Drift**  
- **Log Drift**  

Each drift MUST be classified as:

- **Critical**  
- **Major**  
- **Minor**  

Critical drift MUST block tranche closure.

---

# 7. Phase 4 — Clarification Integration  
*(Conductor ↔ Human Operator ↔ Curator)*

Clarifications MAY occur during reconciliation.

Clarifications MAY:

- resolve ambiguity  
- correct product intent  
- adjust acceptance criteria  
- adjust scope  
- adjust invariants  
- require new tickets  

Clarifications MUST be:

- interpreted by the Conductor  
- logged  
- applied deterministically  
- validated by the Auditor  

Clarifications MUST NOT:

- alter ticket template structure  
- bypass governance envelopes  
- modify DECOR directly (Architect must do this)  

The **Curator** may provide governance clarifications that override persona interpretations.

---

# 8. Phase 5 — DECOR Alignment Review (Architect Persona)

The Architect MUST:

- review Auditor findings  
- validate structural correctness  
- validate invariant correctness  
- validate governance correctness  
- update DECOR only when drift reveals new truths  
- ensure DECOR remains authoritative  

If DECOR must change, the Architect MUST:

- update `/fugue_docs/decors/<tranche-name>/reconciled-decor.md`  
- document all changes  
- justify changes in the reconciliation log  

---

# 9. Phase 6 — Reconciliation Log Production (Auditor Persona)

The Auditor MUST produce:

```
/fugue_docs/verification/<tranche-name>/reconciliation-log.md
```

The log MUST include:

- summary of findings  
- drift classification  
- determinism validation  
- governance validation  
- DECOR alignment notes  
- ticket template compliance  
- documentation validation  
- test validation  
- recommended corrective actions  
- questions for Conductor / Architect / Implementer  

The log MUST be:

- factual  
- structured  
- deterministic  
- audit‑ready  

---

# 10. Phase 7 — Epilogue Ticket Decision (Conductor Persona)

The Conductor MUST:

- review the reconciliation log  
- determine whether drift requires correction  
- generate an **Epilogue Ticket** if drift exists  
- ensure the epilogue ticket uses the canonical template  
- ensure the epilogue ticket resolves all drift  

If drift exists:

- Implementer MUST implement the epilogue ticket  
- Auditor MUST validate corrections  
- reconciliation MUST repeat until drift is resolved  

If no drift exists:

- proceed to Curator approval  

---

# 11. Phase 8 — Curator Approval (v2.4)

The **Curator** MUST:

- approve reconciliation results  
- validate governance posture  
- validate naming/namespace/identity propagation posture  
- validate evaluator metadata posture  
- validate drift classification  
- validate drift resolution  
- approve readiness for closure  

Curator approval MUST be logged in:

```
/fugue_docs/verification/<tranche-name>/drift/drift-summary.md
```

A tranche MUST NOT proceed to closure without Curator approval.

---

# 12. Governance Requirements

Reconciliation MUST:

- follow persona isolation rules  
- follow canonical templates  
- follow DECOR Specification  
- follow governance posture  
- preserve determinism  
- preserve auditability  

Reconciliation MUST NOT:

- modify DECOR without justification  
- modify tickets  
- modify implementation  
- bypass clarifications  
- weaken governance posture  

---

# 13. Summary

The Reconciliation Workflow ensures:

- implementation aligns with DECOR  
- governance posture is preserved  
- determinism is validated  
- drift is surfaced and corrected  
- clarifications are applied correctly  
- Curator approval is obtained  
- the tranche can close safely  

Reconciliation is the **structural counterpoint** of the Fugue Method.

---
