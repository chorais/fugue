# **documentation-envelope-contract.md (v2.4)**  
**Documentation Envelope Contract — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Authority: Governance Contract  
Scope: All Governed Documentation  
Lifecycle: Global (All Phases)  

---

# 0. Metadata

```yaml
metadata:
  contract-id: "documentation-envelope-contract"
  version: "2.4"
  authoritative: true

  applies-to:
    - all-governed-documentation
    - all-personas
    - all-tranches
    - all-lifecycle-phases
    - all-ticket-maps
    - all-tickets
    - all-decor-surfaces
    - all-logs
    - all-replay-traces

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  governance-envelope: "<id>"
  determinism-envelope: "<id>"
  documentation-envelope: "<self>"
  decor-contract: "<id>"
  lifecycle-contract: "<id>"
  ticket-map-contract: "<id>"
  ticket-template: "<id>"
```

# Placeholder Semantics
# Fields containing "<id>" or "<self>" are canonical placeholders.
# They MUST be concretised in project/branch/theme/tranche governance envelopes.
# They MUST NOT be replaced in methodology-level contracts.
# The Auditor Persona MUST treat these placeholders as intentional and NOT as metadata drift.

---

# 1. Purpose

The Documentation Envelope defines the **governance, determinism, persona‑scoped, metadata‑aligned, and lifecycle‑aligned rules** for documentation creation, validation, correction, and storage within the Fugue Orchestration Method.

Documentation is a **governed artefact**, not an implementation detail.

Documentation MUST be:

- deterministic  
- persona‑scoped  
- DECOR‑aligned  
- metadata‑aligned  
- governance‑aligned  
- reproducible  
- audit‑ready  
- replayable  
- lifecycle‑aligned  
- substrate‑agnostic  

Documentation MUST integrate with:

- DECOR metadata  
- Ticket Template (v2.4)  
- Ticket Map Contract (v2.4)  
- Reconciled DECOR  
- Determinism Envelope  
- Identity Propagation Contract  
- Auditor drift classification  
- Verifier validation  

Documentation MUST NOT:

- redefine DECOR  
- weaken invariants  
- violate persona boundaries  
- bypass governance envelopes  
- be stored outside governed namespaces  
- be created without a ticket  
- depend on conversational context  

---

# 2. Documentation Principles

Documentation MUST be:

- deterministic and reproducible  
- complete and unambiguous  
- persona‑scoped  
- stored in the correct namespace  
- aligned with DECOR invariants and governance envelopes  
- aligned with Ticket Map metadata  
- validated by the Auditor  
- validated by the Verifier during reconciliation  
- reconstructable from governed artefacts  
- metadata‑preserving  
- identity‑preserving  
- naming‑aligned  
- namespace‑aligned  

Documentation MUST NOT:

- override DECOR  
- embed DECOR  
- weaken invariants  
- bypass governance envelopes  
- be embedded inside tickets, DECOR, or logs  
- be stored outside `/fugue_docs/`  
- be created without a ticket  
- violate persona boundaries  

Documentation is a **first‑class governed artefact**.

---

# 3. Documentation Namespaces and Governance Boundaries

Fugue v2.4 recognises **three documentation namespaces**.

## 3.1 `/fugue_docs` — Governed Documentation (Methodology‑Level)

Contains all governed artefacts produced by Fugue personas:

/fugue_docs contains all governed documentation across all layers:

- project-level governed documentation
- branch-level governed documentation
- theme-level governed documentation
- tranche-level governed documentation
- ticket-level governed documentation
- DECORs (all forms)
- logs, traces, verification, closure
- architecture artefacts
- concerns

All content under `/fugue_docs` MUST comply with this envelope.

## 3.2 `/docs` — Developer Documentation (Protected, Not Governed)

Contains implementation‑level documentation:

- design docs  
- diagrams  
- developer guides  
- exploratory notes  

Governance MUST NOT enforce structure here.

## 3.3 `/public-docs` — User‑Facing Documentation (Protected, Not Governed)

Contains externally‑oriented documentation:

- HOW‑TOs  
- guides  
- tutorials  
- onboarding materials  

Governance MUST NOT enforce structure here.


## **3.4 Project / Branch / Theme Governed Namespaces (v2.4 Update)**

Fugue v2.4 introduces three additional governed documentation namespaces:

### **3.4.1 `/fugue_docs/project/` — Project‑Level Governed Documentation**

Contains:

- project preamble  
- project DECOR  
- project governance envelope  
- naming + namespace roots  
- persona map  
- identity propagation rules  
- documentation envelope  
- bootstrap log  

All artefacts under `/fugue_docs/project/` are **fully governed** and MUST comply with:

- Naming Scheme Contract  
- Namespace Scheme Contract  
- Identity Propagation Contract  
- Governance Envelope  
- Determinism Envelope  

---

### **3.4.2 `/fugue_docs/branches/<branch-name>/` — Branch‑Level Governed Documentation**

Contains:

- branch preamble  
- branch DECOR  
- branch governance envelope  
- branch naming + namespace schemes  
- branch identity propagation rules  
- branch documentation envelope  
- branch bootstrap log  

All artefacts under `/fugue_docs/branches/` are **fully governed** and MUST comply with:

- project‑level governance  
- branch‑level governance  
- naming + namespace rules  
- identity propagation rules  

---

### **3.4.3 `/fugue_docs/themes/<theme-name>/` — Theme‑Level Governed Documentation**

Contains:

