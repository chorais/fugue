# **test-suite-contract.md (v2.4)**  
**Test Suite Governance Contract — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Authority: Governance Envelope Contract (v2.4)  
Scope: All Test Templates, All Test Artefacts, All Verification Activities  
Lifecycle: Phase 4 — Verification  

---

# 0. Metadata

```yaml
metadata:
  contract-id: "test-suite-contract"
  version: "2.4"
  authoritative: true

  applies-to:
    - dark-test-template
    - golden-test-template
    - governance-test-template
    - replay-test-template
    - test-suite-index
    - test-folder-structure
    - all-test-artefacts
    - all-test-results
    - all-test-logs
    - all-drift-surfaces
    - all-replay-surfaces
    - all-evaluator-surfaces

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

The Test Suite Contract defines the **mandatory structure, behaviour, metadata, determinism rules, evaluator rules, replay rules, identity rules, namespace rules, and governance rules** for all test artefacts in Fugue v2.4.

It ensures that:

- all tests are deterministic  
- all tests are governance‑aligned  
- all tests are evaluator‑aligned  
- all tests are replay‑aligned  
- all tests are identity‑aligned  
- all tests are namespace‑aligned  
- all tests are lifecycle‑aligned  
- all tests are reproducible  
- all tests are auditable  

The test suite MUST NOT:

- introduce new reasoning  
- violate persona boundaries  
- violate governance envelopes  
- violate determinism  
- violate identity propagation  
- violate namespace rules  
- violate evaluator rules  
- violate replay rules  

---

# 2. Test Suite Composition

The test suite MUST contain exactly four canonical test templates:

1. **dark-test.md**  
2. **golden-test.md**  
3. **governance-test.md**  
4. **replay-test.md**

These MUST NOT be renamed, removed, merged, or extended.

The suite MUST also contain:

- **test-suite-index.md**  
- **test-folder-structure.md**  

These define the structure and purpose of the suite.

---

# 3. Test Template Rules

Each test template MUST:

- follow its canonical structure  
- include all required metadata  
- include all required governance surfaces  
- include all required determinism surfaces  
- include all required evaluator surfaces  
- include all required replay surfaces  
- include all required identity surfaces  
- include all required namespace surfaces  
- include all required documentation surfaces  
- include all required lifecycle surfaces  

Test templates MUST NOT:

- omit required sections  
- add new sections  
- collapse sections  
- merge unrelated surfaces  

---

# 4. Test Artefact Rules

All test artefacts MUST:

- be placed under `/testing/tests/`  
- follow the canonical folder structure  
- follow the canonical naming scheme  
- follow the canonical namespace scheme  
- follow the canonical identity propagation rules  

Test artefacts MUST NOT:

- be stored outside governed namespaces  
- be stored in logs, tickets, or DECOR folders  
- be stored in `/docs` or `/public-docs`  

---

# 5. Test Execution Rules

Test execution MUST:

- be deterministic  
- be reproducible  
- be evaluator‑aligned  
- be replay‑aligned  
- be identity‑aligned  
- be namespace‑aligned  
- be metadata‑aligned  

Test execution MUST NOT:

- infer missing metadata  
- regenerate identity  
- reorder steps  
- skip steps  
- introduce nondeterminism  

---

# 6. Test Result Rules

Test results MUST:

- be stored under `/testing/results/`  
- be stored as JSON  
- include deterministic metadata  
- include evaluator diagnostics  
- include replay diagnostics  
- include drift classification  

Test results MUST NOT:

- be stored in Markdown  
- be stored outside governed namespaces  
- be overwritten without governance approval  

---

# 7. Drift Rules

Drift MUST be classified as:

- Critical  
- Major  
- Minor  

Drift MUST include:

- drift surfaces  
- drift references  
- drift metadata  

Drift MUST NOT:

- be inferred  
- be collapsed  
- be merged  

---

# 8. Replay Rules

Replay MUST:

- follow the Replay Trace Contract  
- include deterministic ordering  
- include deterministic state transitions  
- include deterministic evaluator behaviour  
- include deterministic metadata propagation  
- include deterministic identity propagation  
- include deterministic namespace propagation  

Replay MUST NOT:

- introduce nondeterminism  
- reorder transitions  
- regenerate identity  

---

# 9. Evaluator Rules

Evaluator behaviour MUST:

- follow the Evaluator Contract  
- include evaluator categories  
- include evaluator diagnostics  
- include evaluator determinism rules  
- include evaluator governance rules  

Evaluator behaviour MUST NOT:

- drift  
- infer missing metadata  
- regenerate identity  

---

# 10. Identity & Namespace Rules

Identity MUST:

- follow the Identity Propagation Contract  
- preserve lineage  
- propagate deterministically  

Namespace MUST:

- follow the Namespace Scheme Contract  
- preserve invariants  
- preserve placement  

Identity and namespace MUST NOT:

- drift  
- be regenerated  
- be inferred  

---

# 11. Documentation Rules

Documentation MUST:

- follow the Documentation Envelope Contract  
- include required surfaces  
- include required metadata  
- include required placement  

Documentation MUST NOT:

- be stored outside governed namespaces  
- be merged with test artefacts  

---

# 12. Lifecycle Rules

All test artefacts MUST align with:

```
Lifecycle Phase: Phase 4 — Verification
Persona: Auditor → Verifier
```

Tests MUST NOT be executed or stored during:

- Orchestration  
- Implementation  
- Reconciliation  
- Closure  

---

# 13. Summary

The Test Suite Contract:

- defines the canonical test suite structure  
- enforces governance alignment  
- enforces determinism  
- enforces evaluator behaviour  
- enforces replay determinism  
- enforces identity propagation  
- enforces namespace correctness  
- enforces documentation alignment  
- enforces lifecycle alignment  
- defines drift surfaces  
- defines validation surfaces  

It is the **global governance substrate** for the Fugue v2.4 test suite.

---