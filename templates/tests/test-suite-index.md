# **test-suite-index.md (v2.4)**  
**Test Suite Index — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Authority: Curator  
Scope: All Test Templates  
Lifecycle: Verification (Phase 4)  

---

# 0. Metadata

```yaml
metadata:
  index-id: "test-suite-index"
  version: "v2.4"
  authoritative: true

  applies-to:
    - dark-test-template
    - golden-test-template
    - governance-test-template
    - replay-test-template
    - all-verification-tests
    - all-determinism-tests
    - all-governance-tests
    - all-replay-tests

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  governance-envelope: "<id>"
  determinism-envelope: "<id>"
  documentation-envelope: "<id>"
  identity-propagation-contract: "<id>"
  namespace-scheme-contract: "<id>"
  evaluator-contract: "<id>"
  replay-trace-contract: "<id>"
  lifecycle-contract: "<id>"

  lifecycle-phase: "verification"
  persona: "auditor|verifier"

  last-updated: "<YYYY-MM-DD>"
```

---

# 1. Purpose

The Test Suite Index provides the **canonical listing and purpose** of all test templates in Fugue v2.4.

It ensures:

- deterministic test coverage  
- governance‑aligned test coverage  
- evaluator‑aligned test coverage  
- replay‑aligned test coverage  
- identity‑aligned test coverage  
- namespace‑aligned test coverage  
- documentation‑aligned test coverage  

This index MUST be:

- complete  
- deterministic  
- identity‑aligned  
- namespace‑aligned  
- governance‑aligned  

It MUST NOT:

- omit any test template  
- merge unrelated test types  
- introduce new reasoning  

---

# 2. Test Templates Overview

The Fugue v2.4 test suite consists of **four canonical test templates**:

| Test Type | Purpose | Expected Outcome | Persona | Contract Authority |
|----------|---------|------------------|---------|--------------------|
| **dark-test.md** | Validate failure modes | Fail | Auditor | Determinism Envelope |
| **golden-test.md** | Validate ideal behaviour | Pass | Auditor | Determinism Envelope |
| **governance-test.md** | Validate governance alignment | Pass | Auditor | Governance Envelope |
| **replay-test.md** | Validate deterministic replay | Pass | Auditor | Replay Trace Contract |

All four are required for every tranche.

---

# 3. Test Template Locations

```
/fugue/templates/tests/
  dark-test.md
  golden-test.md
  governance-test.md
  replay-test.md
  test-suite-index.md   ← this file
```

---

# 4. Test Template Definitions

---

## 4.1 **dark-test.md (v2.4)**  
**Purpose:** Validate **failure modes** across governance, determinism, identity, namespace, evaluator, and replay surfaces.  
**Expected Outcome:** Fail  
**Persona:** Auditor  
**Authority:** Determinism Envelope Contract  

**Validates:**

- determinism violations  
- evaluator drift  
- identity drift  
- namespace drift  
- metadata drift  
- governance drift  
- replay drift  
- lifecycle drift  
- DECOR drift  

---

## 4.2 **golden-test.md (v2.4)**  
**Purpose:** Validate **ideal deterministic behaviour** across all surfaces.  
**Expected Outcome:** Pass  
**Persona:** Auditor  
**Authority:** Determinism Envelope Contract  

**Validates:**

- deterministic ordering  
- deterministic evaluator behaviour  
- deterministic metadata propagation  
- deterministic identity propagation  
- deterministic namespace placement  
- deterministic replay traces  
- DECOR alignment  
- governance alignment  

---

## 4.3 **governance-test.md (v2.4)**  
**Purpose:** Validate **strict governance alignment** across all envelopes.  
**Expected Outcome:** Pass  
**Persona:** Auditor  
**Authority:** Governance Envelope Contract  

**Validates:**

- persona boundaries  
- lifecycle boundaries  
- DECOR alignment  
- documentation alignment  
- identity propagation  
- namespace correctness  
- evaluator governance  
- determinism governance  
- replay governance  

---

## 4.4 **replay-test.md (v2.4)**  
**Purpose:** Validate **deterministic replay behaviour**.  
**Expected Outcome:** Pass  
**Persona:** Auditor  
**Authority:** Replay Trace Contract  

**Validates:**

- deterministic ordering  
- deterministic state transitions  
- deterministic evaluator behaviour  
- deterministic metadata propagation  
- deterministic identity propagation  
- deterministic namespace propagation  
- deterministic replay outcomes  

---

# 5. Governance Surfaces Covered

The test suite collectively covers:

```yaml
governance-surfaces:
  determinism:
    - ordering
    - evaluator-behaviour
    - metadata-propagation
    - identity-propagation
    - namespace-propagation
    - replay-determinism

  governance:
    - persona-boundaries
    - lifecycle-boundaries
    - decor-alignment
    - documentation-alignment
    - evaluator-governance
    - replay-governance

  identity:
    - lineage
    - propagation

  namespaces:
    - placement
    - invariants

  documentation:
    - surfaces
    - placement
    - metadata
```

---

# 6. Lifecycle Alignment

All test templates belong to:

```
Lifecycle Phase: Phase 4 — Verification
Persona: Auditor → Verifier
```

Tests MUST NOT be executed:

- during Orchestration  
- during Implementation  
- during Reconciliation  
- during Closure  

---

# 7. Determinism Rules

The test suite MUST:

- be deterministic  
- be reproducible  
- be identity‑aligned  
- be namespace‑aligned  
- be evaluator‑aligned  
- be replay‑aligned  

Test templates MUST NOT:

- introduce nondeterminism  
- infer missing metadata  
- regenerate identity  

---

# 8. Summary

The Test Suite Index:

- defines all test templates  
- defines their purpose  
- defines their governance surfaces  
- defines their determinism surfaces  
- defines their evaluator surfaces  
- defines their replay surfaces  
- defines their lifecycle alignment  
- defines their persona alignment  

It is the **single authoritative index** for the Fugue v2.4 test suite.

---
