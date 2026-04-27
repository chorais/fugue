# **dark-test.md (v2.4)**  
**Dark Test Template — Tranche <X.Y>**  
Persona: Auditor (Author), Verifier (Validator)  
Mode: Verification Mode  
Lifecycle Phase: Phase 4 — Verification  
Authority: Determinism Envelope Contract (v2.4)  

---

# 0. Metadata  
*(Fully aligned with all v2.4 envelopes and contracts)*

```yaml
metadata:
  test-id: "dark-test-<X.Y.N>"
  tranche: "<X.Y>"
  ticket: "ticket-<X.Y.Z>"

  # Governance surfaces
  governance-envelope: "<id>"
  determinism-envelope: "<id>"
  documentation-envelope: "<id>"
  identity-propagation-contract: "<id>"
  namespace-scheme-contract: "<id>"
  evaluator-contract: "<id>"
  replay-trace-contract: "<id>"
  lifecycle-contract: "<id>"

  # Naming / Namespace / Identity
  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  # DECOR lineage
  decor-source: "decors/<X.Y>/decor.md"
  reconciled-decor-source: "decors/<X.Y>/reconciled-decor.md"

  # Test behaviour
  test-type: "dark"
  determinism-critical: true
  governance-critical: true
  identity-critical: true
  namespace-critical: true
  evaluator-critical: true
  replay-critical: true

  # Status
  status: "Pending|In-Progress|Complete"
  last-updated: "<YYYY-MM-DD>"
```

---

# 1. **Test Summary**

```yaml
summary: >
  <One-sentence description of the failure mode being validated.>
```

---

# 2. **Purpose**  
*(Why this dark test exists — grounded in governance envelopes)*

```yaml
purpose: >
  <Describe the governance, determinism, identity, namespace, or evaluator failure mode this test is designed to detect.>
```

---

# 3. **Failure Mode Under Test**  
*(Explicitly defined failure surface)*

```yaml
failure-mode:
  type: "<determinism|identity|namespace|metadata|evaluator|governance|decor|lifecycle>"
  description: >
    <Describe the expected failure condition.>
  expected-drift-classification: "<Critical|Major|Minor>"
```

---

# 4. **Inputs**  
*(Governed inputs required to trigger the failure)*

```yaml
inputs:
  artefacts:
    - "<path-to-artefact>"
  metadata:
    - "<metadata-surface>"
  identity:
    - "<identity-surface>"
  namespaces:
    - "<namespace-surface>"
  evaluator:
    - "<evaluator-surface>"
  replay:
    - "<replay-trace>"
```

---

# 5. **Expected Failure Behaviour**  
*(Deterministic failure expectations)*

```yaml
expected-failure:
  determinism:
    - "<expected-determinism-violation>"
  evaluator:
    - "<expected-evaluator-violation>"
  identity:
    - "<expected-identity-violation>"
  namespace:
    - "<expected-namespace-violation>"
  metadata:
    - "<expected-metadata-violation>"
  governance:
    - "<expected-governance-violation>"
  replay:
    - "<expected-replay-violation>"
```

---

# 6. **Evaluator Expectations**  
*(Required by Evaluator Contract v2.4)*

```yaml
evaluator:
  categories:
    - "<category>"
  expected-diagnostics:
    - "<diagnostic>"
  expected-drift:
    - "<evaluator-drift>"
  determinism:
    - "<determinism-rule>"
```

---

# 7. **Replay Trace Expectations**  
*(Required by Replay Trace Contract v2.4)*

```yaml
replay-trace:
  required: true
  expected-traces:
    - "<trace-id>"
  expected-state-transitions:
    - "<transition>"
  expected-ordering:
    - "<ordering-rule>"
  expected-identity-propagation:
    - "<identity-rule>"
  expected-metadata-propagation:
    - "<metadata-rule>"
```

---

# 8. **Identity & Namespace Expectations**  
*(Required by Identity Propagation + Namespace Scheme Contracts)*

```yaml
identity:
  expected-lineage:
    - "<identity-event>"
  expected-propagation:
    - "<identity-rule>"

namespaces:
  expected-placement:
    - "<namespace-rule>"
  expected-invariants:
    - "<namespace-invariant>"
```

---

# 9. **Governance Envelope Expectations**

```yaml
governance:
  expected-violations:
    - "<governance-violation>"
  expected-enforcement:
    - "<governance-rule>"
```

---

# 10. **Documentation Envelope Expectations**

```yaml
documentation:
  expected-violations:
    - "<doc-violation>"
  expected-enforcement:
    - "<doc-rule>"
```

---

# 11. **Lifecycle Alignment Expectations**

```yaml
lifecycle:
  expected-phase:
    - "<phase>"
  expected-transition:
    - "<transition>"
  expected-violation:
    - "<lifecycle-violation>"
```

---

# 12. **Execution Steps**  
*(Deterministic steps the Auditor must perform)*

```yaml
steps:
  - "<step-1>"
  - "<step-2>"
  - "<step-3>"
```

---

# 13. **Observed Behaviour**  
*(Filled in by Auditor)*

```yaml
observed:
  determinism:
    - "<observed-determinism>"
  evaluator:
    - "<observed-evaluator>"
  identity:
    - "<observed-identity>"
  namespace:
    - "<observed-namespace>"
  metadata:
    - "<observed-metadata>"
  governance:
    - "<observed-governance>"
  replay:
    - "<observed-replay>"
```

---

# 14. **Drift Classification**  
*(Required by Reconciled DECOR Contract v2.4)*

```yaml
drift:
  classification: "<Critical|Major|Minor>"
  surfaces:
    - "<drift-surface>"
  references:
    - "<reference>"
```

---

# 15. **Auditor Notes**

```yaml
auditor-notes:
  - "<note>"
```

---

# 16. **Verifier Notes**

```yaml
verifier-notes:
  - "<note>"
```

---

# 17. **Change Log**

```yaml
changelog:
  - version: "<v2.4.x>"
    date: "<YYYY-MM-DD>"
    changes:
      - "<change>"
    updated-by: "<persona>"
```

---