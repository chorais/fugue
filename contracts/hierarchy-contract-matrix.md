# **Hierarchy × Contract Matrix (v2.4)**  
**Status:** Authoritative  
**Governance Authority:** Curator  
**Purpose:** Define contract applicability across Project → Branch → Theme → Tranche  

---

# **1. Matrix Overview**

This matrix defines:

- which contracts apply at each hierarchy layer  
- which contracts govern structural behaviour  
- which contracts govern execution  
- which contracts govern runtime  
- which contracts govern continuity  
- which contracts govern metadata, naming, namespace, identity, determinism  

All entries are **MUST‑apply** unless otherwise stated.

---

# **2. Hierarchy × Contract Matrix**

```mermaid
flowchart LR

    subgraph PROJECT["🏛️ Project Layer"]
        P_DECOR["DECOR ✓"]
        P_LIFECYCLE["Lifecycle ✓"]
        P_IDENTITY["Identity ✓"]
        P_NAMING["Naming ✓"]
        P_NAMESPACE["Namespace ✓"]
        P_DOCS["Documentation ✓"]
        P_DETERMINISM["Determinism ✓"]
        P_TMAP["Ticket Map ✓"]
        P_REPLAY["Replay Trace ✓"]
        P_AUDIT["Auditor ✓"]
        P_VERIFY["Verifier ✓"]
        P_RCC["RCC ✓"]
    end

    subgraph BRANCH["🌿 Branch Layer"]
        B_DECOR["DECOR ✓"]
        B_LIFECYCLE["Lifecycle ✓"]
        B_IDENTITY["Identity ✓"]
        B_NAMING["Naming ✓"]
        B_NAMESPACE["Namespace ✓"]
        B_DOCS["Documentation ✓"]
        B_DETERMINISM["Determinism ✓"]
        B_TMAP["Ticket Map ✓"]
        B_REPLAY["Replay Trace ✓"]
        B_AUDIT["Auditor ✓"]
        B_VERIFY["Verifier ✓"]
        B_RCC["RCC ✓"]
    end

    subgraph THEME["🎨 Theme Layer"]
        T_DECOR["DECOR ✓"]
        T_LIFECYCLE["Lifecycle ✓"]
        T_IDENTITY["Identity ✓"]
        T_NAMING["Naming ✓"]
        T_NAMESPACE["Namespace ✓"]
        T_DOCS["Documentation ✓"]
        T_DETERMINISM["Determinism ✓"]
        T_TMAP["Ticket Map ✓"]
        T_REPLAY["Replay Trace ✓"]
        T_AUDIT["Auditor ✓"]
        T_VERIFY["Verifier ✓"]
        T_RCC["RCC ✓"]
    end

    subgraph TRANCHE["📦 Tranche Layer"]
        TR_DECOR["DECOR ✓"]
        TR_LIFECYCLE["Lifecycle ✓"]
        TR_IDENTITY["Identity ✓"]
        TR_NAMING["Naming ✓"]
        TR_NAMESPACE["Namespace ✓"]
        TR_DOCS["Documentation ✓"]
        TR_DETERMINISM["Determinism ✓"]
        TR_TMAP["Ticket Map ✓"]
        TR_TICKET["Ticket Template ✓"]
        TR_REPLAY["Replay Trace ✓"]
        TR_AUDIT["Auditor ✓"]
        TR_VERIFY["Verifier ✓"]
        TR_RECON["Reconciliation ✓"]
        TR_RCC["RCC ✓"]
        TR_TRP["TRP ✓"]
    end

    PROJECT --> BRANCH
    BRANCH --> THEME
    THEME --> TRANCHE
```

---

# **3. Matrix Table (Textual Form)**

| Contract | Project | Branch | Theme | Tranche |
|---------|---------|--------|--------|---------|
| Governance Envelope | ✓ | ✓ | ✓ | ✓ |
| DECOR Specification | ✓ | ✓ | ✓ | ✓ |
| Lifecycle Contract | ✓ | ✓ | ✓ | ✓ |
| Identity Propagation | ✓ | ✓ | ✓ | ✓ |
| Naming Scheme | ✓ | ✓ | ✓ | ✓ |
| Namespace Scheme | ✓ | ✓ | ✓ | ✓ |
| Documentation Envelope | ✓ | ✓ | ✓ | ✓ |
| Determinism Envelope | ✓ | ✓ | ✓ | ✓ |
| Ticket Map Contract | ✓ | ✓ | ✓ | ✓ |
| Ticket Template | — | — | — | ✓ |
| Replay Trace Contract | ✓ | ✓ | ✓ | ✓ |
| Auditor Contract | ✓ | ✓ | ✓ | ✓ |
| Verifier Contract | ✓ | ✓ | ✓ | ✓ |
| Reconciliation Contract | — | — | — | ✓ |
| Restart Continuity Contract (RCC) | ✓ | ✓ | ✓ | ✓ |
| Tranche Resume Pattern (TRP) | — | — | — | ✓ |

---

# **4. Completeness**

This matrix is:

- hierarchy‑complete  
- governance‑aligned  
- naming‑aligned  
- namespace‑aligned  
- identity‑aligned  
- determinism‑aligned  
- lifecycle‑aligned  
- documentation‑aligned  
- reconciliation‑aligned  

This is the **final, authoritative v2.4 Hierarchy × Contract Matrix**.
