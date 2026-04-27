# **naming-scheme-contract.md (v2.4)**  
**Naming Scheme Governance Contract**  
Version: 2.4  
Governance Authority: Curator  
Personas Bound: All Personas  
Lifecycle: All Phases  

---

# 0. Metadata
```yaml
metadata:
  contract-id: "naming-scheme-contract"
  version: "2.4"
  authoritative: true

  applies-to:
    - naming-rules
    - tranche-names
    - ticket-names
    - artefact-names
    - folder-names
    - namespace-names
    - adr-names
    - concern-names

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  governance-envelope: "<id>"
  documentation-envelope: "<id>"
  determinism-envelope: "<id>"
  lifecycle-contract: "<id>"
  ticket-map-contract: "<id>"
  replay-trace-contract: "<id>"
```

# Placeholder Semantics
# Fields containing "<id>" or "<self>" are canonical placeholders.
# They MUST be concretised in project/branch/theme/tranche governance envelopes.
# They MUST NOT be replaced in methodology-level contracts.
# The Auditor Persona MUST treat these placeholders as intentional and NOT as metadata drift.

---

# 1. Contract Purpose  
This contract defines the governed naming system for all Fugue artefacts.

The naming system MUST:

- ensure deterministic identity  
- ensure stable lineage  
- ensure unambiguous referencing  
- ensure semantic expressiveness  
- ensure human readability  
- ensure machine parseability  
- ensure archival suitability  

The naming system MUST NOT:

- encode implementation detail  
- encode persona identity  
- encode ephemeral context  
- rely on numeric versioning semantics  
- rely on implicit ordering  

---

# 2. Naming Principles  
All names in Fugue MUST satisfy:

- determinism  
- stability  
- unambiguity  
- semantic expressiveness  
- human readability  
- machine parseability  
- governance alignment  
- identity propagation alignment  
- archival suitability  

Names MUST NOT:

- introduce naming drift  
- contradict governance posture  
- contradict identity propagation rules  

---

# 3. Tranche Naming Rules  
A tranche name MUST be:

- semantic  
- expressive  
- human‑readable  
- stable across the lifecycle  
- unique within the branch  
- aligned with the tranche mission  

A tranche name MUST follow the structure:

```
<branch>.<theme>.<semantic-name>
```

Where:

- **branch** = stable project lineage identifier  
- **theme** = high‑level thematic grouping  
- **semantic-name** = deterministic, descriptive name for the tranche  

Tranche names MUST NOT:

- include the prefix “tranche‑”  
- include numeric versioning semantics  
- include ticket identifiers  
- include persona identifiers  

---

# 4. Ticket Naming Rules  
Ticket names MUST be:

- short  
- structured  
- deterministic  
- persona‑neutral  
- stable  

Ticket names MUST follow:

```
T<number>
```

Supplementary ticket types MUST follow:

```
C<number>   (conceptual)
E<number>   (epilogue)
```

Ticket names MUST NOT:

- include tranche names  
- include semantic descriptors  
- include implementation detail  
- include persona identifiers  

---

# 5. Folder Naming Rules  
Folder names MUST be:

- semantic  
- human‑readable  
- aligned with tranche names  
- aligned with documentation envelope structure  

Folder names MUST follow:

```
/fugue_docs/<category>/<name>/
```

Where **category** MUST be one of:

- 'project'
- 'branches'
- 'themes'
- 'governance'
- 'specs'
- 'decors'
- 'tickets'
- 'logs'
- 'replay'
- 'verification'
- 'closure'
- 'runtime'
- 'testing'
- 'integration'
- 'architecture'
- 'concerns'
- 'archive'

Where:

- 'project' = project‑level governance artefacts
- 'branches' = branch‑level governance artefacts
- 'themes' = theme‑level governance artefacts

all other categories = tranche‑level governed categories

Folder names MUST NOT:
- include the prefix “tranche‑”
- include numeric identifiers unrelated to the tranche
- include persona identifiers

---

# 6. Artefact Naming Rules  
Artefact names MUST be:

- deterministic  
- aligned with their category  
- aligned with their ticket or tranche  
- stable across the lifecycle  

