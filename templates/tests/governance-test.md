# **governance-test.md (v2.4)**  
**Governance Test Template — Tranche <X.Y>**  
Persona: Auditor (Author), Verifier (Validator)  
Mode: Verification Mode  
Lifecycle Phase: Phase 4 — Verification  
Authority: Governance Envelope Contract (v2.4)  

---

# 0. Metadata  
*(Fully aligned with all v2.4 governance envelopes and contracts)*

```yaml
metadata:
  test-id: "governance-test-<X.Y.N>"
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
  test-type: "governance"
  governance-critical: true
  determinism-critical: true
  identity-critical: true
  namespace-critical: true
  evaluator-critical: true
  replay-critical: true
  documentation-critical: true

  # Status
  status: "Pending|In-Progress|Complete"
  last-updated: "<YYYY-MM-DD>"
```

---

# 1. **Test Summary**

```yaml
summary: >
  <One-sentence description of the governance rule or envelope being validated.>
```

---

# 2. **Purpose**  
*(Why this governance test exists — grounded in governance envelopes)*

```yaml
purpose: >
  <Describe the governance rule, envelope, or invariant this test validates.>
```

---

# 3. **Governance Surface Under Test**  
*(Explicitly defined governance surface)*

```yaml
governance-surface:
  type: "<persona-boundary|lifecycle-boundary|decor-alignment|documentation-alignment|identity-propagation|namespace-scheme|evaluator-governance|determinism-governance|replay-governance>"
  description: >
    <Describe the governance rule being validated.>
  expected-outcome: "Pass"
```

---

# 4. **Inputs**  
*(Governed inputs required to validate governance alignment)*

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
  documentation:
    - "<documentation-surface>"
```

---

# 5. **Expected Governance Behaviour**  
*(Deterministic governance expectations)*

```yaml
expected-governance:
  persona-boundaries:
    - "<expected-persona-rule>"
  lifecycle:
    - "<expected-lifecycle-rule>"
  decor:
    - "<expected-decor-rule>"
  documentation:
    - "<expected-doc-rule>"
  identity:
    - "<expected-identity-rule>"
  namespace:
    - "<expected-namespace-rule>"
  evaluator:
    - "<expected-evaluator-rule>"
  determinism:
    - "<expected-determinism-rule>"
  replay:
    - "<expected-replay-rule>"
```

---

# 6. **Evaluator Governance Expectations**  
*(Required by Evaluator Contract v2.4)*

```yaml
evaluator:
  categories:
    - "<category>"
  expected-governance:
    - "<evaluator-governance-rule>"
  expected-diagnostics:
    - "<diagnostic>"
  determinism:
    - "<determinism-rule>"
```

---

# 7. **Replay Trace Governance Expectations**  
*(Required by Replay Trace Contract v2.4)*

```yaml
replay-trace:
  required: true
  expected-traces:
    - "<trace-id>"
  expected-governance:
    - "<replay-governance-rule>"
  expected-ordering:
    - "<ordering-rule>"
  expected-identity-propagation:
    - "<identity-rule>"
  expected-metadata-propagation:
    - "<metadata-rule>"
```

---

# 8. **Identity & Namespace Governance Expectations**  
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

# 9. **Documentation Envelope Expectations**

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

# 10. **Lifecycle Governance Expectations**

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

# 11. **Execution Steps**  
*(Deterministic steps the Auditor must perform)*

```yaml
steps:
  - "<step-1>"
  - "<step-2>"
  - "<step-3>"
```

---

# 12. **Observed Behaviour**  
*(Filled in by Auditor)*

```yaml
observed:
  persona-boundaries:
    - "<observed-persona>"
  lifecycle:
    - "<observed-lifecycle>"
  decor:
    - "<observed-decor>"
  documentation:
    - "<observed-doc>"
  identity:
    - "<observed-identity>"
  namespace:
    - "<observed-namespace>"
  evaluator:
    - "<observed-evaluator>"
  determinism:
    - "<observed-determinism>"
  replay:
    - "<observed-replay>"
```

---

# 13. **Validation Result**

```yaml
result:
  status: "Pass|Fail"
  notes:
    - "<note>"
```

---

# 14. **Auditor Notes**

```yaml
auditor-notes:
  - "<note>"
```

---

# 15. **Verifier Notes**

```yaml
verifier-notes:
  - "<note>"
```

---

# 16. **Change Log**

```yaml
changelog:
  - version: "<v2.4.x>"
    date: "<YYYY-MM-DD>"
    changes:
      - "<change>"
    updated-by: "<persona>"
```

---