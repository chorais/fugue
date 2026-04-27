# **test-folder-structure.md (v2.4)**  
**Test Folder Structure Template — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Authority: Namespace Scheme Contract (v2.4)  
Scope: All Governed Test Artefacts  
Lifecycle: Verification (Phase 4)  
Persona: Auditor → Verifier  

---

# 1. Purpose

This template defines the **canonical directory structure** for all governed test artefacts in Fugue v2.4.

It ensures:

- deterministic placement  
- deterministic retrieval  
- deterministic verification  
- deterministic replay  
- persona‑safe boundaries  
- governance‑safe storage  
- audit‑ready structure  
- namespace correctness  
- identity propagation correctness  

This structure MUST be used for **every tranche**, without modification.

---

# 2. Root Placement

All governed test artefacts MUST be placed under:

```
/fugue_docs/verification/<tranche-name>/
```

Where:

- `<tranche-name>` is defined by the **Naming Scheme Contract (v2.4)**  
- the namespace is **category‑based**, not tranche‑based  
- the folder is **governed**  
- the lifecycle is **Phase 4 — Verification**  

This namespace is owned by:

- Persona: **Auditor → Verifier**  
- Lifecycle: **Verification**  

---

# 3. Canonical Test Folder Structure (v2.4)

```
/fugue_docs/verification/<tranche-name>/
│
├── tests/
│   ├── dark/
│   │   └── dark-test-<id>.md
│   ├── golden/
│   │   └── golden-test-<id>.md
│   ├── governance/
│   │   └── governance-test-<id>.md
│   └── replay/
│       └── replay-test-<id>.md
│
├── suite/
│   ├── test-suite-index.md
│   └── test-metadata.json
│
├── results/
│   ├── dark/
│   │   └── dark-test-<id>-result.json
│   ├── golden/
│   │   └── golden-test-<id>-result.json
│   ├── governance/
│   │   └── governance-test-<id>-result.json
│   └── replay/
│       └── replay-test-<id>-result.json
│
├── logs/
│   ├── test-run-log.md
│   ├── evaluator-diagnostics/
│   │   └── <diagnostic-file>.json
│   └── replay-diagnostics/
│       └── <replay-diagnostic>.json
│
├── drift/
│   ├── drift-summary.md
│   ├── drift-index.md
│   └── drift-surfaces/
│       └── drift-<id>.md
│
└── archive/
    └── <archived-test>.md
```

---

# 4. Directory‑Level Governance Rules

## 4.1 `/tests/`
Persona: **Auditor**  
Lifecycle: **Verification**  
Governance: **Strictly governed**

Contains:

- canonical test instances  
- one file per test  
- no results  
- no logs  

Subfolders:

- `/dark/` — failure mode tests  
- `/golden/` — ideal behaviour tests  
- `/governance/` — governance alignment tests  
- `/replay/` — replay determinism tests  

Each MUST contain only `.md` test files.

---

## 4.2 `/suite/`
Persona: **Auditor → Verifier**  
Lifecycle: **Verification**  
Governance: **Strictly governed**

Contains:

- `test-suite-index.md`  
- `test-metadata.json`  

These define the **structure** and **metadata** of the governed test suite.

---

## 4.3 `/results/`
Persona: **Auditor**  
Lifecycle: **Verification**  
Governance: **Governed**

Contains:

- JSON results for each test  
- one result file per test instance  
- separated by test type  

---

## 4.4 `/logs/`
Persona: **Auditor**  
Lifecycle: **Verification**  
Governance: **Governed**

Contains:

- test run logs  
- evaluator diagnostics  
- replay diagnostics  

These support:

- replay determinism  
- evaluator correctness  
- drift classification  

---

## 4.5 `/drift/`
Persona: **Auditor → Verifier**  
Lifecycle: **Verification → Reconciliation**  
Governance: **Strictly governed**

Contains:

- drift summary  
- drift index  
- drift surfaces  

These are required by:

- Drift Schema  
- Test Suite Contract  
- Test Engine Contract  

---

## 4.6 `/archive/`
Persona: **Curator**  
Lifecycle: **Global**  
Governance: **Strictly governed**

Contains:

- archived test artefacts  
- deprecated test structures  

Archived artefacts MUST preserve:

- identity  
- metadata  
- namespace  

---

# 5. Determinism Rules

The test folder structure MUST be:

- deterministic  
- stable  
- reproducible  
- identity‑aligned  
- namespace‑aligned  

Folders MUST NOT:

- be created dynamically  
- be renamed without governance approval  
- contain mixed test types  
- contain ungoverned artefacts  

---

# 6. Identity & Namespace Rules

Every test artefact MUST:

- preserve identity lineage  
- preserve namespace lineage  
- follow the Namespace Scheme Contract  
- follow the Identity Propagation Contract  

Identity MUST NOT:

- drift  
- be regenerated  
- be inferred  

---

# 7. Lifecycle Rules

All test artefacts MUST align with:

```
Lifecycle Phase: Phase 4 — Verification
Persona: Auditor → Verifier
```

Tests MUST NOT be executed or stored during:

- Orchestration  
- Implementation  
- Reconciliation  
- Closure  

---
