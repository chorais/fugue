# **branch-contract.md**  
**Fugue Branch Contract**  
Version: 2.4  
Status: Active  
Purpose: Define the governance‑level structure, invariants, envelopes, and lifecycle of a Fugue Branch.  
Methodology: Fugue Orchestration Method  
Implementation: Chorais  

---

# **1. Purpose**

The Branch Contract defines:

- the **parallel development stream** within a Fugue Project  
- the **governance and architectural boundaries** that apply across all Themes and Tranches within the Branch  
- the **branch‑level invariants, constraints, and envelopes**  
- the **branch‑level naming and namespace propagation rules**  
- the **branch‑level identity propagation rules**  
- the **branch‑level governance posture**  

A Branch is the **unit of parallelism** in Fugue.  
It enables multiple streams of work to proceed safely, deterministically, and independently.

---

# **2. Scope**

A Branch governs:

- all Themes within the Branch  
- all Tranches within those Themes  
- all DECOR artefacts produced under the Branch  
- all documentation under the Branch  
- all naming and namespace propagation under the Branch  
- all governance envelopes under the Branch  

A Branch MUST NOT:

- override Project‑level invariants  
- override Project‑level governance  
- override Project‑level naming or namespace roots  
- define ticket‑level detail  
- define tranche‑level detail  
- define implementation detail  

These are governed by lower‑level contracts.

---

# **3. Branch Structure**

A Branch MUST contain the following governed artefacts:

```
/fugue_docs/branches/<branch-name>/preamble.md
/fugue_docs/branches/<branch-name>/branch-governance.md
/fugue_docs/branches/<branch-name>/branch-decor.md
/fugue_docs/branches/<branch-name>/naming-scheme.md
/fugue_docs/branches/<branch-name>/namespace-scheme.md
/fugue_docs/branches/<branch-name>/identity-propagation.md
```

Each artefact MUST be:

- deterministic  
- complete  
- unambiguous  
- aligned with the Project Contract  
- aligned with the Documentation Envelope  

---

# **4. Branch Preamble**

The Branch Preamble defines:

- the branch mission  
- the branch boundaries  
- the branch scope  
- the branch risks  
- the branch constraints  
- the branch acceptance criteria  
- the branch success criteria  
- the branch dependencies  

The Branch Preamble MUST:

- be authored by the **Initiator persona**  
- be approved by the **Curator**  
- remain immutable except through governed updates  

---

# **5. Branch DECOR**

Branch DECOR defines:

- branch‑level invariants  
- branch‑level constraints  
- branch‑level envelopes  
- branch‑level structural expectations  
- cross‑theme architectural rules  
- cross‑tranche architectural rules within the branch  

Branch DECOR MUST:

- be authored by the **Architect persona**  
- follow the DECOR Specification  
- remain authoritative across all Themes and Tranches within the Branch  
- be updated only through governed DECOR Updates  

Branch DECOR MUST NOT:

- include theme‑specific detail  
- include tranche‑specific detail  
- include ticket‑level detail  
- include implementation detail  

---

# **6. Branch Governance Envelope**

The Branch Governance Envelope defines:

- the governance posture for the branch  
- the approval hierarchy  
- persona isolation rules  
- governance invariants  
- governance constraints  
- branch‑level drift boundaries  

The Governance Envelope MUST:

- be authored by the **Curator persona**  
- be enforced across all Themes and Tranches within the Branch  
- remain immutable except through governed updates  

---

# **7. Naming Scheme (Branch‑Level)**

The Branch Naming Scheme defines:

- naming conventions specific to the branch  
- naming invariants  
- naming constraints  
- naming propagation rules  

Branch naming MUST derive from the **Project Naming Scheme**.

---

# **8. Namespace Scheme (Branch‑Level)**

The Branch Namespace Scheme defines:

- the branch namespace  
- namespace propagation rules  
- namespace invariants  
- namespace constraints  

Branch namespaces MUST derive from the **Project Namespace Scheme**.

---

# **9. Identity Propagation**

Branch identity propagation defines:

- how identity flows across Themes within the Branch  
- how identity flows across Tranches within the Branch  
- how identity flows across DECOR artefacts  
- how identity flows across documentation  

Identity propagation MUST be:

- deterministic  
- traceable  
- reversible  
- auditable  

---

# **10. Themes**

A Branch MUST contain one or more Themes.

A Theme MUST:

- derive from the Branch Preamble  
- comply with Branch DECOR  
- comply with Branch Governance Envelope  
- comply with Project DECOR  
- comply with Project Governance Envelope  

Themes MUST NOT:

- override branch‑level invariants  
- override branch‑level governance  
- override project‑level invariants  

Themes MAY:

- diverge temporarily  
- merge through governed reconciliation  

---

# **11. Tranches**

A Branch MUST contain one or more Tranches (via Themes).

A Tranche MUST:

- derive from a Theme  
- comply with Branch DECOR  
- comply with Branch Governance Envelope  
- comply with Theme DECOR  
- comply with Project DECOR  
- comply with the Tranche Lifecycle Contract  

Tranches MUST NOT:

- override branch‑level invariants  
- override branch‑level governance  
- override project‑level invariants  

---

# **12. Branch Lifecycle**

A Branch proceeds through:

1. **Branch Bootstrap**  
2. **Theme Creation**  
3. **Tranche Execution**  
4. **Reconciliation**  
5. **Epilogue**  
6. **Branch Closure**  

The Branch Lifecycle MUST be:

- deterministic  
- persona‑isolated  
- governed  
- auditable  

---

# **13. Curator Authority**

The Curator MUST approve:

- the Branch Preamble  
- the Branch DECOR  
- the Branch Governance Envelope  
- the Branch Naming Scheme  
- the Branch Namespace Scheme  
- all Themes within the Branch  
- all Tranches within the Branch  
- all Reconciled DECOR  
- all closures  

The Curator is the **final governance authority**.

---

# **14. Documentation Requirements**

All branch‑level documentation MUST be stored under:

```
/fugue_docs/branches/<branch-name>/
```

Documentation MUST be:

- deterministic  
- complete  
- aligned with Branch DECOR  
- aligned with the Branch Governance Envelope  
- auditable  

---