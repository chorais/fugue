# **drift-summary-template.md (v2.4)**  
**Drift Summary Template — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Persona: Auditor (Author), Verifier (Validator)  
Lifecycle: Verification → Reconciliation  
Authority: Reconciled DECOR Contract (v2.4)  

---

# 0. Metadata

```yaml
metadata:
  drift-summary-id: "drift-summary-<X.Y>"
  tranche: "<X.Y>"

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

  generated-on: "<YYYY-MM-DD>"
```

---

# 1. Summary

```yaml
summary: >
  <High-level summary of drift detected across the tranche, including total drift
  events, severity distribution, and any critical governance or determinism failures.>
```

---

# 2. Drift Totals

```yaml
totals:
  total-drift-events: <count>
  critical: <count>
  major: <count>
  minor: <count>
```

---

# 3. Drift by Test Type

```yaml
by-test-type:
  dark-tests:
    total: <count>
    critical: <count>
    major: <count>
    minor: <count>

  golden-tests:
    total: <count>
    critical: <count>
    major: <count>
    minor: <count>

  governance-tests:
    total: <count>
    critical: <count>
    major: <count>
    minor: <count>

  replay-tests:
    total: <count>
    critical: <count>
    major: <count>
    minor: <count>
```

---

# 4. Drift Surfaces

```yaml
drift-surfaces:
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

# 5. Drift Events

Each entry corresponds to a single drift artefact.

```yaml
events:
  - drift-id: "<id>"
    test-id: "<test-id>"
    ticket: "<ticket-id>"
    classification: "<Minor|Major|Critical>"
    surfaces:
      - "<surface>"

    determinism:
      ordering: "<observed>"
      state-transitions: "<observed>"
      metadata-propagation: "<observed>"
      identity-propagation: "<observed>"
      namespace-propagation: "<observed>"

    evaluator:
      drift: "<observed>"
      diagnostics:
        - "<diagnostic>"

    replay:
      ordering: "<observed>"
      state-transitions: "<observed>"
      identity-propagation: "<observed>"
      metadata-propagation: "<observed>"
      evaluator-behaviour: "<observed>"

    identity:
      lineage: "<observed>"
      propagation: "<observed>"

    namespace:
      placement: "<observed>"
      invariants: "<observed>"

    metadata:
      propagation: "<observed>"
      completeness: "<observed>"

    governance:
      violation: "<observed>"
      rule: "<governance-rule>"

    documentation:
      surfaces: "<observed>"
      placement: "<observed>"
      metadata: "<observed>"

    lifecycle:
      phase: "<observed>"
      transition: "<observed>"
```

---

# 6. Critical Drift Summary

```yaml
critical-drift:
  count: <count>
  events:
    - drift-id: "<id>"
      surface: "<surface>"
      description: "<description>"
```

---

# 7. Major Drift Summary

```yaml
major-drift:
  count: <count>
  events:
    - drift-id: "<id>"
      surface: "<surface>"
      description: "<description>"
```

---

# 8. Minor Drift Summary

```yaml
minor-drift:
  count: <count>
  events:
    - drift-id: "<id>"
      surface: "<surface>"
      description: "<description>"
```

---

# 9. Governance Impact Assessment

```yaml
governance-impact:
  persona-boundaries: "<Pass|Fail>"
  lifecycle-alignment: "<Pass|Fail>"
  decor-alignment: "<Pass|Fail>"
  documentation-alignment: "<Pass|Fail>"
  identity-propagation: "<Pass|Fail>"
  namespace-scheme: "<Pass|Fail>"
  evaluator-governance: "<Pass|Fail>"
  determinism-governance: "<Pass|Fail>"
  replay-governance: "<Pass|Fail>"
```

---

# 10. Reconciliation Requirements

```yaml
reconciliation:
  required: "<Yes|No>"
  required-actions:
    - "<action>"
  blocking-issues:
    - "<issue>"
  recommended-fixes:
    - "<fix>"
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