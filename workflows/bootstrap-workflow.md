# **bootstrap-workflow.md (v2.4)**  
**Bootstrap Workflow**  
Version: 2.4  
Status: Active  
Purpose: Define the deterministic, persona‑isolated bootstrap sequence for a new tranche.  
Methodology: Fugue Orchestration Method  
Implementation: Chorais  

---

# 1. Purpose

The Bootstrap Workflow defines the **first phase** of every tranche.  
It ensures that:

- the tranche is initialised deterministically  
- personas begin in a clean, isolated state  
- governance posture is established  
- DECOR can be generated without ambiguity  
- all required folders, logs, and templates exist before work begins  

Bootstrap MUST complete before any tickets are generated.

---

# 2. Preconditions

Bootstrap may begin only when:

- the previous tranche is closed  
- reconciled DECOR (if any) is final  
- governance posture is stable  
- the human sponsor has approved the tranche theme  

Bootstrap MUST NOT begin mid‑tranche.

---

# 3. Workflow Overview

Bootstrap consists of the following deterministic steps:

1. **Tranche Namespace Creation**  
2. **Preamble Drafting (Curator)**  
3. **Preamble Interpretation (Initiator)**  
4. **Initial DECOR Generation (Architect)**  
5. **DECOR Routing Decision (Conductor)**  
6. **Bootstrap Validation (Auditor)**  
7. **Tranche Activation**  

Each step MUST be completed in order.

---

# 4. Step‑by‑Step Workflow

## 4.1 Step 1 — Tranche Namespace Creation

Chorais MUST create the following governed structure:

```
/fugue_docs/specs/<tranche-name>/
  preamble.md
  preamble-interpretation.md

/fugue_docs/decors/<tranche-name>/
  decor.md
  decor-updates/
  reconciled-decor.md

/fugue_docs/tickets/<tranche-name>/
  ticket-map.md

/fugue_docs/verification/<tranche-name>/
  drift/
    drift-summary.md
    drift-surfaces/

/fugue_docs/closure/<tranche-name>/
  closure-report.md
  closure-log.md
```

All folders MUST exist before personas begin work.

---

## 4.2 Step 2 — Preamble Drafting (Curator Persona)

The Curator Persona MUST:

- draft the tranche preamble  
- define the tranche mission  
- define governance posture  
- define constraints and boundaries  
- define acceptance criteria  
- define naming/namespace/identity propagation posture  

The preamble MUST be stored in:

```
/fugue_docs/specs/<tranche-name>/preamble.md
```

The preamble MUST follow the canonical v2.4 template.

---

## 4.3 Step 3 — Preamble Interpretation (Initiator Persona)

The Initiator Persona MUST:

- interpret the preamble  
- extract governance themes  
- extract mission intent  
- extract scope and boundaries  
- extract identity propagation rules  
- extract naming/namespace posture  
- extract evaluator metadata posture  
- identify ambiguities  
- request clarifications from the Curator or Conductor  

The Initiator MUST NOT generate DECOR.

The interpretation MUST be written into:

```
/fugue_docs/specs/<tranche-name>/preamble-interpretation.md
```

---

## 4.4 Step 4 — Initial DECOR Generation (Architect Persona)

The Architect Persona MUST generate:

```
/fugue_docs/decors/<tranche-name>/decor.md
```

Initial DECOR MUST follow the canonical v2.4 DECOR template and MUST include:

- Design  
- Extensions  
- Considerations  
- Opportunities  
- Risks  

Initial DECOR MUST NOT be modified after this step except through:

- governed DECOR Updates  
- reconciliation  

---

## 4.5 Step 5 — DECOR Routing Decision (Conductor Persona)

The Conductor Persona MUST choose:

- **Method A — Product‑First Grounding**  
- **Method B — Technical‑First Grounding**  

The routing decision MUST be:

- justified  
- logged  
- deterministic  
- aligned with governance posture  

The decision MUST be recorded in:

```
/fugue_docs/specs/<tranche-name>/preamble-interpretation.md
```

and referenced in:

```
/fugue_docs/tickets/<tranche-name>/ticket-map.md
```

---

## 4.6 Step 6 — Bootstrap Validation (Auditor Persona)

The Auditor Persona MUST validate that:

- the preamble exists and follows the template  
- the preamble interpretation exists and is complete  
- Initial DECOR exists and follows the template  
- the DECOR routing decision is logged  
- all required folders and logs exist  
- no persona has violated isolation  
- no template drift has occurred  
- naming/namespace/identity propagation posture is present  
- evaluator metadata posture is present  

Any deviation MUST be classified as drift.

Bootstrap MUST NOT proceed until drift is resolved.

---

## 4.7 Step 7 — Tranche Activation

Bootstrap completes when:

- Conductor approves  
- Architect approves  
- Auditor approves  
- Human sponsor approves  

Bootstrap approval MUST be recorded in:

```
/fugue_docs/specs/<tranche-name>/bootstrap-approval.md
```

The bootstrap approval record MUST include:

- date and tranche identifier  
- approving personas listed  
- human sponsor approval confirmation  
- DECOR routing decision reference  
- any outstanding concerns or conditions noted at activation  

Once activated:

- ticket generation may begin  
- personas may proceed to the Ticket Loop Workflow  

Bootstrap MUST NOT be repeated mid‑tranche.

---

# 5. Outputs

Bootstrap produces the following deterministic artefacts:

- tranche namespace structure  
- tranche preamble  
- preamble interpretation  
- Initial DECOR  
- DECOR routing decision  
- bootstrap validation log  
- bootstrap approval record  

These artefacts MUST exist before any tickets are generated.

---

# 6. Governance Requirements

Bootstrap MUST:

- follow persona isolation rules  
- follow canonical templates  
- follow DECOR Specification  
- follow Naming Scheme Contract  
- follow Namespace Scheme Contract  
- follow Identity Propagation Contract  
- follow Fugue Method lifecycle  
- be deterministic and reproducible  

Bootstrap MUST NOT:

- generate tickets  
- generate implementation artefacts  
- modify DECOR after creation  
- skip validation steps  

---

# 7. Summary

Bootstrap establishes:

- governance posture  
- architectural foundation  
- deterministic structure  
- persona isolation  
- DECOR alignment  
- auditability  

It is the **foundation** of every tranche.