- theme preamble  
- theme DECOR  
- theme governance envelope  
- theme naming + namespace schemes  
- theme identity propagation rules  
- theme documentation envelope  
- theme bootstrap log  

All artefacts under `/fugue_docs/themes/` are **fully governed** and MUST comply with:

- project‑level governance  
- branch‑level governance  
- theme‑level governance  
- naming + namespace rules  
- identity propagation rules  


---

# 4. Persona‑Scoped Documentation Ownership

Documentation MUST be authored only by the persona responsible for that documentation type.

### 4.1 Conceptual Personas  
- Curator → governance documentation  
- Conductor (Conceptual) → conceptual orchestration documentation  
- Methodologist → methodology drafts, templates, lifecycle artefacts  
- Architect → DECOR, invariants, conceptual models  

### 4.2 Practical Personas  
- Initiator → bootstrap documentation  
- Orchestrator → Ticket Map documentation, governance metadata  
- Implementer → implementation documentation, logs, traces  
- Auditor → validation notes, drift classification  
- Verifier → final validation notes, closure readiness  

No persona may author documentation outside its scope.

---

# 5. Documentation Storage Rules

Documentation MUST:

- be stored in the correct namespace  
- follow naming‑scheme rules  
- follow namespace‑scheme rules  
- include required metadata  
- preserve identity lineage  
- preserve metadata lineage  
- preserve evaluator metadata  
- preserve determinism metadata  
- project-level documentation MUST be stored under `/fugue_docs/project/`
- branch-level documentation MUST be stored under `/fugue_docs/branches/<branch-name>/`
- theme-level documentation MUST be stored under `/fugue_docs/themes/<theme-name>/`

Documentation MUST NOT:

- be stored outside governed namespaces  
- be embedded inside tickets  
- be embedded inside DECOR  
- be embedded inside logs  
- be stored in persona‑unsafe locations 
- MUST NOT store project, branch, or theme documentation in tranche-level namespaces

---

# 6. Documentation Requirements in Tickets

Tickets MUST include a **Documentation Requirements** section when documentation is required.

Documentation Requirements MUST:

- list documentation paths  
- specify the responsible persona  
- specify the required format (ADR, diagram, spec, etc.)  
- specify acceptance criteria  
- propagate DECOR metadata  
- propagate Ticket Map metadata  
- propagate naming/namespace/identity metadata  
- propagate evaluator metadata requirements  

Documentation MUST NOT:

- be embedded in the ticket  
- be assigned to the wrong persona  
- be omitted when required  

### Concerns  
If a ticket surfaces a forward concern, the Implementer MUST create:

```
/fugue_docs/concerns/DC-<number>.md
```

The ticket MUST reference the Concern ID.

---

# 7. Documentation Flow Across the Lifecycle

Documentation MUST propagate:

- naming  
- namespaces  
- identity lineage  
- metadata  
- evaluator metadata  
- determinism metadata  

across all lifecycle transitions.

Documentation MUST be updated only through:

- tickets  
- DECOR updates  
- reconciliation workflows  

Documentation MUST NOT be mutated implicitly.

---

# 8. Governed Artefact Rules

Governed artefacts MUST:

- preserve identity lineage  
- preserve metadata lineage  
- preserve naming and namespace lineage  
- preserve evaluator metadata lineage  
- preserve determinism lineage  

Governed artefacts MUST NOT:

- be modified outside persona boundaries  
- be modified without a ticket  
- be modified outside governed namespaces  

---

# 9. Documentation Drift Classification

Documentation drift MUST include:

- naming drift  
- namespace drift  
- identity propagation drift  
- evaluator metadata drift  
- determinism metadata drift  
- missing documentation  
- incorrect documentation  
- incomplete documentation  

Drift MUST be classified by the Auditor and validated by the Verifier.

---

# 10. Documentation Correction (Epilogue Workflow)

Documentation corrections MUST include:

- reconciliation lineage  
- metadata lineage  
- identity lineage  
- evaluator metadata lineage  
- determinism lineage  

Corrections MUST follow:

- Ticket Map Contract  
- Lifecycle Contract  
- Governance Envelope  
- Determinism Envelope  

Corrections MUST NOT be made manually.

---

# 11. Documentation and DECOR

Documentation MUST align with:

- DECOR  
- DECOR updates  
- Reconciled DECOR  
- DECOR invariants  
- DECOR constraints  
- DECOR metadata  

Documentation MUST NOT:

- redefine DECOR  
- embed DECOR  
- override DECOR  
- weaken invariants  

Documentation MUST reference DECOR surfaces explicitly when required.

---

# 12. Documentation Determinism

Documentation MUST be:

- reproducible  
- structured  
- stable  
- audit‑ready  
- free of ambiguity  
- free of narrative drift  
- free of persona drift  
- metadata‑preserving  
- identity‑preserving  

Documentation determinism MUST include:

```yaml
determinism-schema:
  ordering:
    - "Documentation MUST follow deterministic ordering rules"
  evaluator:
    - "Documentation MUST include evaluator metadata when required"
  replay:
    - "Documentation MUST support deterministic replay traces"
  metadata:
    - "Documentation MUST preserve metadata lineage"
  identity:
    - "Documentation MUST preserve identity lineage"
```

Documentation MUST NOT depend on:

- conversational context  
- implicit memory  
- inferred state  

Documentation MUST be reconstructable from:

- tickets  
- DECOR  
- tranche logs  
- implementation logs  

---
