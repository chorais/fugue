# **drift-surface-template.md (v2.4)**  
**Drift Surface Template — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Persona: Auditor (Author), Verifier (Validator)  
Lifecycle: Verification → Reconciliation  
Authority: Reconciled DECOR Contract (v2.4)  

---

# 0. Metadata

```yaml
metadata:
  drift-id: "drift-<X.Y.N>"
  tranche: "<X.Y>"
  ticket: "ticket-<X.Y.Z>"

  classification: "<Minor|Major|Critical>"
  surface-type: "<determinism|evaluator|identity|namespace|metadata|replay|governance|documentation|lifecycle>"

  # Governance surfaces
  governance-envelope: "<id>"
  determinism-envelope: "<id>"
  documentation-envelope: "<id>"
  identity-propagation-contract: "<id>"
  namespace-scheme-contract: "<id>"
  evaluator-contract: "<id>"
  replay-trace-contract: "<id>"
  lifecycle-contract: "<id>"

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  lifecycle-phase: "verification → reconciliation"
  persona: "auditor → verifier"

  detected-on: "<YYYY-MM-DD>"
  last-updated: "<YYYY-MM-DD>"
```

---

# 1. Drift Summary

```yaml
summary: >
  <One-sentence description of the drift surface, including what failed and why it
  is classified as Minor/Major/Critical.>
```

---

# 2. Drift Description

```yaml
description: >
  <Detailed explanation of the drift, including the expected behaviour, the observed
  behaviour, and the specific governance or determinism rule violated.>
```

---

# 3. Drift Classification Rationale

```yaml
classification-rationale:
  severity: "<Minor|Major|Critical>"
  justification: >
    <Explain why this drift severity is appropriate, referencing governance,
    determinism, evaluator, replay, identity, namespace, or lifecycle rules.>
```

---

# 4. Affected Surfaces

```yaml
affected-surfaces:
  determinism:
    - "<surface>"
  evaluator:
    - "<surface>"
  identity:
    - "<surface>"
  namespace:
    - "<surface>"
  metadata:
    - "<surface>"
  replay:
    - "<surface>"
  governance:
    - "<surface>"
  documentation:
    - "<surface>"
  lifecycle:
    - "<surface>"
```

---

# 5. Expected Behaviour

```yaml
expected:
  determinism:
    - "<expected-rule>"
  evaluator:
    - "<expected-rule>"
  identity:
    - "<expected-rule>"
  namespace:
    - "<expected-rule>"
  metadata:
    - "<expected-rule>"
  replay:
    - "<expected-rule>"
  governance:
    - "<expected-rule>"
  documentation:
    - "<expected-rule>"
  lifecycle:
    - "<expected-rule>"
```

---

# 6. Observed Behaviour

```yaml
observed:
  determinism:
    - "<observed>"
  evaluator:
    - "<observed>"
  identity:
    - "<observed>"
  namespace:
    - "<observed>"
  metadata:
    - "<observed>"
  replay:
    - "<observed>"
  governance:
    - "<observed>"
  documentation:
    - "<observed>"
  lifecycle:
    - "<observed>"
```

---

# 7. Root Cause Analysis

```yaml
root-cause:
  primary-cause: "<description>"
  contributing-factors:
    - "<factor>"
  governance-rule-violated: "<rule>"
  determinism-rule-violated: "<rule>"
  evaluator-rule-violated: "<rule>"
  replay-rule-violated: "<rule>"
  identity-rule-violated: "<rule>"
  namespace-rule-violated: "<rule>"
  metadata-rule-violated: "<rule>"
  lifecycle-rule-violated: "<rule>"
```

---

# 8. Impact Assessment

```yaml
impact:
  governance-impact: "<High|Medium|Low>"
  determinism-impact: "<High|Medium|Low>"
  evaluator-impact: "<High|Medium|Low>"
  replay-impact: "<High|Medium|Low>"
  identity-impact: "<High|Medium|Low>"
  namespace-impact: "<High|Medium|Low>"
  metadata-impact: "<High|Medium|Low>"
  lifecycle-impact: "<High|Medium|Low>"
  documentation-impact: "<High|Medium|Low>"
```

---

# 9. Required Remediation

```yaml
remediation:
  required: "<Yes|No>"
  actions:
    - "<action>"
  blocking-issues:
    - "<issue>"
  recommended-fixes:
    - "<fix>"
```

---

# 10. Verification Requirements

```yaml
verification:
  required-tests:
    - "<test-id>"
  required-evaluator-checks:
    - "<check>"
  required-replay-checks:
    - "<check>"
  required-governance-checks:
    - "<check>"
  required-lifecycle-checks:
    - "<check>"
```

---

# 11. Auditor Notes

```yaml
auditor-notes:
  - "<note>"
```

---

# 12. Verifier Notes

```yaml
verifier-notes:
  - "<note>"
```

---
