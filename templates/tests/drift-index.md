# **drift-index.md (v2.4)**  
**Drift Index — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Persona: Auditor (Author), Verifier (Validator)  
Lifecycle: Verification → Reconciliation  
Authority: Reconciled DECOR Contract (v2.4)  

---

# 0. Metadata

```yaml
metadata:
  drift-index-id: "drift-index-<X.Y>"
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
  last-updated: "<YYYY-MM-DD>"
```

---

# 1. Purpose

```yaml
purpose: >
  The Drift Index provides the authoritative listing of all drift artefacts for
  tranche <X.Y>, including drift surfaces, drift events, classifications, and
  reconciliation requirements. It ensures deterministic, governed, and auditable
  tracking of all deviations from expected behaviour across determinism,
  evaluator, replay, identity, namespace, metadata, governance, documentation,
  and lifecycle surfaces.
```

---

# 2. Drift Summary Overview

```yaml
summary:
  total-drift-events: <count>
  critical: <count>
  major: <count>
  minor: <count>
  reconciliation-required: "<Yes|No>"
```

---

# 3. Drift Artefact Locations

```yaml
locations:
  drift-summary: "testing/drift/drift-summary.md"
  drift-surfaces: "testing/drift/drift-surfaces/"
  drift-events: "testing/results/*-result.json"
```

---

# 4. Drift Surface Index

Each entry corresponds to a **drift surface file** generated from the drift-surface-template.

```yaml
drift-surfaces:
  - drift-id: "drift-<X.Y.1>"
    surface-type: "<determinism|evaluator|identity|namespace|metadata|replay|governance|documentation|lifecycle>"
    classification: "<Minor|Major|Critical>"
    file: "testing/drift/drift-surfaces/drift-<X.Y.1>.md"

  - drift-id: "drift-<X.Y.2>"
    surface-type: "<...>"
    classification: "<...>"
    file: "testing/drift/drift-surfaces/drift-<X.Y.2>.md"
```

---

# 5. Drift by Classification

```yaml
classification:
  critical:
    - "drift-<X.Y.A>"
    - "drift-<X.Y.B>"

  major:
    - "drift-<X.Y.C>"

  minor:
    - "drift-<X.Y.D>"
    - "drift-<X.Y.E>"
```

---

# 6. Drift by Surface Type

```yaml
by-surface:
  determinism:
    - "drift-<X.Y.1>"
  evaluator:
    - "drift-<X.Y.2>"
  identity:
    - "drift-<X.Y.3>"
  namespace:
    - "drift-<X.Y.4>"
  metadata:
    - "drift-<X.Y.5>"
  replay:
    - "drift-<X.Y.6>"
  governance:
    - "drift-<X.Y.7>"
  documentation:
    - "drift-<X.Y.8>"
  lifecycle:
    - "drift-<X.Y.9>"
```

---

# 7. Drift by Test Type

```yaml
by-test-type:
  dark-tests:
    - "drift-<X.Y.1>"
    - "drift-<X.Y.4>"

  golden-tests:
    - "drift-<X.Y.5>"

  governance-tests:
    - "drift-<X.Y.7>"

  replay-tests:
    - "drift-<X.Y.2>"
    - "drift-<X.Y.6>"
```

---

# 8. Drift Event Index

Each entry corresponds to a **drift event** recorded in a test result file.

```yaml
drift-events:
  - drift-id: "drift-<X.Y.1>"
    test-id: "<test-id>"
    ticket: "<ticket-id>"
    classification: "<Minor|Major|Critical>"
    surfaces:
      - "<surface>"
    result-file: "testing/results/<test-id>-result.json"

  - drift-id: "drift-<X.Y.2>"
    test-id: "<test-id>"
    ticket: "<ticket-id>"
    classification: "<...>"
    surfaces:
      - "<...>"
    result-file: "testing/results/<test-id>-result.json"
```

---

# 9. Governance Impact Summary

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
  blocking-issues:
    - "<issue>"
  required-actions:
    - "<action>"
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
