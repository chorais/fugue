# **tranche-template-contract.md (v2.4)**  
**Tranche Template Contract — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Authority: Governance Contract  
Scope: All Tranches, All Personas, All Lifecycle Phases  
Lifecycle: Intake → Orchestration → Implementation → Verification → Reconciliation → Closure  

---

# 0. Metadata

```yaml
metadata:
  contract-id: "tranche-template-contract"
  version: "2.4"
  authoritative: true

  applies-to:
    - tranche-template
    - all-tranches
    - all-tranche-folders
    - all-lifecycle-phases
    - all-decor-surfaces
    - all-ticket-maps
    - all-governed-documentation
    - all-replay-traces
    - all-logs
    - all-reconciled-artefacts

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

---

# 1. Purpose

The Tranche Template Contract defines the **mandatory structure, metadata, lifecycle alignment, DECOR alignment, governance alignment, and determinism rules** for all tranche‑level templates in the Fugue Orchestration Method.

The tranche template is the **root governance artefact** for a tranche.  
It ensures that every tranche is:

- deterministic  
- persona‑safe  
- lifecycle‑aligned  
- DECOR‑aligned  
- metadata‑aligned  
- identity‑aligned  
- namespace‑aligned  
- evaluator‑aligned  
- documentation‑aligned  
- reconciliation‑ready  

The tranche template MUST NOT:

- introduce new reasoning  
- violate persona boundaries  
- violate governance envelopes  
- violate DECOR  
- violate determinism  
- violate identity propagation  
- violate namespace rules  

---

# 2. Tranche Template Structure (v2.4)

The tranche template MUST contain the following sections:

1. Metadata  
2. Tranche Summary  
3. Mission  
4. Scope  
5. Boundaries  
6. Acceptance Criteria  
7. Lifecycle Alignment  
8. DECOR Surfaces  
9. Architect Fill Phase Requirements  
10. Ticket Map Summary  
11. Dependencies & Sequencing  
12. Documentation Surfaces  
13. Evaluator Surfaces  
14. Determinism Surfaces  
15. Identity & Namespace Surfaces  
16. Risks & Considerations  
17. Clarifications Needed  
18. Change Log  

No section may be removed.  
Sections may be empty only when lifecycle rules allow.

---

# 3. Metadata Rules

The metadata block MUST include:

- tranche ID  
- version  
- status  
- governance envelopes  
- determinism envelope  
- documentation envelope  
- identity propagation contract  
- namespace scheme contract  
- lifecycle contract  
- ticket map contract  
- evaluator contract  
- replay trace contract  
- naming scheme  
- namespace scheme  
- identity propagation  
- persona lineage  
- lifecycle metadata  
- DECOR lineage  
- Ticket Map lineage  
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

# 4. Persona Lineage Rules

The tranche template MUST include:

- initiator identity  
- conductor identity  
- architect identity  
- auditor identity  
- verifier identity  

Persona lineage MUST:

- propagate deterministically  
- preserve identity lineage  
- follow the Identity Propagation Contract  

Persona lineage MUST NOT:

- drift  
- be regenerated  
- be inferred  

---

# 5. Mission Rules

The mission MUST:

- be derived from the Sponsor Preamble  
- be deterministic  
- be governance‑aligned  
- be DECOR‑aligned  

The mission MUST NOT:

- introduce new reasoning  
- reinterpret Sponsor intent  

---

# 6. Scope Rules

Scope MUST include:

- in‑scope items  
- out‑of‑scope items  

Scope MUST:

- be deterministic  
- be governance‑aligned  
- be DECOR‑aligned  

Scope MUST NOT:

- drift  
- contradict DECOR  

---

# 7. Boundaries Rules

Boundaries MUST include:

- structural boundaries  
- architectural boundaries  
- governance boundaries  
- identity boundaries  
- namespace boundaries  

Boundaries MUST:

- be deterministic  
- be DECOR‑aligned  
- be governance‑aligned  

Boundaries MUST NOT:

- contradict DECOR  
- contradict governance envelopes  

---

# 8. Acceptance Criteria Rules

Acceptance criteria MUST include:

- tranche‑level criteria  
- governance criteria  
- determinism criteria  
- documentation criteria  
- identity criteria  
- namespace criteria  

Acceptance criteria MUST be:

- deterministic  
- testable  
- replayable  

Acceptance criteria MUST NOT:

- contain narrative drift  
- contain persona drift  

---

# 9. Lifecycle Alignment Rules

The tranche template MUST include outputs for:

- Phase 1 — Intake  
- Phase 2 — Orchestration  
- Phase 3 — Implementation  
- Phase 4 — Verification  
- Phase 5 — Reconciliation  
- Phase 6 — Closure  

Lifecycle alignment MUST:

- follow the Lifecycle Contract  
- be deterministic  
- be metadata‑aligned  

Lifecycle alignment MUST NOT:

- skip phases  
- merge phases  
- reorder phases  

---

# 10. DECOR Surfaces Rules

The tranche template MUST include:

- design  
- considerations  
- risks  
- opportunities  
- open questions  
- constraints  
- invariants  

DECOR surfaces MUST:

- be extracted deterministically  
- be metadata‑aligned  
- be identity‑aligned  
- be namespace‑aligned  

DECOR surfaces MUST NOT:

- introduce new DECOR  
- reinterpret DECOR  

---

# 11. Architect Fill Phase Rules

The tranche template MUST include:

- whether Fill Phase is required  
- which DECOR surfaces require conceptual output  
- expected conceptual artefacts  
- metadata rules  
- identity propagation rules  
- namespace rules  

Fill Phase MUST:

- follow the Lifecycle Contract  
- follow the DECOR Specification  
- follow the Ticket Map Contract  

Fill Phase MUST NOT:

- introduce new DECOR  
- contradict DECOR  

---

# 12. Ticket Map Summary Rules

The tranche template MUST include:

- total tickets  
- governance tickets  
- implementation tickets  
- architect fill tickets  
- determinism‑critical tickets  
- documentation‑required tickets  

Ticket Map summary MUST:

- follow the Ticket Map Contract  
- be deterministic  
- be metadata‑aligned  

---

# 13. Dependencies & Sequencing Rules

Dependencies MUST include:

- cross‑tranche dependencies  
- governance dependencies  
- determinism dependencies  
- identity dependencies  
- namespace dependencies  

Dependencies MUST:

- be deterministic  
- be acyclic  
- be validated by the Auditor  

Dependencies MUST NOT:

- be inferred  
- be mutated implicitly  

---

# 14. Documentation Surfaces Rules

Documentation surfaces MUST include:

- required surfaces  
- placement rules  
- metadata rules  
- naming rules  
- namespace rules  

Documentation MUST follow the Documentation Envelope Contract.

---

# 15. Evaluator Surfaces Rules

Evaluator surfaces MUST include:

- evaluator categories  
- determinism rules  
- diagnostic rules  

Evaluator surfaces MUST follow the Evaluator Contract.

---

# 16. Determinism Surfaces Rules

Determinism surfaces MUST include:

- ordering rules  
- evaluator behaviour rules  
- metadata propagation rules  
- identity propagation rules  
- replay trace rules  

Determinism surfaces MUST follow the Determinism Envelope.

---

# 17. Identity & Namespace Surfaces Rules

Identity surfaces MUST include:

- identity lineage  
- identity propagation rules  

Namespace surfaces MUST include:

- placement rules  
- namespace invariants  

Identity and namespace MUST follow:

- Identity Propagation Contract  
- Namespace Scheme Contract  

---

# 18. Risks & Considerations Rules

Risks MUST include:

- tranche risks  
- governance risks  
- determinism risks  
- identity risks  
- namespace risks  

Risks MUST NOT:

- contradict DECOR  
- contradict governance envelopes  

---

# 19. Clarifications Rules

Clarifications MUST include:

- sponsor clarifications  
- architect clarifications  
- governance clarifications  
- DECOR clarifications  

Clarifications MUST NOT:

- introduce new DECOR  
- introduce new governance rules  

---

# 20. Change Log Rules

The change log MUST:

- record all changes  
- include persona identity  
- include date  
- include version  

The change log MUST NOT:

- be rewritten  
- be collapsed  

---
