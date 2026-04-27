# **tranche.md (v2.4)**  
**Tranche Template — Tranche <X.Y>**  
Persona: Conductor (Author)  
Mode: Orchestration Mode  
Lifecycle Phase: Phase 1 → Phase 2  
Authority: Canonical Tranche Template (v2.4)  

---

# 0. Metadata  
*(Fully aligned with all v2.4 governance envelopes and contracts)*

```yaml
metadata:
  tranche: "<X.Y>"
  version: "v2.4"
  status: "Draft|Active|Closed"

  # Governance surfaces
  governance-envelope: "<id>"
  determinism-envelope: "<id>"
  documentation-envelope: "<id>"
  identity-propagation-contract: "<id>"
  namespace-scheme-contract: "<id>"
  lifecycle-contract: "<id>"
  ticket-map-contract: "<id>"
  evaluator-contract: "<id>"
  replay-trace-contract: "<id>"

  # Naming / Namespace / Identity
  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  # Persona lineage
  initiator: "<persona-id>"
  conductor: "<persona-id>"
  architect: "<persona-id>"
  auditor: "<persona-id>"
  verifier: "<persona-id>"

  # Lifecycle
  lifecycle-phase: "intake|orchestration|implementation|verification|reconciliation|closure"
  lifecycle-context: "phase-1→phase-2"

  # DECOR lineage
  decor:
    source: "decors/<X.Y>/decor.md"
    updates: "decors/<X.Y>/decor-updates/"
    reconciled: "decors/<X.Y>/reconciled-decor.md"

  # Ticket Map lineage
  ticket-map: "tickets/<X.Y>/ticket-map.md"

  # Status
  last-updated: "<YYYY-MM-DD>"
```

---

# 1. **Tranche Summary**

```yaml
summary: >
  <One-sentence description of the tranche mission and scope.>
```

---

# 2. **Mission**  
*(Derived from Sponsor Preamble — no new reasoning)*

```yaml
mission: >
  <Describe the tranche mission as defined in the preamble.>
```

---

# 3. **Scope**

```yaml
scope:
  in-scope:
    - "<item>"
    - "<item>"
  out-of-scope:
    - "<item>"
    - "<item>"
```

---

# 4. **Boundaries**

```yaml
boundaries:
  structural:
    - "<boundary>"
  architectural:
    - "<boundary>"
  governance:
    - "<boundary>"
  identity:
    - "<boundary>"
  namespace:
    - "<boundary>"
```

---

# 5. **Acceptance Criteria**

```yaml
acceptance-criteria:
  tranche-level:
    - "<criterion>"
  governance:
    - "<governance-criterion>"
  determinism:
    - "<determinism-criterion>"
  documentation:
    - "<documentation-criterion>"
  identity-propagation:
    - "<identity-criterion>"
  namespace:
    - "<namespace-criterion>"
```

---

# 6. **Lifecycle Alignment**

```yaml
lifecycle:
  phase-1-intake:
    - "<intake-output>"
  phase-2-orchestration:
    - "<orchestration-output>"
  phase-3-implementation:
    - "<implementation-output>"
  phase-4-verification:
    - "<verification-output>"
  phase-5-reconciliation:
    - "<reconciliation-output>"
  phase-6-closure:
    - "<closure-output>"
```

---

# 7. **DECOR Surfaces**  
*(Required by DECOR Specification v2.4)*

```yaml
decor-surfaces:
  design:
    - "<D-001>"
  considerations:
    - "<C-002>"
  risks:
    - "<R-003>"
  opportunities:
    - "<O-004>"
  open-questions:
    - "<Q-005>"
  constraints:
    - "<K-006>"
  invariants:
    - "<I-007>"
```

---

# 8. **Architect Fill Phase Requirements**  
*(Required when DECOR surfaces declare `content-required: true`)*

```yaml
architect-fill-phase:
  required: <true|false>
  surfaces:
    - "<decor-surface>"
  expected-output:
    - "<conceptual-artefact>"
  metadata:
    - "<metadata-rule>"
  identity-propagation:
    - "<identity-rule>"
  namespaces:
    - "<namespace-rule>"
```

---

# 9. **Ticket Map Summary**  
*(Derived from Ticket Map Contract v2.4)*

```yaml
ticket-map:
  total-tickets: <N>
  governance-tickets:
    - "ticket-<X.Y.N>"
  implementation-tickets:
    - "ticket-<X.Y.M>"
  architect-fill-tickets:
    - "ticket-<X.Y.K>"
  determinism-critical:
    - "ticket-<X.Y.D>"
  documentation-required:
    - "ticket-<X.Y.DR>"
```

---

# 10. **Dependencies & Sequencing**

```yaml
dependencies:
  cross-tranche:
    - "<dependency>"
  governance:
    - "<governance-dependency>"
  determinism:
    - "<determinism-dependency>"
  identity-propagation:
    - "<identity-dependency>"
  namespace:
    - "<namespace-dependency>"
```

---

# 11. **Documentation Surfaces**

```yaml
documentation:
  required: <true|false>
  surfaces:
    - "<doc-surface>"
  placement:
    - "/fugue_docs/<X.Y>/..."
  metadata:
    - "<metadata-rule>"
  naming:
    - "<naming-rule>"
  namespaces:
    - "<namespace-rule>"
```

---

# 12. **Evaluator Surfaces**

```yaml
evaluator:
  categories:
    - "<category>"
  determinism:
    - "<determinism-rule>"
  diagnostics:
    - "<diagnostic-rule>"
```

---

# 13. **Determinism Surfaces**

```yaml
determinism:
  ordering:
    - "<ordering-rule>"
  evaluator-behaviour:
    - "<evaluator-rule>"
  metadata-propagation:
    - "<metadata-rule>"
  identity-propagation:
    - "<identity-rule>"
  replay-traces:
    - "<trace-rule>"
```

---

# 14. **Identity & Namespace Surfaces**

```yaml
identity:
  lineage:
    - "<identity-event>"
  propagation:
    - "<identity-rule>"

namespaces:
  placement:
    - "<namespace-rule>"
  invariants:
    - "<namespace-invariant>"
```

---

# 15. **Risks & Considerations**

```yaml
risks:
  tranche-risks:
    - "<risk>"
  governance-risks:
    - "<governance-risk>"
  determinism-risks:
    - "<determinism-risk>"
  identity-risks:
    - "<identity-risk>"
  namespace-risks:
    - "<namespace-risk>"
```

---

# 16. **Clarifications Needed**

```yaml
clarifications:
  sponsor:
    - "<clarification>"
  architect:
    - "<clarification>"
  governance:
    - "<clarification>"
  decor:
    - "<clarification>"
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