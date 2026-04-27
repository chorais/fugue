# **epilogue-workflow.md (v2.4)**  
**Epilogue Workflow**  
Version: 2.4  
Status: Active  
Purpose: Define the deterministic, persona‑isolated process for correcting drift and finalising a tranche.  
Methodology: Fugue Orchestration Method  
Implementation: Chorais  

---

# 1. Purpose

The Epilogue Workflow ensures that:

- all drift identified during reconciliation is corrected  
- documentation drift is resolved  
- corrected documentation is validated  
- DECOR is updated if required  
- governance posture is preserved  
- determinism is restored  
- the tranche can close safely and reproducibly  

The epilogue is the **final corrective pass** before tranche closure.

The **Curator** acts as the governance authority for epilogue approval.

---

# 2. Preconditions

The Epilogue Workflow may begin only when:

- reconciliation is complete  
- the reconciliation log is finalised  
- the Conductor has reviewed all drift classifications  
- the **Curator** has approved reconciliation results  
- the human sponsor has approved reconciliation results  

The epilogue MUST NOT begin before reconciliation is complete.

---

# 3. Epilogue Overview

The epilogue proceeds through the following deterministic phases:

1. **Epilogue Ticket Generation (Conductor)**  
2. **Epilogue Ticket Implementation (Implementer / Architect)**  
3. **Documentation Corrections (Architect / Implementer)**  
4. **Validation of Corrections (Auditor)**  
5. **Reconciled DECOR Update (Architect)**  
6. **Epilogue Log Update (Conductor)**  
7. **Tranche Closure Decision (Conductor + Curator + Human Operator)**  

Each phase MUST be completed in order.

---

# 4. Phase 1 — Epilogue Ticket Generation (Conductor Persona)

The Conductor MUST:

- review the reconciliation log  
- identify all drift requiring correction  
- generate a single **Epilogue Ticket** using the canonical v2.4 ticket template  
- ensure the ticket is atomic, unambiguous, and deterministic  
- ensure all drift categories are addressed  

The Conductor MUST NOT:

- modify DECOR  
- modify implementation  
- correct drift directly  

The epilogue ticket MUST include:

- governance drift  
- invariant drift  
- architectural drift  
- implementation drift  
- test drift  
- documentation drift  
- determinism drift  
- clarification drift  
- ticket structure drift  

All drift MUST be corrected within the epilogue ticket.

---

# 5. Phase 2 — Epilogue Ticket Implementation (Implementer Persona)

The Implementer MUST:

- implement the epilogue ticket exactly as written  
- correct implementation drift  
- correct test drift  
- correct determinism drift  
- update the implementation log  

The Implementer MUST NOT:

- modify DECOR  
- correct architectural documentation  
- reinterpret governance envelopes  
- expand scope beyond the epilogue ticket  

If the epilogue ticket is unclear or infeasible, the Implementer MUST request clarification.

---

# 6. Phase 3 — Documentation Corrections (Architect / Implementer)

If documentation drift was identified during reconciliation, the Conductor MUST route documentation corrections to the correct persona.

### 6.1 Persona‑Scoped Documentation Responsibilities

**Architect MUST correct:**

- ADRs  
- architecture diagrams  
- design specifications  
- governance drafts  
- canonical models  

**Implementer MUST correct:**

- runtime diagrams  
- integration notes  
- test documentation  
- developer‑facing behaviour notes  
- determinism‑related notes  

### 6.2 Documentation Correction Rules

All corrected documentation MUST:

- satisfy ticket requirements  
- be deterministic  
- be complete and unambiguous  
- align with DECOR invariants  
- align with governance envelopes  
- be stored in the correct folder under `/fugue_docs/`  

Personas MUST NOT correct documentation outside their scope.

---

# 7. Phase 4 — Validation of Corrections (Auditor Persona)

The Auditor MUST validate:

- implementation corrections  
- test corrections  
- documentation corrections  
- determinism corrections  
- governance alignment  
- invariant alignment  
- ticket template fidelity  

### 7.1 Documentation Validation

The Auditor MUST ensure that corrected documentation:

- resolves all documentation drift  
- satisfies all ticket requirements  
- aligns with DECOR and governance posture  
- is deterministic and reproducible  
- is stored in the correct folder  
- is complete and audit‑ready  

### 7.2 Replay Trace Validation

The Auditor MUST validate that all replay traces produced in the epilogue ticket:

- document all correction inputs  
- document all correction outputs  
- record final evaluator state  
- include determinism notes  
- conclude with a `PASS` determinism verdict  

A `FAIL` or `CONDITIONAL` verdict MUST block tranche closure.

---

# 8. Phase 5 — Reconciled DECOR Update (Architect Persona)

If reconciliation or epilogue corrections reveal new architectural truths, the Architect MUST:

- update:

```
/fugue_docs/decors/<tranche-name>/reconciled-decor.md
```

- document all changes  
- justify changes in the epilogue log  
- ensure invariants remain stable  
- ensure governance posture remains intact  

The Architect MUST NOT:

- weaken invariants  
- reinterpret clarifications  
- modify DECOR arbitrarily  

Reconciled DECOR becomes the authoritative input to the next tranche.

---

# 9. Phase 6 — Epilogue Log Update (Conductor Persona)

The Conductor MUST update:

```
/fugue_docs/closure/<tranche-name>/closure-report.md
```

The log MUST include:

- summary of drift corrected  
- documentation corrections  
- DECOR updates  
- determinism corrections  
- governance corrections  
- Auditor validation results  
- any remaining risks or follow‑ups  

### 9.1 Conductor Log Correction Rule

If the Auditor identifies **log drift**, the Conductor MUST:

- correct logs directly  
- record what was corrected and why  
- request Auditor re‑validation  

The Conductor MUST NOT delegate log corrections.

The log MUST be:

- factual  
- structured  
- deterministic  
- audit‑ready  

---

# 10. Phase 7 — Tranche Closure Decision

A tranche may close only when:

- all drift is corrected  
- all documentation drift is resolved  
- all documentation is validated  
- reconciled DECOR is complete  
- all tests pass  
- governance posture is stable  
- determinism is preserved  
- **Curator approves closure**  
- human sponsor approves closure  

The Conductor MUST NOT close a tranche early.

---

# 11. Summary

The Epilogue Workflow ensures:

- all drift is corrected  
- documentation is complete and validated  
- DECOR is updated deterministically  
- governance posture is preserved  
- Curator approval is obtained  
- the tranche closes safely and reproducibly  

The epilogue is the **final structural correction** before the next tranche begins.

---
