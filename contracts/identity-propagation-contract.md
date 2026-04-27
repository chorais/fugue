# **identity-propagation-contract.md (v2.4 — Hierarchy‑Complete)**  
**Identity Propagation Contract — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Authority: Governance Contract  
Scope: All Personas, All Artefacts, All Lifecycle Phases  
Lifecycle: Global (Methodology‑Level Identity Rules)  

---

# 0. Metadata

```yaml
metadata:
  contract-id: "identity-propagation-contract"
  version: "2.4"
  authoritative: true

  applies-to:
    - all-personas
    - all-projects
    - all-branches
    - all-themes
    - all-tranches
    - all-tickets
    - all-lifecycle-phases
    - all-governed-artefacts
    - all-ticket-maps
    - all-decor-surfaces
    - all-logs
    - all-replay-traces
    - all-documentation

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "<self>"

  governance-envelope: "<id>"
  documentation-envelope: "<id>"
  determinism-envelope: "<id>"
  replay-trace-contract: "<id>"
  lifecycle-contract: "<id>"
  ticket-map-contract: "<id>"
```

# Placeholder Semantics
# Fields containing "<id>" or "<self>" are canonical placeholders.
# They MUST be concretised in project/branch/theme/tranche governance envelopes.
# They MUST NOT be replaced in methodology-level contracts.
# The Auditor Persona MUST treat these placeholders as intentional and NOT as metadata drift.

---

# 1. Purpose

The Identity Propagation Contract defines the **identity model, lineage rules, propagation rules, and determinism constraints** for all governed artefacts across the full Fugue hierarchy:

> **Project → Branch → Theme → Tranche → Ticket**

Identity propagation ensures:

- deterministic ownership  
- deterministic lineage  
- deterministic persona boundaries  
- deterministic metadata propagation  
- deterministic reconciliation  
- deterministic replay  
- audit‑ready provenance  

Identity MUST NOT:

- drift  
- be regenerated  
- be inferred implicitly  
- be mutated outside persona boundaries  
- depend on conversational context  

Identity is a **governed, deterministic, lifecycle‑aligned surface**.

---

# 2. Identity Model (v2.4)

Fugue v2.4 defines **three identity types**.

## 2.1 Initiator Identity (Immutable)

The identity of the persona that **created** the artefact.

It MUST:

- be immutable  
- be preserved across all lifecycle phases  
- be included in metadata  
- be included in replay traces  
- be included in reconciliation lineage  

It MUST NOT:

- be regenerated  
- be overwritten  

---

## 2.2 Owner Identity (Mutable)

The identity of the persona **responsible** for the artefact at the current lifecycle phase.

It MUST:

- be explicitly recorded  
- change only during lifecycle transitions  
- follow persona boundaries  
- be included in metadata  

It MUST NOT:

- change implicitly  
- be inferred  

---

## 2.3 Effective Execution Identity (Derived)

The identity used for **execution**, **evaluation**, or **implementation**.

It MUST:

- be deterministic  
- be derived from persona routing  
- be recorded in implementation logs  
- be recorded in replay traces  

It MUST NOT:

- override initiator identity  
- override owner identity  

---

# 3. Identity Principles

Identity MUST be:

- deterministic  
- explicit  
- complete  
- lineage‑preserving  
- metadata‑aligned  
- naming‑aligned  
- namespace‑aligned  
- evaluator‑aligned  
- governance‑aligned  

Identity MUST NOT:

- be inferred  
- be regenerated  
- be mutated implicitly  
- be omitted from metadata  
- be omitted from replay traces  

Identity MUST be reconstructable from:

- DECOR  
- tickets  
- implementation logs  
- replay traces  
- documentation  
- tranche logs  
- bootstrap logs (Project / Branch / Theme)

---

# 4. Identity Propagation Rules (Hierarchy‑Complete)

Identity MUST propagate deterministically across the full hierarchy:

```
Project → Branch → Theme → Tranche → Ticket
```

And across all lifecycle transitions:

```
Ticket → Implementation Log → Replay Trace → Verification → Reconciliation → Closure
```

Identity propagation MUST be:

- deterministic  
- explicit  
- metadata‑preserving  
- lineage‑preserving  

Identity propagation MUST NOT:

- be inferred from context  
- be mutated by persona improvisation  
- be omitted during transitions  

---

# 5. Identity Metadata Schema (v2.4)

