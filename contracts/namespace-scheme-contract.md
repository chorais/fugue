# **namespace-scheme-contract.md (v2.4 — Updated for Project/Branch/Theme)**  
**Namespace Scheme Contract — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Authority: Governance Contract  
Scope: All Governed Artefacts  
Lifecycle: Global (Methodology‑Level Structural Rules)  

---

# 0. Metadata

```yaml
metadata:
  contract-id: "namespace-scheme-contract"
  version: "2.4"
  authoritative: true

  applies-to:
    - all-governed-artefacts
    - all-personas
    - all-projects
    - all-branches
    - all-themes
    - all-tranches
    - all-lifecycle-phases
    - all-ticket-maps
    - all-tickets
    - all-decor-surfaces
    - all-logs
    - all-replay-traces
    - all-governed-documentation

  naming-scheme: "v2.4"
  namespace-scheme: "<self>"
  identity-propagation: "v2.4"

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

The Namespace Scheme Contract defines the **directory structure, placement rules, governance boundaries, and lifecycle‑aligned namespaces** for all governed artefacts in the Fugue Orchestration Method.

Namespaces ensure:

- deterministic placement  
- deterministic retrieval  
- deterministic reconciliation  
- deterministic replay  
- persona‑scoped boundaries  
- governance‑safe storage  
- audit‑ready structure  
- substrate‑agnostic organisation  

Namespaces MUST NOT:

- drift  
- collapse  
- merge implicitly  
- be created ad‑hoc  
- be repurposed without governance approval  

Namespaces are a **governed structural surface**.

---

# 2. Namespace Principles

Namespaces MUST be:

- deterministic  
- stable  
- persona‑scoped  
- lifecycle‑aligned  
- governance‑aligned  
- naming‑aligned  
- identity‑aligned  
- metadata‑aligned  

Namespaces MUST NOT:

- depend on conversational context  
- depend on implicit memory  
- depend on runtime state  
- embed governed artefacts inside other governed artefacts  

Namespaces MUST be reconstructable from:

- DECOR  
- Ticket Map  
- Documentation Envelope  
- Determinism Envelope  
- Replay Trace Contract  

---

# 3. Root Namespace Structure (v2.4)

Fugue v2.4 defines **three root namespaces**:

```
/fugue_docs/      → governed documentation + governed artefacts
/docs/            → developer documentation (non-governed)
/public-docs/     → user-facing documentation (non-governed)
```

Only `/fugue_docs` is governed.

---

# 4. Governed Namespace Structure (`/fugue_docs`)

All governed artefacts MUST be stored under:

```
/fugue_docs/
```

Fugue v2.4 recognises **four governance layers**, each with its own governed namespace:

```
/fugue_docs/project/
/fugue_docs/branches/<branch-name>/
/fugue_docs/themes/<theme-name>/
/fugue_docs/<category>/<tranche-name>/
```

The governed namespace MUST contain the following directories:

```
project/
branches/
themes/
governance/
specs/
decors/
tickets/
logs/
replay/
verification/
closure/
runtime/
testing/
integration/
architecture/
concerns/
archive/
```

Each directory has strict persona and lifecycle boundaries.

---

# 5. Namespace Definitions (Updated v2.4)

## **5.1 `/fugue_docs/project/` — Project‑Level Governed Namespace**

Contains:

- project preamble  
- project DECOR  
- project governance envelope  
- naming + namespace roots  
- persona map  
- identity propagation rules  
- documentation envelope  
- bootstrap log  

Persona: **Initiator / Architect / Curator**  
Lifecycle: **Project Bootstrap → Global**

---

## **5.2 `/fugue_docs/branches/<branch-name>/` — Branch‑Level Governed Namespace**

Contains:

- branch preamble  
- branch DECOR  
- branch governance envelope  
- branch naming + namespace schemes  
- branch identity propagation rules  
- branch documentation envelope  
- branch bootstrap log  

Persona: **Initiator / Architect / Curator**  
Lifecycle: **Branch Bootstrap → Global**

---

## **5.3 `/fugue_docs/themes/<theme-name>/` — Theme‑Level Governed Namespace**

Contains:

- theme preamble  
- theme DECOR  
- theme governance envelope  
- theme naming + namespace schemes  
- theme identity propagation rules  
- theme documentation envelope  
- theme bootstrap log  

Persona: **Initiator / Architect / Curator**  
Lifecycle: **Theme Bootstrap → Global**

---

## **5.4 `/fugue_docs/governance/`**
Contains:

- governance contracts  
- governance posture  
- lifecycle specifications  
- naming, namespace, identity contracts  

Persona: **Curator**  
Lifecycle: **Bootstrap → Global**

---

## **5.5 `/fugue_docs/specs/`**
Contains:

- orchestration specifications  
- conceptual lifecycle docs  
- persona boundary specifications  

Persona: **Conductor (Conceptual)**  
Lifecycle: **Bootstrap → Orchestration**

---

## **5.6 `/fugue_docs/decors/`**
Contains:

- Day‑0 DECOR  
- Updated DECOR  
- Reconciled DECOR  
- DECOR metadata  

Persona: **Architect**  
Lifecycle: **Bootstrap → Reconciliation**

---

## **5.7 `/fugue_docs/tickets/`**
Contains:

- ticket bundles  
- ticket metadata  
- ticket lineage  

Persona: **Conductor (Conceptual)**  
Lifecycle: **Orchestration**

---

## **5.8 `/fugue_docs/logs/`**
Contains:

- implementation logs  
- orchestration logs  
- lifecycle logs  

Persona: **Implementer / Orchestrator**  
Lifecycle: **Implementation → Verification**

---

## **5.9 `/fugue_docs/replay/`**
Contains:

- replay traces  
- replay metadata  
- determinism lineage  

Persona: **Implementer**  
Lifecycle: **Implementation → Verification**

---

## **5.10 `/fugue_docs/verification/`**
Contains:

- drift classification  
- auditor notes  
- verification reports  

Persona: **Auditor / Verifier**  
Lifecycle: **Verification**

---

## **5.11 `/fugue_docs/closure/`**
Contains:

- closure reports  
- reconciled artefacts  
- tranche closure metadata  

Persona: **Conductor / Curator**  
Lifecycle: **Closure**

---

## **5.12 `/fugue_docs/runtime/`**
Contains:

- runtime diagrams  
- integration notes  
- runtime metadata  

Persona: **Implementer**  
Lifecycle: **Implementation**

---

## **5.13 `/fugue_docs/testing/`**
Contains:

- test documentation  
- test metadata  

Persona: **Implementer**  
Lifecycle: **Implementation**

---

## **5.14 `/fugue_docs/integration/`**
Contains:

- integration documentation  
- integration metadata  

Persona: **Implementer**  
Lifecycle: **Implementation**

---

## **5.15 `/fugue_docs/architecture/`**
Contains:

- ADRs  
- architecture diagrams  
- conceptual architecture artefacts  

Persona: **Architect**  
Lifecycle: **Bootstrap → Reconciliation**

---

## **5.16 `/fugue_docs/concerns/`**
Contains:

- forward developer‑facing concerns  
- concern metadata  

Persona: **Implementer**  
Lifecycle: **Implementation → Verification**

---

## **5.17 `/fugue_docs/archive/`**
Contains:

- immutable historical artefacts  
- superseded versions  
- deprecated structures  

Persona: **Curator**  
Lifecycle: **Global**

---

# 6. Forbidden Namespace Rules

Governed artefacts MUST NOT be stored in:

- root directory  
- `/docs`  
- `/public-docs`  
- persona folders  
- implementation logs  
- tickets  
- DECOR files  

Project/Branch/Theme artefacts MUST NOT be stored in tranche‑level namespaces.

Architecture documentation MUST NOT be stored under `/specs`.

Concerns MUST NOT be stored under:

- `/tickets`  
- `/logs`  
- `/specs`  

Replay traces MUST NOT be stored under:

- `/logs`  
- `/tickets`  
- `/decors`  

---

# 7. Namespace Determinism Rules

Namespaces MUST be:

- deterministic  
- stable  
- reproducible  
- identity‑aligned  
- naming‑aligned  

Namespace determinism includes:

- deterministic folder creation  
- deterministic folder naming  
- deterministic artefact placement  
- deterministic lineage preservation  

Namespaces MUST NOT:

- be created dynamically  
- be renamed without governance approval  
- be merged implicitly  

---

# 8. Namespace Identity Rules

Namespaces MUST preserve:

- identity lineage  
- persona ownership  
- lifecycle ownership  

Identity propagation MUST follow the **Identity Propagation Contract (v2.4)**.

---

# 9. Namespace Drift Classification

Namespace drift MUST be classified as:

### **Critical**
- artefacts stored in the wrong namespace  
- governed artefacts stored outside `/fugue_docs`  
- missing required namespaces  
- corrupted namespace structure  

### **Major**
- mis‑routed persona documentation  
- incorrect placement of governed artefacts  

### **Minor**
- naming inconsistencies  
- metadata inconsistencies  

All namespace drift MUST be recorded in:

- auditor notes  
- reconciliation log  
- reconciled DECOR  

---

# 10. Namespace Correction (Epilogue Workflow)

If namespace drift exists:

1. **Orchestrator** MUST generate an epilogue ticket  
2. **Responsible persona** MUST correct namespace placement  
3. **Auditor** MUST validate corrections  
4. **Verifier** MUST validate final structure  
5. **Orchestrator** MUST update reconciliation lineage  

Namespace corrections MUST NOT occur outside persona boundaries.

---