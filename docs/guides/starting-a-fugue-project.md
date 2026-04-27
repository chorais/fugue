# **Starting a Fugue Project, Branch, and Theme (v2.4)**  
**A Unified Operator Guide**  
Version: 2.4  
Status: Active  
Methodology: Fugue Orchestration Method  
Implementation: Chorais  

---

# **1. Purpose of This Guide**

This guide explains **how to start work in Fugue v2.4**, from the very top of the hierarchy:

> **Project → Branch → Theme → Tranche → Ticket**

It provides a **single, deterministic sequence** for:

- creating a **Fugue Project**  
- creating a **Branch** within that project  
- creating a **Theme** within that branch  

This guide is for human operators and the Initiator, Curator, and Architect personas.

---

# **2. Overview of the Hierarchy**

Fugue v2.4 introduces a strict, governance‑aligned hierarchy:

```
Project
└── Branch
    └── Theme
        └── Tranche
            └── Ticket
```

Each layer has its own:

- bootstrap workflow  
- preamble  
- DECOR  
- governance envelope  
- naming + namespace scheme  
- identity propagation rules  
- documentation envelope  

This guide covers the **top three layers**.

---

# **3. Starting a Fugue Project**

A **Project** is the root governance object.  
It defines the long‑term mission, architecture, governance posture, naming roots, and persona map.

### **3.1 Preconditions**
You may start a project when:

- no project exists  
- you have a project name  
- you have the project‑level contracts available  

### **3.2 Steps**

#### **Step 1 — Initiator creates the Project Preamble**
Defines:

- mission  
- vision  
- scope  
- boundaries  
- strategic objectives  
- constraints  
- risks  
- dependencies  
- success criteria  

Saved to:

```
/fugue_docs/project/preamble.md
```

---

#### **Step 2 — Architect derives Project DECOR**
Defines:

- project‑level invariants  
- project‑level constraints  
- project‑level envelopes  
- cross‑branch and cross‑theme architectural rules  

Saved to:

```
/fugue_docs/project/project-decor.md
```

---

#### **Step 3 — Curator establishes the Governance Envelope**
Defines:

- governance posture  
- persona isolation rules  
- approval hierarchy  
- governance constraints  

Saved to:

```
/fugue_docs/project/governance-envelope.md
```

---

#### **Step 4 — Curator defines Naming + Namespace roots**
Saved to:

```
/fugue_docs/project/naming-scheme.md
/fugue_docs/project/namespace-scheme.md
```

---

#### **Step 5 — Curator defines Persona Map + Identity Propagation**
Saved to:

```
/fugue_docs/project/persona-map.md
/fugue_docs/project/identity-propagation.md
```

---

#### **Step 6 — Curator defines Documentation Envelope**
Saved to:

```
/fugue_docs/project/documentation-envelope.md
```

---

#### **Step 7 — Curator produces the Project Bootstrap Log**
Saved to:

```
/fugue_docs/project/bootstrap-log.md
```

---

#### **Step 8 — Curator approves the Project**
Only after approval may Branch creation begin.

---

# **4. Starting a Fugue Branch**

A **Branch** is a parallel development stream within a project.  
It allows multiple teams or initiatives to run concurrently.

### **4.1 Preconditions**
You may start a branch when:

- the Project Bootstrap Workflow is complete  
- the Curator has approved the project  
- no branch with this name exists  

### **4.2 Steps**

#### **Step 1 — Initiator creates the Branch Preamble**
Defines:

- branch mission  
- branch vision  
- scope  
- boundaries  
- strategic objectives  
- constraints  
- risks  
- dependencies  
- success criteria  

Saved to:

```
/fugue_docs/branches/<branch-name>/preamble.md
```

---

#### **Step 2 — Architect derives Branch DECOR**
Defines:

- branch‑level invariants  
- branch‑level constraints  
- branch‑level envelopes  
- cross‑theme and cross‑tranche architectural rules  

Saved to:

```
/fugue_docs/branches/<branch-name>/branch-decor.md
```

---

#### **Step 3 — Curator establishes Branch Governance Envelope**
Saved to:

```
/fugue_docs/branches/<branch-name>/branch-governance.md
```

---

#### **Step 4 — Curator defines Branch Naming + Namespace**
Saved to:

```
/fugue_docs/branches/<branch-name>/naming-scheme.md
/fugue_docs/branches/<branch-name>/namespace-scheme.md
```

---

#### **Step 5 — Curator defines Branch Identity Propagation**
Saved to:

```
/fugue_docs/branches/<branch-name>/identity-propagation.md
```

---

#### **Step 6 — Curator defines Branch Documentation Envelope**
Saved to:

```
/fugue_docs/branches/<branch-name>/documentation-envelope.md
```

---

#### **Step 7 — Curator produces the Branch Bootstrap Log**
Saved to:

```
/fugue_docs/branches/<branch-name>/bootstrap-log.md
```

---

#### **Step 8 — Curator approves the Branch**
Only after approval may Theme creation begin.

---

# **5. Starting a Fugue Theme**

A **Theme** is a coherent, multi‑tranche initiative within a branch.  
It provides narrative and architectural continuity.

### **5.1 Preconditions**
You may start a theme when:

- the Branch Bootstrap Workflow is complete  
- the Curator has approved the branch  
- no theme with this name exists  

### **5.2 Steps**

#### **Step 1 — Initiator creates the Theme Preamble**
Defines:

- theme mission  
- theme vision  
- scope  
- boundaries  
- strategic objectives  
- constraints  
- risks  
- dependencies  
- success criteria  

Saved to:

```
/fugue_docs/themes/<theme-name>/preamble.md
```

---

#### **Step 2 — Architect derives Theme DECOR**
Defines:

- theme‑level invariants  
- theme‑level constraints  
- theme‑level envelopes  
- cross‑tranche architectural rules  

Saved to:

```
/fugue_docs/themes/<theme-name>/theme-decor.md
```

---

#### **Step 3 — Curator establishes Theme Governance Envelope**
Saved to:

```
/fugue_docs/themes/<theme-name>/governance.md
```

---

#### **Step 4 — Curator defines Theme Naming + Namespace**
Saved to:

```
/fugue_docs/themes/<theme-name>/naming-scheme.md
/fugue_docs/themes/<theme-name>/namespace-scheme.md
```

---

#### **Step 5 — Curator defines Theme Identity Propagation**
Saved to:

```
/fugue_docs/themes/<theme-name>/identity-propagation.md
```

---

#### **Step 6 — Curator defines Theme Documentation Envelope**
Saved to:

```
/fugue_docs/themes/<theme-name>/documentation-envelope.md
```

---

#### **Step 7 — Curator produces the Theme Bootstrap Log**
Saved to:

```
/fugue_docs/themes/<theme-name>/bootstrap-log.md
```

---

#### **Step 8 — Curator approves the Theme**
Only after approval may Tranche creation begin.

---

# **6. Summary of the Full Bootstrap Path**

```
Start Project
    ↓
Create Branch
    ↓
Create Theme
    ↓
Start Tranche
    ↓
Execute Tickets
```

Each layer:

- has its own Preamble  
- has its own DECOR  
- has its own Governance Envelope  
- has its own Naming + Namespace rules  
- has its own Identity Propagation  
- has its own Documentation Envelope  
- must be approved by the Curator  

This ensures:

- determinism  
- persona isolation  
- governance safety  
- architectural continuity  
- auditability  
- multi‑team scalability  