All governed artefacts MUST include:

```yaml
identity:
  initiator: "<persona-id>"
  owner: "<persona-id>"
  effective-execution: "<persona-id>"
  lineage:
    - "<identity-event>"
```

Identity lineage MUST include:

- creation event  
- ownership transfer events  
- lifecycle transition events  
- reconciliation events  
- verification events  
- bootstrap events (Project / Branch / Theme)  

Identity lineage MUST NOT:

- be truncated  
- be rewritten  
- be collapsed  

---

# 6. Identity in Project / Branch / Theme Artefacts

## 6.1 Project Identity Rules
Project‑level artefacts MUST include:

- initiator identity (Initiator)  
- owner identity (Curator)  
- lineage of all bootstrap events  

Identity MUST propagate into:

- Branch artefacts  
- Theme artefacts  
- Tranche artefacts  

---

## 6.2 Branch Identity Rules
Branch‑level artefacts MUST include:

- initiator identity (Initiator)  
- owner identity (Curator)  
- lineage of branch bootstrap events  

Identity MUST propagate into:

- Theme artefacts  
- Tranche artefacts  

---

## 6.3 Theme Identity Rules
Theme‑level artefacts MUST include:

- initiator identity (Initiator)  
- owner identity (Curator)  
- lineage of theme bootstrap events  

Identity MUST propagate into:

- Tranche artefacts  
- Ticket artefacts  

---

# 7. Identity in Tranches

Tranche artefacts MUST include:

- initiator identity (Initiator)  
- owner identity (Curator → Orchestrator → Auditor → Verifier)  
- lineage of tranche lifecycle transitions  

Identity MUST propagate into:

- ticket bundles  
- implementation logs  
- replay traces  
- verification artefacts  
- closure artefacts  

---

# 8. Identity in Tickets

Tickets MUST include:

- initiator identity (Conductor for conceptual tickets; Orchestrator for implementation tickets)  
- owner identity (Implementer or Architect)  
- effective execution identity (Implementer)  

Identity MUST propagate into:

- implementation logs  
- replay traces  
- documentation artefacts  

Tickets MUST NOT:

- omit identity metadata  
- mutate identity implicitly  

---

# 9. Identity in DECOR

DECOR MUST include:

- initiator identity (Architect)  
- owner identity (Architect → Orchestrator → Auditor → Verifier)  
- effective execution identity (N/A)  

Identity MUST propagate into:

- updated DECOR  
- reconciled DECOR  
- DECOR metadata  

Identity MUST NOT:

- be regenerated  
- be overwritten  

---

# 10. Identity in Implementation Logs

Implementation logs MUST include:

- implementer identity  
- evaluator identity  
- identity propagation lineage  

Identity MUST propagate into:

- replay traces  
- verification artefacts  

---

# 11. Identity in Replay Traces

Replay traces MUST include:

- implementer identity  
- evaluator identity  
- identity propagation lineage  

Identity MUST be:

- deterministic  
- explicit  
- complete  

Replay traces MUST NOT:

- omit identity  
- regenerate identity  
- infer identity  

Replay traces MUST follow the **Replay Trace Contract (v2.4)**.

---

# 12. Identity in Documentation

Documentation MUST include:

- initiator identity  
- owner identity  
- identity lineage  

Documentation MUST NOT:

- override identity  
- weaken identity lineage  

Documentation MUST follow the **Documentation Envelope Contract (v2.4)**.

---

# 13. Identity Drift Classification

Identity drift MUST be classified as:

### **Critical**
- missing identity metadata  
- regenerated identity  
- incorrect initiator identity  
- incorrect owner identity  
- incorrect evaluator identity  
- corrupted identity lineage  

### **Major**
- incomplete identity lineage  
- incorrect ownership transfer  
- inconsistent persona routing  

### **Minor**
- formatting issues  
- non‑blocking metadata issues  

All identity drift MUST be recorded in:

- auditor notes  
- reconciliation log  
- reconciled DECOR  

---

# 14. Identity Correction (Epilogue Workflow)

If identity drift exists:

1. **Orchestrator** MUST generate an epilogue ticket  
2. **Responsible persona** MUST correct identity metadata  
3. **Auditor** MUST validate corrections  
4. **Verifier** MUST validate final identity lineage  
5. **Orchestrator** MUST update reconciliation lineage  

Identity MUST NOT be corrected outside persona boundaries.

---