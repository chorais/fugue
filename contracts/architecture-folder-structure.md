# **architecture-folder-structure.md (v2.4)**  
**Architecture Folder Structure Contract**  
Version: 2.4  
Governance Authority: Curator  
Personas Bound: Architect, Implementer, Orchestrator  
Lifecycle: All Phases  

---

# 0. Metadata

| Field | Description |
|-------|-------------|
| **Contract Scope** | Folder structure, artefact placement, and naming rules for architecture documentation |
| **Governance Posture** | Architecture MUST be developer‑facing, explanatory, non‑normative, and aligned with DECOR |
| **Identity Propagation Rules** | Architecture MUST align with identity lineage rules defined in tranche preambles |
| **Contract Status** | Draft / Active |

---

# 1. Contract Purpose  
This contract defines the governed structure for all architecture documentation.

Architecture documentation MUST:

- be developer‑facing  
- be explanatory  
- be conceptual  
- be non‑normative  
- be authored by the Architect  
- be aligned with DECOR  
- be aligned with the documentation envelope  

Architecture documentation MUST NOT:

- introduce invariants  
- introduce constraints  
- introduce governance envelopes  
- contradict DECOR  
- contradict governance posture  

---

# 2. Architecture Folder Namespace  
Architecture documentation MUST be stored under:

```
/fugue_docs/architecture/
```

Architecture documentation MAY be tranche‑scoped or global.

Tranche‑scoped architecture MUST follow:

```
/fugue_docs/architecture/<tranche-name>/
```

Global architecture MUST follow:

```
/fugue_docs/architecture/global/
```

Architecture namespaces MUST NOT:

- include persona identifiers  
- include numeric versioning semantics  
- include implementation detail  

---

# 3. Architecture Subfolders  
The architecture folder MUST contain the following governed subfolders:

### 3.1 ADRs  
```
/fugue_docs/architecture/<scope>/adrs/
```

### 3.2 Diagrams  
```
/fugue_docs/architecture/<scope>/diagrams/
```

### 3.3 Conceptual Documentation  
```
/fugue_docs/architecture/<scope>/concepts/
```

### 3.4 Notes  
```
/fugue_docs/architecture/<scope>/notes/
```

Where `<scope>` MUST be either:

- `<tranche-name>`  
- `global`  

Architecture subfolders MUST NOT include additional categories.

---

# 4. ADR Placement Rules  
ADRs MUST be stored under:

```
/fugue_docs/architecture/<scope>/adrs/
```

ADRs MUST follow the naming scheme:

```
ADR-<number>.md
```

ADRs MUST:

- be authored by the Architect  
- be developer‑facing  
- be explanatory  
- be non‑normative  
- reference DECOR where relevant  

ADRs MUST NOT:

- contradict DECOR  
- introduce invariants  
- introduce constraints  
- introduce governance envelopes  

---

# 5. Diagram Placement Rules  
Diagrams MUST be stored under:

```
/fugue_docs/architecture/<scope>/diagrams/
```

Diagrams MUST:

- be developer‑facing  
- be conceptual  
- be explanatory  
- be aligned with DECOR  

Diagrams MUST NOT:

- introduce normative content  
- contradict DECOR  
- contradict governance posture  

Diagram filenames MUST be deterministic and descriptive.

---

# 6. Conceptual Documentation Rules  
Conceptual documentation MUST be stored under:

```
/fugue_docs/architecture/<scope>/concepts/
```

Conceptual documentation MUST:

- describe architectural concepts  
- describe structural relationships  
- describe developer‑facing mental models  

Conceptual documentation MUST NOT:

- introduce normative requirements  
- contradict DECOR  
- contradict governance posture  

---

# 7. Notes Rules  
Notes MUST be stored under:

```
/fugue_docs/architecture/<scope>/notes/
```

Notes MUST:

- be developer‑facing  
- be explanatory  
- be non‑normative  

Notes MUST NOT:

- modify DECOR  
- modify governance posture  
- introduce invariants or constraints  

---

# 8. Tranche‑Scoped vs Global Architecture  
Architecture MAY be:

### 8.1 Tranche‑Scoped  
Stored under:

```
/fugue_docs/architecture/<tranche-name>/
```

Tranche‑scoped architecture MUST:

- relate to a specific tranche  
- reference the tranche DECOR  
- reference tranche tickets  

### 8.2 Global  
Stored under:

```
/fugue_docs/architecture/global/
```

Global architecture MUST:

- relate to system‑wide concepts  
- relate to cross‑tranche structures  
- relate to long‑term architectural posture  

---

# 9. Lifecycle Integration  
Architecture documentation MUST integrate with lifecycle phases as follows:

### 9.1 Orchestration  
- Architect MAY produce architecture documentation  
- Architecture MUST align with DECOR  

### 9.2 Implementation  
- Implementer MAY reference architecture documentation  
- Implementer MUST NOT modify architecture documentation  

### 9.3 Verification  
- Auditor MUST confirm architecture documentation does not contradict DECOR  
- Verifier MUST confirm architecture documentation is non‑normative  

### 9.4 Closure  
- Curator MUST confirm architecture documentation is complete for the tranche  

---

# 10. Identity Propagation  
Architecture documentation MUST:

- propagate tranche identity  
- propagate artefact identity  
- propagate ADR identity  
- propagate diagram identity  

Architecture documentation MUST NOT:

- introduce naming drift  
- contradict identity propagation rules  

---

# 11. Contract Outputs  
This contract MUST produce:

- deterministic architecture folder structure  
- deterministic ADR placement rules  
- deterministic diagram placement rules  
- deterministic conceptual documentation rules  
- deterministic notes rules  
- deterministic tranche/global scoping rules  
- deterministic lifecycle integration rules  

These rules MUST be applied across:

- orchestration  
- implementation  
- verification  
- closure  
- archival  
