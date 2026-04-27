# **ticket-map.md (v2.4)**  
**Ticket Map Template — Fugue Orchestration Method**  
Version: 2.4  
Status: Draft → Active  
Persona: Conductor (Author)  
Lifecycle: Phase 2 — Orchestration  
Namespace: `/fugue_docs/tickets/<tranche-name>/`  
Authority: Ticket Map Contract (v2.4)  

---

# 0. Metadata

```yaml
metadata:
  tranche-name: "<tranche-name>"
  version: "v2.4"
  status: "Draft|Active"

  # Governance Contracts
  ticket-map-contract: "v2.4"
  decor-contract: "v2.4"
  reconciled-decor-contract: "v2.4"
  lifecycle-contract: "v2.4"
  naming-scheme-contract: "v2.4"
  namespace-scheme-contract: "v2.4"
  identity-propagation-contract: "v2.4"
  documentation-envelope: "v2.4"
  determinism-envelope: "v2.4"

  # Persona Lineage
  conductor: "<persona-id>"
  architect: "<persona-id>"
  implementer: "<persona-id>"
  auditor: "<persona-id>"
  verifier: "<persona-id>"

  # Lifecycle
  lifecycle-phase: "orchestration"
  lifecycle-context: "phase-2"

  # DECOR Lineage
  decor:
    source: "/fugue_docs/decors/<tranche-name>/decor.md"
    updates: "/fugue_docs/decors/<tranche-name>/decor-updates/"
    reconciled: "/fugue_docs/decors/<tranche-name>/reconciled-decor.md"

  # Ticket Namespace
  ticket-namespace: "/fugue_docs/tickets/<tranche-name>/"

  last-updated: "<YYYY-MM-DD>"
```

---

# 1. Ticket Map Summary

```yaml
summary: >
  <One-sentence description of the tranche execution plan, grounded in DECOR and
  aligned with the tranche mission, boundaries, and acceptance criteria.>
```

---

# 2. Ticket Index

A deterministic, ordered list of all tickets in this tranche.

```yaml
tickets:
  - id: "<ticket-id>"
    title: "<short-title>"
    persona: "architect|implementer|hybrid"
    requires-fill: <true|false>
    dependencies:
      - "<ticket-id>"
    decor:
      categories:
        - "<D|C|O|R|Q|K|I>"
      surfaces:
        - "<decor-surface-id>"
    documentation:
      required: <true|false>
      surfaces:
        - "<doc-surface>"
    determinism:
      critical: <true|false>
    namespace:
      path: "/fugue_docs/tickets/<tranche-name>/<ticket-id>.md"
    identity:
      lineage: "<identity-token>"
```

Repeat the block above for each ticket.

---

# 3. Ticket Definitions

Each ticket MUST have its own section.

---

## **3.N Ticket `<ticket-id>`**

```yaml
id: "<ticket-id>"
title: "<short-title>"
persona: "architect|implementer|hybrid"
requires-fill: <true|false>

description: >
  <Detailed description of the ticket intent, grounded in DECOR and aligned with
  tranche mission, boundaries, and acceptance criteria.>

decor:
  categories:
    - "<D|C|O|R|Q|K|I>"
  surfaces:
    - "<decor-surface-id>"
  metadata:
    content-required: <true|false>
    implementation-required: <true|false>
    architect-required: <true|false>

dependencies:
  required:
    - "<ticket-id>"
  transitive:
    - "<ticket-id>"

documentation:
  required: <true|false>
  surfaces:
    - "<doc-surface>"
  placement:
    - "/fugue_docs/<category>/<tranche-name>/..."

determinism:
  ordering:
    - "<ordering-rule>"
  evaluator:
    - "<evaluator-rule>"
  replay:
    - "<replay-rule>"

identity:
  lineage: "<identity-token>"
  propagation:
    - "<identity-propagation-rule>"

namespace:
  path: "/fugue_docs/tickets/<tranche-name>/<ticket-id>.md"
  invariants:
    - "<namespace-invariant>"

acceptance:
  conditions:
    - "<condition>"
  governance:
    - "<governance-condition>"
  documentation:
    - "<documentation-condition>"
  determinism:
    - "<determinism-condition>"
```

---

# 4. Dependency Graph

```yaml
dependency-graph:
  nodes:
    - "<ticket-id>"
  edges:
    - "<ticket-id> -> <ticket-id>"
  acyclic: <true|false>
  notes: >
    <Explanation of dependency structure and rationale.>
```

---

# 5. Persona Routing Summary

```yaml
persona-routing:
  architect:
    - "<ticket-id>"
  implementer:
    - "<ticket-id>"
  hybrid:
    - "<ticket-id>"
```

---

# 6. Requires‑Fill Summary

```yaml
requires-fill:
  true:
    - "<ticket-id>"
  false:
    - "<ticket-id>"
```

---

# 7. Documentation Requirements Summary

```yaml
documentation:
  required:
    - "<ticket-id>"
  optional:
    - "<ticket-id>"
  surfaces:
    - "<doc-surface>"
```

---

# 8. Determinism Surfaces

```yaml
determinism:
  critical:
    - "<ticket-id>"
  ordering:
    - "<ordering-rule>"
  evaluator:
    - "<evaluator-rule>"
  replay:
    - "<replay-rule>"
```

---

# 9. Identity & Namespace Summary

```yaml
identity:
  lineage:
    - "<ticket-id>: <identity-token>"
  propagation:
    - "<identity-propagation-rule>"

namespace:
  paths:
    - "/fugue_docs/tickets/<tranche-name>/<ticket-id>.md"
  invariants:
    - "<namespace-invariant>"
```

---

# 10. Governance Notes

```yaml
governance:
  invariants:
    - "<governance-invariant>"
  risks:
    - "<risk>"
  mitigations:
    - "<mitigation>"
  audit:
    - "<audit-note>"
```

---

# 11. Change Log

```yaml
changelog:
  - version: "<v2.4.x>"
    date: "<YYYY-MM-DD>"
    changes:
      - "<change>"
    updated-by: "<persona>"
```

---
