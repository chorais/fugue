# **theme-contract.md**  
**Fugue Theme Contract**  
Version: 2.4  
Status: Active  
Purpose: Define the governance‑level structure, invariants, envelopes, and lifecycle of a Fugue Theme.  
Methodology: Fugue Orchestration Method  
Implementation: Chorais  

---

# **1. Purpose**

The Theme Contract defines:

- the **mid‑level governance object** of a Fugue Project  
- the **architectural and product direction** that spans multiple tranches  
- the **scope, boundaries, risks, and constraints** of a long‑running initiative  
- the **theme‑level invariants and envelopes**  
- the **theme‑level DECOR** (optional but recommended)  
- the **identity, naming, and namespace propagation rules** for all tranches within the theme  

A Theme is the **narrative arc** of a Fugue Project.  
It provides continuity across tranches and ensures architectural coherence.

---

# **2. Scope**

A Theme governs:

- all Branches within the Theme  
- all Tranches within those Branches  
- all DECOR artefacts produced under the Theme  
- all documentation under the Theme  
- all naming and namespace propagation under the Theme  
- all governance envelopes under the Theme  

A Theme MUST NOT:

- override Project‑level invariants  
- override Project‑level governance  
- override Project‑level naming or namespace roots  
- define ticket‑level detail  
- define tranche‑level detail  
- define implementation detail  

These are governed by lower‑level contracts.

---

# **3. Theme Structure**

A Theme MUST contain the following governed artefacts:

```
/fugue_docs/themes/<theme-name>/preamble.md
/fugue_docs/themes/<theme-name>/theme-decor.md
/fugue_docs/themes/<theme-name>/governance.md
/fugue_docs/themes/<theme-name>/naming-scheme.md
/fugue_docs/themes/<theme-name>/namespace-scheme.md
/fugue_docs/themes/<theme-name>/identity-propagation.md
```

Each artefact MUST be:

- deterministic  
- complete  
- unambiguous  
- aligned with the Project Contract  
- aligned with the Documentation Envelope  

---

# **4. Theme Preamble**

The Theme Preamble defines:

- the theme mission  
- the theme boundaries  
- the theme scope  
- the theme risks  
- the theme constraints  
- the theme acceptance criteria  
- the theme success criteria  
- the theme dependencies  

The Theme Preamble MUST:

- be authored by the **Initiator persona**  
- be approved by the **Curator**  
- remain immutable except through governed updates  

---

# **5. Theme DECOR**

Theme DECOR is optional but recommended.

Theme DECOR defines:

- theme‑level invariants  
- theme‑level constraints  
- theme‑level envelopes  
- theme‑level structural expectations  
- cross‑tranche architectural rules  
- cross‑branch architectural rules within the theme  

Theme DECOR MUST:

- be authored by the **Architect persona**  
- follow the DECOR Specification  
- remain authoritative across all Branches and Tranches within the Theme  
- be updated only through governed DECOR Updates  

Theme DECOR MUST NOT:

- include tranche‑specific detail  
- include ticket‑level detail  
- include implementation detail  

---

# **6. Theme Governance Envelope**

The Theme Governance Envelope defines:

- the governance posture for the theme  
- the approval hierarchy  
- persona isolation rules  
- governance invariants  
- governance constraints  
- theme‑level drift boundaries  

The Governance Envelope MUST:

- be authored by the **Curator persona**  
- be enforced across all Branches and Tranches within the Theme  
- remain immutable except through governed updates  

---

# **7. Naming Scheme (Theme‑Level)**

The Theme Naming Scheme defines:

- naming conventions specific to the theme  
- naming invariants  
- naming constraints  
- naming propagation rules  

Theme naming MUST derive from the **Project Naming Scheme**.

---

# **8. Namespace Scheme (Theme‑Level)**

The Theme Namespace Scheme defines:

- the theme namespace  
- namespace propagation rules  
- namespace invariants  
- namespace constraints  

Theme namespaces MUST derive from the **Project Namespace Scheme**.

---

# **9. Identity Propagation**

Theme identity propagation defines:

- how identity flows across Branches within the Theme  
- how identity flows across Tranches within the Theme  
- how identity flows across DECOR artefacts  
- how identity flows across documentation  

Identity propagation MUST be:

- deterministic  
- traceable  
- reversible  
- auditable  

---

# **10. Branches**

A Theme MAY contain one or more Branches.

A Branch MUST:

- derive from the Theme Preamble  
- comply with Theme DECOR  
- comply with Theme Governance Envelope  
- comply with Project DECOR  
- comply with Project Governance Envelope  

Branches MUST NOT:

- override theme‑level invariants  
- override theme‑level governance  
- override project‑level invariants  

Branches MAY:

- diverge temporarily  
- merge through governed reconciliation  

---

# **11. Tranches**

A Theme MUST contain one or more Tranches.

A Tranche MUST:

- derive from a Branch  
- comply with Theme DECOR  
- comply with Theme Governance Envelope  
- comply with Project DECOR  
- comply with Project Governance Envelope  
- comply with the Tranche Lifecycle Contract  

Tranches MUST NOT:

- override theme‑level invariants  
- override theme‑level governance  
- override project‑level invariants  

---

# **12. Theme Lifecycle**

A Theme proceeds through:

1. **Theme Bootstrap**  
2. **Branch Creation**  
3. **Tranche Execution**  
4. **Reconciliation**  
5. **Epilogue**  
6. **Theme Closure**  

The Theme Lifecycle MUST be:

- deterministic  
- persona‑isolated  
- governed  
- auditable  

---

# **13. Curator Authority**

The Curator MUST approve:

- the Theme Preamble  
- the Theme DECOR  
- the Theme Governance Envelope  
- the Theme Naming Scheme  
- the Theme Namespace Scheme  
- all Branches within the Theme  
- all Tranches within the Theme  
- all Reconciled DECOR  
- all closures  

The Curator is the **final governance authority**.

---

# **14. Documentation Requirements**

All theme‑level documentation MUST be stored under:

```
/fugue_docs/themes/<theme-name>/
```

Documentation MUST be:

- deterministic  
- complete  
- aligned with Theme DECOR  
- aligned with the Theme Governance Envelope  
- auditable  
