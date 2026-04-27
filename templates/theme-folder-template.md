
# **theme-folder-template.md — Theme Folder Template (v2.4)**  
Version: 1.0  
Status: Active  
Methodology: Fugue Orchestration Method  
Scope: Theme‑Level Folder Structure  
Personas:  
- **Initiator** (preamble author)  
- **Architect** (theme DECOR)  
- **Curator** (governance, naming, namespace, identity, documentation)  
- **Tranche creators** (downstream consumers)  

---

# **1. Purpose**

This template defines the **canonical directory structure** for a Fugue Theme.

A Theme is the **coherent, multi‑tranche initiative** in the hierarchy:

> **Project → Branch → Theme → Tranche → Ticket**

This folder structure MUST be created during **Theme Bootstrap** and MUST remain stable for the entire lifecycle of the theme.

All Tranches derive from this structure.

---

# **2. Canonical Theme Directory Structure**

```
/fugue_docs/
└── themes/
    └── <theme-name>/
        ├── preamble.md
        ├── theme-decor.md
        ├── governance.md
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

- theme mission  
- theme vision  
- scope (in‑scope / out‑of‑scope)  
- boundaries  
- strategic objectives  
- constraints  
- risks  
- dependencies  
- success criteria  

This is the **root intent artefact** for the theme.

---

## **3.2 theme-decor.md**
Authored by: **Architect**  
Approved by: **Curator**

Contains:

- theme‑level invariants  
- theme‑level constraints  
- theme‑level envelopes  
- cross‑tranche architectural rules  
- structural expectations  

This is the **theme‑level architectural contract**.

Theme DECOR is optional but recommended.

---

## **3.3 governance.md**
Authored by: **Curator**

Contains:

- governance posture  
- approval hierarchy  
- persona isolation rules  
- governance invariants  
- governance constraints  

This is the **theme‑level governance contract**.

---

## **3.4 naming-scheme.md**
Authored by: **Curator**

Contains:

- naming conventions specific to the theme  
- naming invariants  
- naming constraints  
- naming propagation rules  

Theme naming MUST derive from:

- **Project Naming Scheme**  
- **Branch Naming Scheme**  

---

## **3.5 namespace-scheme.md**
Authored by: **Curator**

Contains:

- theme namespace  
- namespace invariants  
- namespace constraints  
- namespace propagation rules  

Theme namespaces MUST derive from:

- **Project Namespace Scheme**  
- **Branch Namespace Scheme**  

---

## **3.6 identity-propagation.md**
Authored by: **Curator**

Contains:

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

This is the **theme‑level documentation contract**.

---

## **3.8 bootstrap-log.md**
Authored by: **Curator**

Contains:

- summary of Theme Bootstrap  
- theme‑level invariants  
- governance posture  
- naming + namespace rules  
- identity propagation rules  
- documentation envelope  
- next steps (Tranche creation)  

This is the **audit log** for Theme Bootstrap.

---

## **3.9 README.md**
Authored by: **Curator or Methodologist**

Contains:

- overview of the theme  
- explanation of theme‑level artefacts  
- instructions for Tranche creators  

This is the **human‑readable entrypoint** for the theme.

---

# **4. Directory Invariants**

The following MUST always hold:

- No files may be added to `/fugue_docs/themes/<theme-name>/` except through governed updates.  
- No files may be removed except through governed archival.  
- No files may be renamed except through governed migration.  
- No persona may write outside their authorised artefacts.  
- All Tranches MUST derive from these theme‑level contracts.  

---