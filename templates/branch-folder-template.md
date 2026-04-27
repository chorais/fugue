# **branch-folder-template.md — Branch Folder Template (v2.4)**  
Version: 1.0  
Status: Active  
Methodology: Fugue Orchestration Method  
Scope: Branch‑Level Folder Structure  
Personas:  
- **Initiator** (preamble author)  
- **Architect** (branch DECOR)  
- **Curator** (governance, naming, namespace, identity, documentation)  
- **Theme creators** (downstream consumers)  

---

# **1. Purpose**

This template defines the **canonical directory structure** for a Fugue Branch.

A Branch is the **parallel development stream** in the hierarchy:

> **Project → Branch → Theme → Tranche → Ticket**

This folder structure MUST be created during **Branch Bootstrap** and MUST remain stable for the entire lifecycle of the branch.

All Themes and Tranches derive from this structure.

---

# **2. Canonical Branch Directory Structure**

```
/fugue_docs/
└── branches/
    └── <branch-name>/
        ├── preamble.md
        ├── branch-decor.md
        ├── branch-governance.md
        ├── naming-scheme.md
        ├── namespace-scheme.md
        ├── identity-propagation.md
        ├── documentation-envelope.md
        ├── bootstrap-log.md
        └── README.md
```

Each file is described below.

---

# **3. File Specifications**

## **3.1 preamble.md**
Authored by: **Initiator**  
Approved by: **Curator**

Contains:

- branch mission  
- branch vision  
- scope (in‑scope / out‑of‑scope)  
- boundaries  
- strategic objectives  
- constraints  
- risks  
- dependencies  
- success criteria  

This is the **root intent artefact** for the branch.

---

## **3.2 branch-decor.md**
Authored by: **Architect**  
Approved by: **Curator**

Contains:

- branch‑level invariants  
- branch‑level constraints  
- branch‑level envelopes  
- cross‑theme architectural rules  
- cross‑tranche architectural rules  
- structural expectations  

This is the **branch‑level architectural contract**.

---

## **3.3 branch-governance.md**
Authored by: **Curator**

Contains:

- governance posture  
- approval hierarchy  
- persona isolation rules  
- governance invariants  
- governance constraints  

This is the **branch‑level governance contract**.

---

## **3.4 naming-scheme.md**
Authored by: **Curator**

Contains:

- naming conventions specific to the branch  
- naming invariants  
- naming constraints  
- naming propagation rules  

Branch naming MUST derive from the **Project Naming Scheme**.

---

## **3.5 namespace-scheme.md**
Authored by: **Curator**

Contains:

- branch namespace  
- namespace invariants  
- namespace constraints  
- namespace propagation rules  

Branch namespaces MUST derive from the **Project Namespace Scheme**.

---

## **3.6 identity-propagation.md**
Authored by: **Curator**

Contains:

- identity propagation rules across Themes  
- identity propagation rules across Tranches  
- identity propagation rules across DECOR artefacts  
- identity propagation rules across documentation  

Identity propagation MUST be deterministic, traceable, reversible, and auditable.

---

## **3.7 documentation-envelope.md**
Authored by: **Curator**

Contains:

- documentation invariants  
- documentation constraints  
- documentation propagation rules  
- documentation namespace structure  

This is the **branch‑level documentation contract**.

---

## **3.8 bootstrap-log.md**
Authored by: **Curator**

Contains:

- summary of Branch Bootstrap  
- branch‑level invariants  
- governance posture  
- naming + namespace rules  
- identity propagation rules  
- documentation envelope  
- next steps (Theme creation)  

This is the **audit log** for Branch Bootstrap.

---

## **3.9 README.md**
Authored by: **Curator or Methodologist**

Contains:

- overview of the branch  
- explanation of branch‑level artefacts  
- instructions for Theme creators  
- instructions for Tranche creators  

This is the **human‑readable entrypoint** for the branch.

---

# **4. Directory Invariants**

The following MUST always hold:

- No files may be added to `/fugue_docs/branches/<branch-name>/` except through governed updates.  
- No files may be removed except through governed archival.  
- No files may be renamed except through governed migration.  
- No persona may write outside their authorised artefacts.  
- All Themes and Tranches MUST derive from these branch‑level contracts.  

---
