# **ticket.md (v2.4)**  
**Ticket Template — `<tranche-name>`**  
Persona: Conductor (Author)  
Mode: Orchestration Mode  
Lifecycle Phase: Phase 2 — Orchestration  
Authority: Canonical Ticket Template (v2.4)  
Namespace: `/fugue_docs/tickets/<tranche-name>/`  

---

# 0. Metadata  
*(Fully aligned with all v2.4 governance envelopes and contracts)*

```yaml
metadata:
  ticket-id: "<ticket-id>"
  tranche-name: "<tranche-name>"

  # DECOR lineage
  decor-source: "/fugue_docs/decors/<tranche-name>/decor.md"
  decor-updates:
    - "/fugue_docs/decors/<tranche-name>/decor-updates/<update-id>.md"
  reconciled-decor-source: "/fugue_docs/decors/<tranche-name>/reconciled-decor.md"
  decor-ids:
    - "<D-001>"
    - "<C-002>"
    - "<R-003>"

  # Persona routing (v2.4 — no hybrid unless justified)
  persona-routing: "implementer|architect"
  persona-routing-summary: "Conductor→Implementer|Architect"

  # Governance surfaces
  governance-envelope: "<id>"
  documentation-envelope: "<id>"
  determinism-envelope: "<id>"
  identity-propagation-contract: "<id>"
  namespace-scheme-contract: "<id>"
  evaluator-contract: "<id>"
  replay-trace-contract: "<id>"
  lifecycle-contract: "<id>"

  # Naming / Namespace / Identity Propagation
  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  # Ticket behaviour
  requires-fill: <true|false>
  method: "A|B"
  documentation-required: <true|false>
  governance-critical: <true|false>
  determinism-critical: <true|false>
  risk-critical: <true|false>

  # Dependencies
  dependencies:
    explicit:
      - "<ticket-id>"
    transitive:
      - "<ticket-id>"

  # Lifecycle
  lifecycle-phase: "orchestration"
  lifecycle-context: "phase-2"

  # Status
  status: "Pending|In-Progress|Complete"
  last-updated: "<YYYY-MM-DD>"
```

---

# 1. **Ticket Summary**

```yaml
summary: >
  <One-sentence description of what this ticket accomplishes.>
```

---

# 2. **Intent**  
*(Grounded in DECOR — no new reasoning)*

```yaml
intent: >
  <Describe the architectural, structural, or behavioural intent derived from DECOR.>
```

---

# 3. **DECOR Subset**  
*(Required by Ticket Map Contract v2.4)*

```yaml
decor-subset:
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

# 4. **Acceptance Criteria**  
*(Deterministic, testable, replayable)*

```yaml
acceptance-criteria:
  required:
    - "<criterion-1>"
    - "<criterion-2>"
    - "<criterion-3>"

  determinism:
    ordering: "<deterministic-ordering-rule>"
    evaluator-behaviour: "<deterministic-evaluator-rule>"
    replay-traces:
      - "<required-trace>"
```

---

# 5. **Implementation Requirements**  
*(Only when persona-routing = implementer)*

```yaml
implementation-requirements:
  behaviour:
    - "<required-behaviour>"
  state-transitions:
    - "<required-transition>"
  outputs:
    - "<required-output>"
  logs:
    - "<required-log>"
  replay-traces:
    - "<required-replay-trace>"
  metadata-propagation:
    - "<metadata-rule>"
  identity-propagation:
    - "<identity-rule>"
  naming:
    - "<naming-rule>"
  namespaces:
    - "<namespace-rule>"
```

---

# 6. **Conceptual Requirements**  
*(Only when persona-routing = architect OR requires-fill = true)*

```yaml
conceptual-requirements:
  invariants:
    - "<invariant>"
  constraints:
    - "<constraint>"
  governance-envelopes:
    - "<envelope>"
  identity-propagation:
    - "<identity-rule>"
  naming:
    - "<naming-rule>"
  namespaces:
    - "<namespace-rule>"
  documentation-envelope:
    - "<doc-envelope-rule>"
  determinism-envelope:
    - "<determinism-envelope-rule>"
```

---

# 7. **Documentation Requirements**  
*(Derived from DECOR metadata + Documentation Envelope Contract v2.4)*

```yaml
documentation:
  required: <true|false>
  surfaces:
    - "<doc-surface>"
  placement:
    - "/fugue_docs/<category>/<tranche-name>/..."
  metadata:
    - "<metadata-surface>"
  naming:
    - "<naming-rule>"
  namespaces:
    - "<namespace-rule>"
  evaluator:
    - "<evaluator-doc-requirement>"
```

---

# 8. **Evaluator Metadata**  
*(Required by Evaluator Contract v2.4)*

```yaml
evaluator:
  categories:
    - "<category>"
  diagnostics:
    - "<diagnostic>"
  determinism:
    - "<determinism-rule>"
```

---

# 9. **Dependencies**  
*(Explicit + transitive — enforced by Ticket Map Contract v2.4)*

```yaml
dependencies:
  explicit:
    - "<ticket-id>"
  transitive:
    - "<ticket-id>"
  governance:
    - "<governance-dependency>"
  determinism:
    - "<determinism-dependency>"
  identity-propagation:
    - "<identity-dependency>"
```

---

# 10. **Clarifications Needed**  
*(Used by Implementer to request Architect input)*

```yaml
clarifications:
  general:
    - "<clarification-needed>"
  decor:
    - "<decor-clarification>"
  governance-envelope:
    - "<governance-clarification>"
```

---

# 11. **Implementation Notes (Implementer Persona Only)**  
*(Generated during execution)*

```yaml
implementation-notes:
  logs:
    - "<log-entry>"
  replay-traces:
    - "<trace-entry>"
  surfaced-contradictions:
    - "<contradiction>"
  metadata-propagation:
    - "<metadata-note>"
  identity-propagation:
    - "<identity-note>"
```

---

# 12. **Architect Notes (Architect Persona Only)**  
*(Used when requires-fill = true or DECOR updates occur)*

```yaml
architect-notes:
  conceptual-output:
    - "<conceptual-artefact>"
  decor-updates:
    - "<decor-update-id>"
  identity-updates:
    - "<identity-update>"
  governance-envelope-updates:
    - "<governance-update>"
```

---

# 13. **Auditor Notes (Verification Phase Only)**  
*(Used during drift classification + reconciliation)*

```yaml
auditor-notes:
  drift:
    - "<drift-item>"
  naming-namespace-identity-drift:
    - "<identity-drift>"
  evaluator-drift:
    - "<evaluator-drift>"
  reconciliation:
    - "<reconciliation-note>"
  validated:
    - "<validated-surface>"
```

---

# 14. **Change Log**

```yaml
changelog:
  - version: "<v2.4.x>"
    date: "<YYYY-MM-DD>"
    changes:
      - "<change>"
    updated-by: "<persona>"
```

---
