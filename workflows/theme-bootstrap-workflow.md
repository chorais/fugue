# **theme-bootstrap-workflow.md**  
**Theme Bootstrap Workflow**  
Version: 2.4  
Status: Active  
Purpose: Define the deterministic, persona‑isolated process for creating and initialising a Fugue Theme.  
Methodology: Fugue Orchestration Method  
Implementation: Chorais  

---

# **1. Purpose**

Theme Bootstrap establishes:

- the **Theme Preamble**  
- the **Theme DECOR** (optional but recommended)  
- the **Theme Governance Envelope**  
- the **Theme Naming Scheme**  
- the **Theme Namespace Scheme**  
- the **Theme Identity Propagation Rules**  
- the **Theme Documentation Envelope**  

A Theme is a **multi‑tranche initiative** within a Branch.  
Theme Bootstrap MUST be completed before any Tranche can begin.

---

# **2. Preconditions**

Theme Bootstrap may begin only when:

- a **Branch** already exists  
- the **Project Bootstrap Workflow** is complete  
- the **Branch Bootstrap Workflow** is complete  
- the operator has attached the required contracts  
- no Theme artefacts exist for the given theme name  

Theme Bootstrap MUST NOT begin mid‑theme.

---

# **3. Required Inputs**

The operator MUST attach:

```
/contracts/theme-contract.md
/contracts/persona-boundaries.md
/contracts/methodology-overview.md
/contracts/naming-scheme-contract.md
/contracts/namespace-scheme-contract.md
/contracts/governance-envelope-contract.md
/contracts/identity-propagation-contract.md
/contracts/documentation-envelope.md
/fugue_docs/branches/<branch-name>/branch-decor.md
/fugue_docs/branches/<branch-name>/branch-governance.md
```

These files form the **theme bootstrap substrate**.

---

# **4. Theme Bootstrap Overview**

Theme Bootstrap proceeds through the following deterministic phases:

1. **Theme Initiation (Initiator)**  
2. **Theme DECOR Derivation (Architect)**  
3. **Theme Governance Envelope Establishment (Curator)**  
4. **Theme Naming Scheme Definition (Curator)**  
5. **Theme Namespace Scheme Definition (Curator)**  
6. **Theme Identity Propagation Definition (Curator)**  
7. **Theme Documentation Envelope Initialisation (Curator)**  
8. **Theme Bootstrap Log Production (Curator)**  
9. **Theme Approval (Curator)**  

Each phase MUST be completed in order.

---

# **5. Phase 1 — Theme Initiation (Initiator Persona)**

The Initiator Persona MUST:

- produce the **Theme Preamble**  
- define the theme mission  
- define theme boundaries  
- define theme scope  
- define theme risks  
- define theme constraints  
- define theme acceptance criteria  
- define theme success criteria  
- define theme dependencies  

The Initiator MUST NOT:

- define architecture  
- define governance  
- define naming or namespace rules  
- define persona behaviour  
- define DECOR  

Output MUST be written to:

```
/fugue_docs/themes/<theme-name>/preamble.md
```

---

# **6. Phase 2 — Theme DECOR Derivation (Architect Persona)**

Theme DECOR is optional but recommended.

The Architect Persona MUST:

- derive **Theme DECOR** from the Theme Preamble  
- incorporate constraints from **Branch DECOR**  
- define theme‑level invariants  
- define theme‑level constraints  
- define theme‑level envelopes  
- define theme‑level structural expectations  
- define cross‑tranche architectural rules  

The Architect MUST NOT:

- define tranche‑specific detail  
- define ticket‑level detail  
- define implementation detail  

Output MUST be written to:

```
/fugue_docs/themes/<theme-name>/theme-decor.md
```

---

# **7. Phase 3 — Theme Governance Envelope Establishment (Curator Persona)**

The Curator Persona MUST:

- define the **Theme Governance Envelope**  
- define governance posture  
- define approval hierarchy  
- define persona isolation rules  
- define governance invariants  
- define governance constraints  

The Curator MUST NOT:

- weaken governance posture  
- override branch‑level invariants  
- override project‑level invariants  

Output MUST be written to:

```
/fugue_docs/themes/<theme-name>/governance.md
```

---

# **8. Phase 4 — Theme Naming Scheme Definition (Curator Persona)**

The Curator MUST:

- define the theme naming scheme  
- define naming invariants  
- define naming constraints  
- define naming propagation rules  

Theme naming MUST derive from:

- **Project Naming Scheme**  
- **Branch Naming Scheme**  

Output MUST be written to:

```
/fugue_docs/themes/<theme-name>/naming-scheme.md
```

---

# **9. Phase 5 — Theme Namespace Scheme Definition (Curator Persona)**

The Curator MUST:

- define the theme namespace  
- define namespace invariants  
- define namespace constraints  
- define namespace propagation rules  

Theme namespaces MUST derive from:

- **Project Namespace Scheme**  
- **Branch Namespace Scheme**  

Output MUST be written to:

```
/fugue_docs/themes/<theme-name>/namespace-scheme.md
```

---

# **10. Phase 6 — Theme Identity Propagation Definition (Curator Persona)**

The Curator MUST:

- define identity propagation rules across Tranches within the Theme  
- define identity propagation rules across DECOR artefacts  
- define identity propagation rules across documentation  

Identity propagation MUST be:

- deterministic  
- traceable  
- reversible  
- auditable  

Output MUST be written to:

```
/fugue_docs/themes/<theme-name>/identity-propagation.md
```

---

# **11. Phase 7 — Theme Documentation Envelope Initialisation (Curator Persona)**

The Curator MUST:

- initialise the theme‑level documentation envelope  
- define documentation invariants  
- define documentation constraints  
- define documentation propagation rules  

Output MUST be written to:

```
/fugue_docs/themes/<theme-name>/documentation-envelope.md
```

---

# **12. Phase 8 — Theme Bootstrap Log Production (Curator Persona)**

The Curator MUST produce:

```
/fugue_docs/themes/<theme-name>/bootstrap-log.md
```

The log MUST include:

- summary of theme bootstrap  
- theme‑level invariants  
- theme‑level governance posture  
- naming + namespace rules  
- identity propagation rules  
- documentation envelope  
- recommended next steps (Branch or Tranche creation)  

The log MUST be:

- factual  
- structured  
- deterministic  
- audit‑ready  

---

# **13. Phase 9 — Theme Approval (Curator Persona)**

The Curator MUST:

- approve the Theme Preamble  
- approve Theme DECOR (if present)  
- approve the Theme Governance Envelope  
- approve naming + namespace rules  
- approve identity propagation  
- approve the documentation envelope  
- approve the bootstrap log  

A Theme MUST NOT proceed to Tranche creation without Curator approval.
