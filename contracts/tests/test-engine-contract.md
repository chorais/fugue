# **test-engine-contract.md (v2.4)**  
**Test Execution Engine Governance Contract — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Authority: Determinism Envelope Contract (v2.4)  
Scope: Test Execution Engine (TEE)  
Lifecycle: Phase 4 — Verification  

---

# 0. Metadata

```yaml
metadata:
  contract-id: "test-engine-contract"
  version: "2.4"
  authoritative: true

  applies-to:
    - test-execution-engine
    - test-runner
    - evaluator-engine
    - replay-engine
    - metadata-engine
    - identity-engine
    - namespace-engine
    - drift-engine
    - diagnostics-engine

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

The Test Execution Engine (TEE) is the **runtime enforcement mechanism** for all verification activities in Fugue v2.4.

This contract defines:

- how tests MUST be executed  
- how determinism MUST be enforced  
- how evaluator behaviour MUST be validated  
- how replay determinism MUST be validated  
- how identity & namespace propagation MUST be validated  
- how drift MUST be detected and classified  
- how logs and results MUST be produced  
- how governance alignment MUST be enforced  

The TEE MUST NOT:

- infer missing metadata  
- regenerate identity  
- reorder steps  
- introduce nondeterminism  
- skip required surfaces  
- collapse governance surfaces  

---

# 2. Engine Responsibilities

The Test Execution Engine MUST:

- execute all test templates deterministically  
- validate all governance surfaces  
- validate all determinism surfaces  
- validate all evaluator surfaces  
- validate all replay surfaces  
- validate all identity surfaces  
- validate all namespace surfaces  
- validate all documentation surfaces  
- validate all lifecycle surfaces  
- produce test results  
- produce drift artefacts  
- produce logs  
- produce diagnostics  

The engine MUST NOT:

- modify test artefacts  
- modify metadata  
- modify identity  
- modify namespaces  
- modify DECOR  
- modify tickets  
- modify tranche artefacts  

---

# 3. Determinism Rules

The engine MUST enforce:

- deterministic ordering  
- deterministic state transitions  
- deterministic evaluator behaviour  
- deterministic metadata propagation  
- deterministic identity propagation  
- deterministic namespace propagation  
- deterministic replay outcomes  

The engine MUST NOT:

- reorder transitions  
- reorder metadata  
- reorder identity lineage  
- reorder namespace lineage  
- reorder evaluator diagnostics  

---

# 4. Evaluator Rules

The engine MUST:

- load evaluator categories  
- validate evaluator determinism  
- validate evaluator governance  
- validate evaluator diagnostics  
- detect evaluator drift  

The engine MUST NOT:

- infer evaluator behaviour  
- modify evaluator output  
- suppress evaluator diagnostics  

---

# 5. Replay Rules

The engine MUST:

- load replay traces  
- validate replay ordering  
- validate replay state transitions  
- validate replay identity propagation  
- validate replay metadata propagation  
- validate replay evaluator behaviour  

The engine MUST NOT:

- regenerate replay traces  
- reorder replay transitions  
- infer missing replay metadata  

---

# 6. Identity Rules

The engine MUST:

- validate identity lineage  
- validate identity propagation  
- detect identity drift  

The engine MUST NOT:

- regenerate identity  
- infer identity lineage  

---

# 7. Namespace Rules

The engine MUST:

- validate namespace placement  
- validate namespace invariants  
- detect namespace drift  

The engine MUST NOT:

- modify namespaces  
- infer namespace placement  

---

# 8. Metadata Rules

The engine MUST:

- validate metadata propagation  
- validate metadata completeness  
- detect metadata drift  

The engine MUST NOT:

- infer metadata  
- generate metadata  

---

# 9. Governance Rules

The engine MUST validate:

- persona boundaries  
- lifecycle alignment  
- DECOR alignment  
- documentation alignment  
- evaluator governance  
- determinism governance  
- replay governance  

The engine MUST NOT:

- override governance envelopes  
- bypass governance checks  

---

# 10. Drift Rules

The engine MUST:

- detect drift  
- classify drift  
- record drift surfaces  
- produce drift artefacts  
- escalate critical drift  

Drift classification MUST be:

- Critical  
- Major  
- Minor  

The engine MUST NOT:

- collapse drift surfaces  
- merge drift events  
- infer drift classification  

---

# 11. Logging Rules

The engine MUST produce:

- test run logs  
- evaluator diagnostics  
- replay diagnostics  
- drift logs  

Logs MUST:

- be deterministic  
- be complete  
- be immutable  

The engine MUST NOT:

- redact logs  
- reorder logs  
- merge logs  

---

# 12. Result Rules

The engine MUST produce:

- JSON test results  
- JSON drift artefacts  

Results MUST:

- follow the test-results-schema.json  
- include all required surfaces  
- include all required metadata  

The engine MUST NOT:

- produce Markdown results  
- omit required fields  
- infer missing fields  

---

# 13. Lifecycle Rules

The engine MUST operate only during:

```
Phase 4 — Verification
```

The engine MUST NOT operate during:

- Orchestration  
- Implementation  
- Reconciliation  
- Closure  

---
