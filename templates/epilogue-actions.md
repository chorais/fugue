# **epilogue-actions.md (v2.4)**  
**Epilogue Actions Log — Tranche `<tranche-name>`**  
Version: 2.4  
Personas: Orchestrator, Architect, Implementer, Auditor, Verifier  
Mode: Epilogue Workflow  
Lifecycle Context: Phase 4 (Verification) → Phase 5 (Closure)  

---

# 0. Metadata

```yaml
metadata:
  tranche-name: "<tranche-name>"

  orchestrator: "<system-identity>"
  architect: "<system-identity>"
  implementer: "<system-identity>"
  auditor: "<system-identity>"
  verifier: "<system-identity>"

  persona-routing-summary: "Orchestrator|Architect|Implementer|Auditor|Verifier"

  # Updated namespace references
  epilogue-ticket-bundle-source: "/fugue_docs/tickets/<tranche-name>/epilogue/"
  reconciled-decor-target: "/fugue_docs/decors/<tranche-name>/reconciled-decor.md"

  governance-posture: "<imported-from-preamble>"
  identity-propagation-rules: "<imported-from-preamble>"

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  governance-envelope: "<id>"
  evaluator-categories: []
  evaluator-diagnostics: []

  lifecycle-context: "verification→closure"
  epilogue-status: "Draft|Active|Complete"

  last-updated: "<YYYY-MM-DD>"
```

---

# 1. Epilogue Inputs  
Record the governed artefacts consumed during the epilogue workflow.

### 1.1 Required Inputs  
- Auditor drift classification  
- Architect reconciliation notes  
- updated DECOR surfaces  
- updated metadata  
- updated documentation  
- updated implementation logs  
- updated replay traces  
- governance posture  
- identity propagation rules  
- naming/namespace posture  

### 1.2 Optional Inputs  
- prior epilogue logs  

The Orchestrator MUST NOT modify any inputs.

---

# 1.3 Schema Alignment Checks (Updated)

The Orchestrator MUST validate:

- DECOR conforms to `/schemas/decor-schema.json`  
- Ticket metadata conforms to the Ticket Template (v2.4)  
- documentation conforms to the Documentation Envelope Contract (v2.4)  
- replay traces conform to the Replay Trace Contract (v2.4)  
- determinism surfaces conform to the Determinism Envelope Contract (v2.4)  
- naming/namespace/identity propagation posture is present  
- evaluator metadata surfaces are present  

If validation fails, the Orchestrator MUST classify the failure as **metadata drift** or **governance drift**.

---

# 2. Epilogue Ticket Dispatch (Orchestrator)  
The Orchestrator MUST:

- generate epilogue tickets  
- route tickets to the correct persona  
- propagate metadata  
- propagate documentation requirements  
- propagate determinism requirements  
- propagate naming/namespace/identity propagation rules  
- propagate evaluator metadata requirements  
- ensure persona isolation  

Each dispatched ticket MUST include:

- ticket ID  
- drift reference  
- DECOR reference  
- metadata reference  
- documentation requirements  
- determinism requirements  
- naming/namespace/identity propagation requirements  
- evaluator metadata requirements  
- acceptance criteria  

Record:

- ticket IDs  
- responsible personas  
- dispatch timestamps  

---

# 3. Structural Corrections (Architect)  
The Architect MUST perform structural corrections for:

- DECOR inconsistencies  
- invariant violations  
- metadata inconsistencies  
- governance envelope violations  
- identity propagation inconsistencies  
- naming/namespace inconsistencies  

Architect corrections MUST include:

- updated DECOR surfaces  
- updated metadata  
- updated governance envelopes  
- updated naming/namespace/identity propagation metadata  

Record:

- corrected DECOR surfaces  
- corrected metadata  
- corrected governance envelopes  
- corrected naming/namespace/identity propagation metadata  
- structural reasoning notes (conceptual only)  

The Architect MUST NOT:

- implement code  
- modify tests  
- modify runtime behaviour  

---

# 4. Implementation Corrections (Implementer)  
The Implementer MUST execute epilogue tickets requiring:

- code corrections  
- test corrections  
- determinism corrections  
- documentation corrections  
- replay trace corrections  
- naming/namespace/identity propagation corrections  
- evaluator metadata corrections  

Record:

- code artefacts created or modified  
- test artefacts created or modified  
- documentation artefacts created or modified  
- replay traces created or modified  
- determinism guarantees implemented  
- naming/namespace/identity propagation guarantees implemented  
- evaluator metadata guarantees implemented  

The Implementer MUST NOT:

- modify DECOR  
- modify metadata  
- modify governance envelopes  

---

# 5. Auditor Validation (Post‑Correction)  
The Auditor MUST validate:

- drift resolution completeness  
- DECOR alignment  
- metadata alignment  
- documentation alignment  
- implementation alignment  
- determinism alignment  
- naming/namespace/identity propagation alignment  
- evaluator metadata alignment  

Record:

- validation results  
- unresolved drift (if any)  
- artefacts requiring further correction  

The Auditor MUST NOT:

- modify artefacts  
- generate new drift classifications  

---

# 6. Verifier Validation (Final Epilogue Check)  
The Verifier MUST validate:

- all corrections are complete  
- all corrections are aligned with governance  
- all corrections are aligned with DECOR  
- all corrections are aligned with metadata  
- all corrections satisfy acceptance criteria  
- all corrections align with naming/namespace/identity propagation rules  
- all corrections align with determinism envelope  
- all corrections align with evaluator metadata schema  

Record:

- validation results  
- final correction completeness  
- readiness for tranche closure  

The Verifier MUST NOT modify artefacts.

---

# 7. Epilogue Completion  
Record:

- all epilogue tickets executed  
- all corrections validated  
- all drift resolved  
- reconciled DECOR ready for closure  
- reconciled documentation ready for closure  
- reconciled metadata ready for closure  
- reconciled evaluator metadata ready for closure  
- reconciled naming/namespace/identity propagation metadata ready for closure  

Epilogue MUST be marked **Complete** only when:

- Auditor validation passes  
- Verifier validation passes  
- no unresolved drift remains  

---

# 8. Handoff to Closure  
Record the artefacts handed off to the Conductor and Curator:

- reconciled DECOR  
- reconciled documentation  
- reconciled metadata  
- reconciled logs  
- reconciled replay traces  
- reconciled naming/namespace/identity propagation metadata  
- reconciled evaluator metadata  
- epilogue log (this file)  
- verification outcome  

This begins **Phase 5 — Closure**.

---
