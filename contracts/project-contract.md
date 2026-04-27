# **project-contract.md**  
**Fugue Project Contract**  
Version: 2.4  
Status: Active  
Purpose: Define the governance‑level structure, invariants, envelopes, and lifecycle of a Fugue Project.  
Methodology: Fugue Orchestration Method  
Implementation: Chorais  

---

# **1. Purpose**

The Fugue Project Contract defines:

- the **root governance object** of a Fugue system  
- the **structural and architectural boundaries** that apply across all Themes, Branches, and Tranches  
- the **identity, naming, and namespace roots**  
- the **project‑level invariants**  
- the **project‑level governance posture**  
- the **persona map** for the entire project  
- the **documentation envelope root**  
- the **project‑level DECOR**  

A Fugue Project is the **highest‑order governed artefact**.  
All Themes, Branches, and Tranches MUST comply with this contract.

---

# **2. Scope**

A Fugue Project governs:

- all Themes  
- all Branches  
- all Tranches  
- all DECOR artefacts  
- all documentation  
- all personas  
- all naming and namespace propagation  
- all governance envelopes  
- all lifecycle execution  

A Fugue Project MUST NOT:

- define ticket‑level detail  
- define tranche‑level detail  
- define implementation detail  
- define evaluator mechanics  
- define persona‑specific behaviour  

These are governed by lower‑level contracts.

---

# **3. Project Structure**

A Fugue Project MUST contain the following governed artefacts:

```
/fugue_docs/project/preamble.md
/fugue_docs/project/project-decor.md
/fugue_docs/project/governance-envelope.md
/fugue_docs/project/naming-scheme.md
/fugue_docs/project/namespace-scheme.md
/fugue_docs/project/persona-map.md
/fugue_docs/project/identity-propagation.md
```

Each artefact MUST be:

- deterministic  
- complete  
- unambiguous  
- aligned with this contract  
- aligned with the Documentation Envelope  

---

# **4. Project Preamble**

The Project Preamble defines:

- the long‑term mission  
- the architectural north star  
- the product or domain vision  
- the project boundaries  
- the project risks  
- the project constraints  
- the project acceptance criteria  
- the project success criteria  

The Project Preamble MUST:

- be authored by the **Initiator persona**  
- be approved by the **Curator**  
- remain immutable except through governed updates  

---

# **5. Project DECOR**

The Project DECOR defines:

- project‑level invariants  
- project‑level constraints  
- project‑level envelopes  
- project‑level structural expectations  
- cross‑theme architectural rules  
- cross‑branch architectural rules  
- cross‑tranche architectural rules  

The Project DECOR MUST:

- be authored by the **Architect persona**  
- follow the DECOR Specification  
- remain authoritative across all Themes, Branches, and Tranches  
- be updated only through governed DECOR Updates  

Project DECOR MUST NOT:

- include tranche‑specific detail  
- include ticket‑level detail  
- include implementation detail  

---

# **6. Governance Envelope**

The Project Governance Envelope defines:

- the governance posture  
- the approval hierarchy  
- the Curator’s authority  
- persona isolation rules  
- cross‑persona boundaries  
- governance invariants  
- governance constraints  

The Governance Envelope MUST:

- be authored by the **Curator persona**  
- be enforced across all Themes, Branches, and Tranches  
- remain immutable except through governed updates  

---

# **7. Naming Scheme Root**

The Project Naming Scheme defines:

- the root naming conventions  
- the naming invariants  
- the naming constraints  
- the naming propagation rules  

All Themes, Branches, and Tranches MUST derive naming from this root.

---

# **8. Namespace Scheme Root**

The Project Namespace Scheme defines:

- the root namespace  
- namespace propagation rules  
- namespace invariants  
- namespace constraints  

All Themes, Branches, and Tranches MUST derive namespaces from this root.

---

# **9. Persona Map**

The Project Persona Map defines:

- which personas are active in the project  
- how personas interact  
- persona isolation rules  
- persona sequencing rules  
- persona governance boundaries  

The Persona Map MUST include:

- Curator  
- Initiator  
- Architect  
- Conductor  
- Implementer  
- Auditor  
- Verifier (optional)  
- Methodologist (optional)  

---

# **10. Identity Propagation**

The Project Identity Propagation Contract defines:

- how identity flows across Themes  
- how identity flows across Branches  
- how identity flows across Tranches  
- how identity flows across DECOR artefacts  
- how identity flows across documentation  

Identity propagation MUST be:

- deterministic  
- traceable  
- reversible  
- auditable  

---

# **11. Themes**

A Fugue Project MAY contain one or more Themes.

A Theme MUST:

- derive from the Project Preamble  
- comply with Project DECOR  
- comply with the Governance Envelope  
- comply with naming and namespace roots  

Themes MUST NOT:

- override project‑level invariants  
- override project‑level governance  
- override project‑level naming or namespace roots  

---

# **12. Branches**

A Fugue Project MAY contain one or more Branches.

A Branch MUST:

- derive from a Theme  
- comply with Project DECOR  
- comply with Theme DECOR (if present)  
- comply with the Governance Envelope  

Branches MUST NOT:

- override project‑level invariants  
- override theme‑level invariants  
- override governance posture  

Branches MAY:

- diverge temporarily  
- merge through governed reconciliation  

---

# **13. Tranches**

A Fugue Project MUST contain one or more Tranches.

A Tranche MUST:

- derive from a Branch  
- comply with Project DECOR  
- comply with Theme DECOR  
- comply with Branch governance  
- comply with the Tranche Lifecycle Contract  

Tranches MUST NOT:

- override project‑level invariants  
- override theme‑level invariants  
- override branch‑level invariants  

---

# **14. Project Lifecycle**

A Fugue Project proceeds through:

1. **Project Bootstrap**  
2. **Theme Creation**  
3. **Branch Creation**  
4. **Tranche Execution**  
5. **Reconciliation**  
6. **Epilogue**  
7. **Closure**  
8. **Continuation or Termination**  

The Project Lifecycle MUST be:

- deterministic  
- persona‑isolated  
- governed  
- auditable  

---

# **15. Curator Authority**

The Curator MUST approve:

- the Project Preamble  
- the Project DECOR  
- the Governance Envelope  
- the Naming Scheme  
- the Namespace Scheme  
- the Persona Map  
- all Themes  
- all Branches  
- all Tranches  
- all Reconciled DECOR  
- all closures  

The Curator is the **final governance authority**.

---

# **16. Documentation Requirements**

All project‑level documentation MUST be stored under:

```
/fugue_docs/project/
```

Documentation MUST be:

- deterministic  
- complete  
- aligned with Project DECOR  
- aligned with the Governance Envelope  
- auditable  