### 6.1 Tranche‑level artefacts MUST follow:

```
decor.md
reconciled-decor.md
metadata.json
preamble.md
preamble-interpretation.md
ticket-map.md
```

### 6.2 Ticket‑level artefacts MUST follow:

```
<ticket-id>-implementation-log.md
<ticket-id>-verification-log.md
<ticket-id>-replay-trace.json
```

### 6.3 ADR artefacts MUST follow:

```
ADR-<number>.md
```

### 6.4 Concern artefacts MUST follow:

```
DC-<number>.md
```

Artefact names MUST NOT:

- include semantic descriptors  
- include persona identifiers  
- include ephemeral context  

---

# 7. Namespace Rules  
Namespaces MUST:

- reflect tranche names  
- reflect artefact categories  
- be deterministic  
- be stable  
- be human‑readable  

Namespaces MUST follow:

```
/fugue_docs/<category>/<tranche-name>/
```

Global concerns and global ADRs MAY follow:

```
/fugue_docs/concerns/
 /fugue_docs/architecture/adrs/
```

Namespaces MUST NOT:

- include numeric versioning semantics  
- include persona identifiers  
- include implementation detail  

---

# 8. ADR Rules  
ADRs MUST:

- be authored by the Architect  
- be developer‑facing  
- be non‑authoritative  
- be explanatory, not normative  
- reference DECOR where relevant  
- never contradict DECOR  
- never introduce invariants  
- never introduce constraints  
- never introduce governance envelopes  

ADRs MUST be stored under:

```
/fugue_docs/architecture/<tranche-name>/adrs/
```

or, if global:

```
/fugue_docs/architecture/adrs/
```

---

# 9. Concern Rules  
Concerns MUST:

- be raised by Implementer or user  
- be triaged by Architect  
- be scheduled by Orchestrator  
- be resolved by a future ticket  
- be non‑blocking  
- be forward‑looking  
- be developer‑facing  
- be cross‑tranche  

Concerns MUST include:

- concern ID  
- detected during  
- severity  
- status  
- summary  
- rationale  
- draft follow‑up ticket  
- business requirements  
- technical requirements  
- acceptance criteria  

Concerns MUST be stored under:

```
/fugue_docs/concerns/
```

---

# 10. Ordering Rules  
Ordering MUST be:

- explicit  
- deterministic  
- metadata‑driven  

Ordering MUST NOT:

- be encoded in names  
- rely on numeric prefixes  
- rely on implicit sequence semantics  

Ordering MUST be expressed through:

- metadata  
- Ticket Map  
- DECOR metadata  
- orchestration sequencing  

---

# 11. Identity Propagation Rules  
Naming MUST align with identity propagation rules defined in tranche preambles.

Identity propagation MUST ensure:

- stable lineage  
- deterministic referencing  
- unambiguous cross‑tranche linking  
- compatibility with reconciled DECOR  
- compatibility with GC  

Identity propagation MUST NOT:

- introduce naming drift  
- weaken governance envelopes  
- contradict tranche naming rules  

---

# 12. Archival Naming Rules  
Archived tranches MUST follow:

```
/fugue/archive/tranches/<tranche-name>/
```

Archived artefacts MUST preserve:

- original names  
- original structure  
- original metadata  

Archival MUST NOT:

- rename artefacts  
- rename folders  
- modify lineage  

---

# 13. Migration Rules  
When migrating from legacy naming (e.g., `tranche-X.8.6`), migration MUST:

- preserve lineage  
- preserve metadata  
- preserve artefact identity  
- remove redundant prefixes  
- convert numeric identifiers to semantic names  
- update references deterministically  

Migration MUST NOT:

- alter artefact content  
- alter DECOR  
- alter governance posture  

---

# 14. Contract Outputs  
This contract MUST produce:

- deterministic tranche naming rules  
- deterministic ticket naming rules  
- deterministic folder naming rules  
- deterministic artefact naming rules  
- deterministic namespace rules  
- deterministic ADR rules  
- deterministic concern rules  
- deterministic archival rules  
- deterministic migration rules  

These rules MUST be applied across:

- orchestration  
- implementation  
- verification  
- closure  
- archival  