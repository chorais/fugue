# **branch-bootstrap-workflow.md**  
**Branch Bootstrap Workflow**  
Version: 2.4  
Status: Active  
Purpose: Define the deterministic, persona‑isolated process for creating and initialising a Fugue Branch.  
Methodology: Fugue Orchestration Method  
Implementation: Chorais  

---

# **1. Purpose**

Branch Bootstrap establishes:

- the **Branch Preamble**  
- the **Branch DECOR**  
- the **Branch Governance Envelope**  
- the **Branch Naming Scheme**  
- the **Branch Namespace Scheme**  
- the **Branch Identity Propagation Rules**  
- the **Branch Documentation Envelope**  

A Branch is the **parallel development stream** within a Fugue Project.  
Branch Bootstrap MUST be completed before any Theme can begin.

---

# **2. Preconditions**

Branch Bootstrap may begin only when:

- a **Project** already exists  
- the **Project Bootstrap Workflow** is complete  
- the operator has attached the required contracts  
- no Branch artefacts exist for the given branch name  

Branch Bootstrap MUST NOT begin mid‑branch.

---

# **3. Required Inputs**

The operator MUST attach:

```
/contracts/branch-contract.md
/contracts/persona-boundaries.md
/contracts/methodology-overview.md
/contracts/naming-scheme-contract.md
/contracts/namespace-scheme-contract.md
/contracts/governance-envelope-contract.md
/contracts/identity-propagation-contract.md
/contracts/documentation-envelope.md
/fugue_docs/project/project-decor.md
/fugue_docs/project/governance-envelope.md
```

These files form the **branch bootstrap substrate**.

---

# **4. Branch Bootstrap Overview**

Branch Bootstrap proceeds through the following deterministic phases:

1. **Branch Initiation (Initiator)**  
2. **Branch DECOR Derivation (Architect)**  
3. **Branch Governance Envelope Establishment (Curator)**  
4. **Branch Naming Scheme Definition (Curator)**  
5. **Branch Namespace Scheme Definition (Curator)**  
6. **Branch Identity Propagation Definition (Curator)**  
7. **Branch Documentation Envelope Initialisation (Curator)**  
8. **Branch Bootstrap Log Production (Curator)**  
9. **Branch Approval (Curator)**  

Each phase MUST be completed in order.

---

# **5. Phase 1 — Branch Initiation (Initiator Persona)**

The Initiator Persona MUST:

- produce the **Branch Preamble**  
- define the branch mission  
- define branch boundaries  
- define branch scope  
- define branch risks  
- define branch constraints  
- define branch acceptance criteria  
- define branch success criteria  
- define branch dependencies  

The Initiator MUST NOT:

- define architecture  
- define governance  
- define naming or namespace rules  
- define persona behaviour  
- define DECOR  

Output MUST be written to:

```
/fugue_docs/branches/<branch-name>/preamble.md
```

---

# **6. Phase 2 — Branch DECOR Derivation (Architect Persona)**

The Architect Persona MUST:

- derive **Branch DECOR** from the Branch Preamble  
- incorporate constraints from **Project DECOR**  
- define branch‑level invariants  
- define branch‑level constraints  
- define branch‑level envelopes  
- define branch‑level structural expectations  
- define cross‑theme architectural rules  
- define cross‑tranche architectural rules within the branch  

The Architect MUST NOT:

- define theme‑specific detail  
- define tranche‑specific detail  
- define ticket‑level detail  
- define implementation detail  

Output MUST be written to:

```
/fugue_docs/branches/<branch-name>/branch-decor.md
```

---

# **7. Phase 3 — Branch Governance Envelope Establishment (Curator Persona)**

The Curator Persona MUST:

- define the **Branch Governance Envelope**  
- define governance posture  
- define approval hierarchy  
- define persona isolation rules  
- define governance invariants  
- define governance constraints  

The Curator MUST NOT:

- weaken governance posture  
- override project‑level invariants  

Output MUST be written to:

```
/fugue_docs/branches/<branch-name>/branch-governance.md
```

---

# **8. Phase 4 — Branch Naming Scheme Definition (Curator Persona)**

The Curator MUST:

- define the branch naming scheme  
- define naming invariants  
- define naming constraints  
- define naming propagation rules  

Branch naming MUST derive from:

- **Project Naming Scheme**  

Output MUST be written to:

```
/fugue_docs/branches/<branch-name>/naming-scheme.md
```

---

# **9. Phase 5 — Branch Namespace Scheme Definition (Curator Persona)**

The Curator MUST:

- define the branch namespace  
- define namespace invariants  
- define namespace constraints  
- define namespace propagation rules  

Branch namespaces MUST derive from:

- **Project Namespace Scheme**  

Output MUST be written to:

```
/fugue_docs/branches/<branch-name>/namespace-scheme.md
```

---

# **10. Phase 6 — Branch Identity Propagation Definition (Curator Persona)**

The Curator MUST:

- define identity propagation rules across Themes within the Branch  
- define identity propagation rules across Tranches within the Branch  
- define identity propagation rules across DECOR artefacts  
- define identity propagation rules across documentation  

Identity propagation MUST be:

- deterministic  
- traceable  
- reversible  
- auditable  

Output MUST be written to:

```
/fugue_docs/branches/<branch-name>/identity-propagation.md
```

---

# **11. Phase 7 — Branch Documentation Envelope Initialisation (Curator Persona)**

The Curator MUST:

- initialise the branch‑level documentation envelope  
- define documentation invariants  
- define documentation constraints  
- define documentation propagation rules  

Output MUST be written to:

```
/fugue_docs/branches/<branch-name>/documentation-envelope.md
```

---

# **12. Phase 8 — Branch Bootstrap Log Production (Curator Persona)**

The Curator MUST produce:

```
/fugue_docs/branches/<branch-name>/bootstrap-log.md
```

The log MUST include:

- summary of branch bootstrap  
- branch‑level invariants  
- branch‑level governance posture  
- naming + namespace rules  
- identity propagation rules  
- documentation envelope  
- recommended next steps (Theme creation)  

The log MUST be:

- factual  
- structured  
- deterministic  
- audit‑ready  

---

# **13. Phase 9 — Branch Approval (Curator Persona)**

The Curator MUST:

- approve the Branch Preamble  
- approve Branch DECOR  
- approve the Branch Governance Envelope  
- approve naming + namespace rules  
- approve identity propagation  
- approve the documentation envelope  
- approve the bootstrap log  

A Branch MUST NOT proceed to Theme creation without Curator approval.

---
