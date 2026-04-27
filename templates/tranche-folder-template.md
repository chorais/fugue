# **tranche-folder-template.md (v2.4 — Namespace‑Aligned)**  
**Tranche Folder Template — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Persona: Conductor (Author), Auditor (Validator)  
Lifecycle: Phase 1 → Phase 6  
Authority: Lifecycle Contract (v2.4), Naming Scheme Contract (v2.4), Namespace Scheme Contract (v2.4)

---

# 0. Metadata

```yaml
metadata:
  template-id: "tranche-folder-template"
  version: "2.4"
  authoritative: true

  applies-to:
    - tranche-folders
    - tranche-structure
    - tranche-namespaces
    - tranche-identity
    - tranche-governance

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  lifecycle-phase: "all"
  persona: "conductor|auditor"

  last-updated: "<YYYY-MM-DD>"
```

---

# 1. Purpose

```yaml
purpose: >
  This template defines the canonical directory and file structure for a Fugue
  tranche (v2.4). It ensures deterministic placement, namespace correctness,
  identity propagation, governance alignment, and reproducibility across all
  lifecycle phases. All folder paths MUST use <tranche-name> as defined by the
  Naming Scheme Contract (v2.4).
```

---

# 2. Canonical Directory Structure  
*(Aligned with Namespace Scheme Contract — category-based namespaces)*

A tranche’s artefacts MUST be distributed across category namespaces using:

```
/fugue_docs/<category>/<tranche-name>/
```

Where:

- `<category>` is one of the governed categories  
- `<tranche-name>` is the semantic tranche name defined by the naming scheme  

---

## **2.1 Governance Namespace**

```
/fugue_docs/governance/<tranche-name>/
│
└── tranche.md
```

This is the tranche contract itself.

---

## **2.2 DECOR Namespace**

```
/fugue_docs/decors/<tranche-name>/
│
├── decor.md
├── reconciled-decor.md
└── decor-updates/
```

---

## **2.3 Tickets Namespace**

```
/fugue_docs/tickets/<tranche-name>/
│
├── ticket-map.md
└── T<number>.md
```

---

## **2.4 Logs Namespace**

```
/fugue_docs/logs/<tranche-name>/
│
├── orchestration-log.md
├── lifecycle-log.md
└── implementation-log.md
```

This replaces the old “implementation namespace”.

---

## **2.5 Replay Namespace**

```
/fugue_docs/replay/<tranche-name>/
│
└── <ticket-id>-replay-trace.json
```

---

## **2.6 Verification Namespace**

```
/fugue_docs/verification/<tranche-name>/
│
├── drift/
│   ├── drift-summary.md
│   ├── drift-index.md
│   └── drift-surfaces/
│       └── drift-<id>.md
│
├── tests/
│   ├── dark/
│   ├── golden/
│   ├── governance/
│   └── replay/
│
└── results/
    └── <test-id>-result.json
```

This replaces the old “verification + reconciliation” split.

---

## **2.7 Closure Namespace**

```
/fugue_docs/closure/<tranche-name>/
│
├── closure-log.md
├── epilogue-actions.md
└── tranche-summary.md
```

---

## **2.8 Runtime Namespace**

```
/fugue_docs/runtime/<tranche-name>/
│
├── diagrams/
└── metadata/
```

---

## **2.9 Testing Namespace**

```
/fugue_docs/testing/<tranche-name>/
│
├── test-docs/
└── test-metadata/
```

---

## **2.10 Integration Namespace**

```
/fugue_docs/integration/<tranche-name>/
│
├── integration-docs/
└── integration-metadata/
```

---

## **2.11 Architecture Namespace**

```
/fugue_docs/architecture/<tranche-name>/
│
├── adrs/
├── diagrams/
└── concepts/
```

---

## **2.12 Concerns Namespace**

```
/fugue_docs/concerns/<tranche-name>/
│
└── DC-<number>.md
```

---

## **2.13 Archive Namespace**

```
/fugue_docs/archive/<tranche-name>/
```

Used only for immutable historical artefacts.

---

# 3. Category Definitions  
*(From Namespace Scheme Contract v2.4)*

Valid categories:

```
governance
specs
decors
tickets
logs
replay
verification
closure
runtime
testing
integration
architecture
concerns
archive
```

A tranche MUST use:

- governance  
- decors  
- tickets  
- logs  
- replay  
- verification  
- closure  
- runtime  
- testing  
- integration  
- architecture  
- concerns  
- archive  

---

# 4. Identity & Namespace Requirements

```yaml
identity:
  rules:
    - "Every file MUST include identity metadata."
    - "Identity lineage MUST propagate across all phases."
    - "Identity MUST NOT be regenerated."

namespaces:
  rules:
    - "All artefacts MUST be stored under /fugue_docs/<category>/<tranche-name>/"
    - "No /tranches/ folder is permitted."
    - "No numeric tranche identifiers are permitted."
    - "Namespace MUST reflect the semantic tranche name."
```

---

# 5. Determinism Requirements

```yaml
determinism:
  ordering:
    - "Folder creation MUST follow lifecycle order."
  propagation:
    - "Metadata, identity, and namespace MUST propagate deterministically."
  replay:
    - "Verification artefacts MUST support deterministic replay."
```

---

# 6. Summary

```yaml
summary: >
  The Tranche Folder Template (v2.4) defines the canonical category-based
  namespace structure for all tranches. It ensures deterministic placement,
  governance alignment, identity and namespace correctness, and reproducibility
  across all lifecycle phases. All paths MUST use <tranche-name> as defined by
  the Naming Scheme Contract (v2.4).
```

---
