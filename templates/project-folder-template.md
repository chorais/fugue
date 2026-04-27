# **project-folder-template.md — Project Folder Template (v2.4)**  
Version: 1.0  
Status: Active  
Methodology: Fugue Orchestration Method  
Scope: Project‑Level Folder Structure  
Persona: Curator (approver), Initiator (author of preamble), Architect (DECOR), Methodologist (optional)  

---

# **1. Purpose**

This template defines the **canonical directory structure** for a Fugue Project.

A Fugue Project is the **root governance object** in the hierarchy:

> **Project → Branch → Theme → Tranche → Ticket**

This folder structure MUST be created during **Project Bootstrap** and MUST remain stable for the entire lifecycle of the project.

All Branches, Themes, and Tranches derive from this structure.

---

# **2. Canonical Project Directory Structure**

```
/fugue_docs/
└── project/
    ├── preamble.md
    ├── project-decor.md
    ├── governance-envelope.md
    ├── naming-scheme.md
    ├── namespace-scheme.md
    ├── persona-map.md
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

- mission  
- vision  
- scope  
- boundaries  
- strategic objectives  
- constraints  
- risks  
- dependencies  
- success criteria  

This is the **root intent artefact** for the entire project.

---

## **3.2 project-decor.md**
Authored by: **Architect**  
Approved by: **Curator**

Contains:

- project‑level invariants  
- project‑level constraints  
- project‑level envelopes  
- cross‑branch architectural rules  
- cross‑theme architectural rules  
- structural expectations  

This is the **root architectural contract** for the entire project.

---

## **3.3 governance-envelope.md**
Authored by: **Curator**

Contains:

- governance posture  
- approval hierarchy  
- persona isolation rules  
- governance invariants  
- governance constraints  

This is the **root governance contract** for the entire project.

---

## **3.4 naming-scheme.md**
Authored by: **Curator**

Contains:

- naming conventions  
- naming invariants  
- naming constraints  
- naming propagation rules  

This is the **root naming scheme** for the entire project.

---

## **3.5 namespace-scheme.md**
Authored by: **Curator**

Contains:

- namespace root  
- namespace invariants  
- namespace constraints  
- namespace propagation rules  

This is the **root namespace scheme** for the entire project.

---

## **3.6 persona-map.md**
Authored by: **Curator**

Contains:

- active personas  
- persona sequencing rules  
- persona isolation rules  
- persona governance boundaries  

This is the **root persona map** for the entire project.

---

## **3.7 identity-propagation.md**
Authored by: **Curator**

Contains:

- identity propagation rules across Branches  
- identity propagation rules across Themes  
- identity propagation rules across Tranches  
- identity propagation rules across DECOR artefacts  
- identity propagation rules across documentation  

This is the **root identity propagation contract**.

---

## **3.8 documentation-envelope.md**
Authored by: **Curator**

Contains:

- documentation invariants  
- documentation constraints  
- documentation propagation rules  
- documentation namespace structure  

This is the **root documentation contract**.

---

## **3.9 bootstrap-log.md**
Authored by: **Curator**

Contains:

- summary of Project Bootstrap  
- project‑level invariants  
- governance posture  
- naming + namespace roots  
- persona map  
- identity propagation rules  
- documentation envelope  
- next steps (Branch creation)  

This is the **audit log** for Project Bootstrap.

---

## **3.10 README.md**
Authored by: **Curator or Methodologist**

Contains:

- overview of the project  
- explanation of the project‑level artefacts  
- instructions for Branch creators  
- instructions for Theme creators  
- instructions for Tranche creators  

This is the **human‑readable entrypoint** for the project.

---

# **4. Directory Invariants**

The following MUST always hold:

- No files may be added to `/fugue_docs/project/` except through governed updates.  
- No files may be removed except through governed archival.  
- No files may be renamed except through governed migration.  
- No persona may write outside their authorised artefacts.  
- All downstream artefacts MUST derive from these root contracts.  

---
