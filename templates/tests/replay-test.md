# **replay-test.md (v2.4)**  
**Replay Test Template — Tranche <X.Y>**  
Persona: Auditor (Author), Verifier (Validator)  
Mode: Verification Mode  
Lifecycle Phase: Phase 4 — Verification  
Authority: Replay Trace Contract (v2.4)  

---

# 0. Metadata  
*(Fully aligned with all v2.4 envelopes and contracts)*

```yaml
metadata:
  test-id: "replay-test-<X.Y.N>"
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
  test-type: "replay"
  determinism-critical: true
  evaluator-critical: true
  identity-critical: true
  namespace-critical: true
  metadata-critical: true
  replay-critical: true

  # Status
  status: "Pending|In-Progress|Complete"
  last-updated: "<YYYY-MM-DD>"
```

---

# 1. **Test Summary**

```yaml
summary: >
  <One-sentence description of the replay determinism being validated.>
```

---

# 2. **Purpose**  
*(Why this replay test exists — grounded in Replay Trace Contract)*

```yaml
purpose: >
  <Describe the deterministic replay behaviour this test validates.>
```

---

# 3. **Replay Surface Under Test**  
*(Explicitly defined replay determinism surface)*

```yaml
replay-surface:
  type: "<ordering|state-transitions|evaluator-behaviour|metadata-propagation|identity-propagation|namespace-propagation>"
  description: >
    <Describe the replay determinism rule being validated.>
  expected-outcome: "Pass"
```

---

# 4. **Inputs**  
*(Governed inputs required to validate replay determinism)*

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

# 5. **Expected Replay Determinism**  
*(Deterministic replay expectations)*

```yaml
expected-replay:
  ordering:
    - "<expected-deterministic-ordering>"
  state-transitions:
    - "<expected-state-transition>"
  evaluator-behaviour:
    - "<expected-evaluator-behaviour>"
  metadata-propagation:
    - "<expected-metadata-propagation>"
  identity-propagation:
    - "<expected-identity-propagation>"
  namespace-propagation:
    - "<expected-namespace-propagation>"
  replay-outcome:
    - "<expected-replay-outcome>"
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
  expected-metadata:
    - "<metadata-rule>"
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
  expected-structure:
    - "<structure-rule>"
  expected-ordering:
    - "<ordering-rule>"
  expected-state-transitions:
    - "<transition>"
  expected-identity-propagation:
    - "<identity-rule>"
  expected-metadata-propagation:
    - "<metadata-rule>"
  expected-evaluator-behaviour:
    - "<evaluator-rule>"
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
  expected-alignment:
    - "<governance-rule>"
  expected-surfaces:
    - "<governance-surface>"
```

---

# 10. **Documentation Envelope Expectations**

```yaml
documentation:
  expected-surfaces:
    - "<doc-surface>"
  expected-placement:
    - "<doc-placement>"
  expected-metadata:
    - "<doc-metadata>"
```

---

# 11. **Lifecycle Alignment Expectations**

```yaml
lifecycle:
  expected-phase:
    - "<phase>"
  expected-transition:
    - "<transition>"
  expected-alignment:
    - "<lifecycle-rule>"
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
  ordering:
    - "<observed-ordering>"
  state-transitions:
    - "<observed-state-transition>"
  evaluator:
    - "<observed-evaluator>"
  identity:
    - "<observed-identity>"
  namespace:
    - "<observed-namespace>"
  metadata:
    - "<observed-metadata>"
  replay:
    - "<observed-replay>"
```

---

# 14. **Validation Result**

```yaml
result:
  status: "Pass|Fail"
  notes:
    - "<note>"
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
