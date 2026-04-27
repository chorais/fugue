# **project-bootstrap-workflow.md**  
**Project Bootstrap Workflow**  
Version: 2.4  
Status: Active  
Purpose: Define the deterministic, persona‑isolated process for creating and initialising a Fugue Project.  
Methodology: Fugue Orchestration Method  
Implementation: Chorais  

---

# **1. Purpose**

Project Bootstrap is the **root lifecycle phase** of the Fugue Method.

It establishes:

- the **Project Preamble**  
- the **Project DECOR**  
- the **Project Governance Envelope**  
- the **Naming Scheme Root**  
- the **Namespace Scheme Root**  
- the **Project Persona Map**  
- the **Identity Propagation Rules**  
- the **Project Documentation Envelope**  

Project Bootstrap MUST be completed **before** any Branch, Theme, or Tranche can be created.

---

# **2. Preconditions**

Project Bootstrap may begin only when:

- the human operator has defined the project name  
- no project‑level artefacts exist  
- no Themes, Branches, or Tranches exist  
- the operator has attached the required contracts  

Project Bootstrap MUST NOT begin mid‑project.

---

# **3. Required Inputs**

The operator MUST attach:

```
/contracts/project-contract.md
/contracts/persona-boundaries.md
/contracts/methodology-overview.md
/contracts/naming-scheme-contract.md
/contracts/namespace-scheme-contract.md
/contracts/governance-envelope-contract.md
/contracts/identity-propagation-contract.md
/contracts/documentation-envelope.md
```

These files form the **project bootstrap substrate**.

---

# **4. Project Bootstrap Overview**

Project Bootstrap proceeds through the following deterministic phases:

1. **Project Initiation (Initiator)**  
2. **Project DECOR Derivation (Architect)**  
3. **Governance Envelope Establishment (Curator)**  
4. **Naming + Namespace Root Definition (Curator)**  
5. **Persona Map Definition (Curator)**  
6. **Identity Propagation Definition (Curator)**  
7. **Project Documentation Envelope Initialisation (Curator)**  
8. **Project Bootstrap Log Production (Curator)**  
9. **Project Approval (Curator)**  

Each phase MUST be completed in order.

---

# **5. Phase 1 — Project Initiation (Initiator Persona)**

The Initiator Persona MUST:

- produce the **Project Preamble**  
- define the long‑term mission  
- define project boundaries  
- define project risks  
- define project acceptance criteria  
- define project success criteria  
- define project dependencies  

The Initiator MUST NOT:

- define architecture  
- define governance  
- define naming or namespace rules  
- define persona behaviour  
- define DECOR  

Output MUST be written to:

```
/fugue_docs/project/preamble.md
```

---

# **6. Phase 2 — Project DECOR Derivation (Architect Persona)**

The Architect Persona MUST:

- derive **Project DECOR** from the Project Preamble  
- define project‑level invariants  
- define project‑level constraints  
- define project‑level envelopes  
- define project‑level structural expectations  
- define cross‑theme and cross‑branch architectural rules  

The Architect MUST NOT:

- define tranche‑level detail  
- define ticket‑level detail  
- define implementation detail  

Output MUST be written to:

```
/fugue_docs/project/project-decor.md
```

---

# **7. Phase 3 — Governance Envelope Establishment (Curator Persona)**

The Curator Persona MUST:

- define the **Project Governance Envelope**  
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
/fugue_docs/project/governance-envelope.md
```

---

# **8. Phase 4 — Naming Scheme Root Definition (Curator Persona)**

The Curator MUST:

- define the root naming scheme  
- define naming invariants  
- define naming constraints  
- define naming propagation rules  

Output MUST be written to:

```
/fugue_docs/project/naming-scheme.md
```

---

# **9. Phase 5 — Namespace Scheme Root Definition (Curator Persona)**

The Curator MUST:

- define the root namespace  
- define namespace invariants  
- define namespace constraints  
- define namespace propagation rules  

Output MUST be written to:

```
/fugue_docs/project/namespace-scheme.md
```

---

# **10. Phase 6 — Persona Map Definition (Curator Persona)**

The Curator MUST:

- define the project‑level persona map  
- define persona isolation rules  
- define persona sequencing rules  
- define persona governance boundaries  

Output MUST be written to:

```
/fugue_docs/project/persona-map.md
```

---

# **11. Phase 7 — Identity Propagation Definition (Curator Persona)**

The Curator MUST:

- define identity propagation rules across Themes  
- define identity propagation rules across Branches  
- define identity propagation rules across Tranches  
- define identity propagation rules across DECOR artefacts  
- define identity propagation rules across documentation  

Output MUST be written to:

```
/fugue_docs/project/identity-propagation.md
```

---

# **12. Phase 8 — Documentation Envelope Initialisation (Curator Persona)**

The Curator MUST:

- initialise the project‑level documentation envelope  
- define documentation invariants  
- define documentation constraints  
- define documentation propagation rules  

Output MUST be written to:

```
/fugue_docs/project/documentation-envelope.md
```

---

# **13. Phase 9 — Project Bootstrap Log Production (Curator Persona)**

The Curator MUST produce:

```
/fugue_docs/project/bootstrap-log.md
```

The log MUST include:

- summary of project bootstrap  
- project‑level invariants  
- project‑level governance posture  
- naming + namespace roots  
- persona map  
- identity propagation rules  
- documentation envelope  
- recommended next steps (Theme or Branch creation)  

The log MUST be:

- factual  
- structured  
- deterministic  
- audit‑ready  

---

# **14. Phase 10 — Project Approval (Curator Persona)**

The Curator MUST:

- approve the Project Preamble  
- approve Project DECOR  
- approve the Governance Envelope  
- approve naming + namespace roots  
- approve the persona map  
- approve identity propagation  
- approve the documentation envelope  
- approve the bootstrap log  

A Project MUST NOT proceed to Theme or Branch creation without Curator approval.

---
