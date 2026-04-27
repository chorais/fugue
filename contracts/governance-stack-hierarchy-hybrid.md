# **Fugue v2.4 — Governance Stack + Hierarchy Hybrid Diagram**

```mermaid
flowchart LR

    %% ============================
    %% LEFT SIDE — GOVERNANCE STACK
    %% ============================

    subgraph STACK["🛡️ Governance Stack (Vertical Layers)"]
        
        L0["LAYER 0 — Governance Envelope<br/>Global Invariants • Persona Boundaries • Drift Rules"]

        subgraph L1["LAYER 1 — Structural Contracts"]
            DECOR["📘 DECOR Specification"]
            LIFECYCLE["🔄 Lifecycle Contract"]
            IDENTITY["🧬 Identity Propagation"]
            NAMING["🏷️ Naming Scheme"]
            NAMESPACE["📁 Namespace Scheme"]
            DOCS["📚 Documentation Envelope"]
            DETERMINISM["🎛️ Determinism Envelope"]
        end

        subgraph L2["LAYER 2 — Hierarchy Contracts"]
            P_CON["🏛️ Project Contracts"]
            B_CON["🌿 Branch Contracts"]
            T_CON["🎨 Theme Contracts"]
            TR_CON["📦 Tranche Contracts"]
        end

        subgraph L3["LAYER 3 — Execution Contracts"]
            TMAP["🗺️ Ticket Map Contract"]
            TICKET["🎫 Ticket Template"]
            REPLAY["🔁 Replay Trace"]
        end

        subgraph L4["LAYER 4 — Runtime Contracts"]
            IMPLEMENT["⚙️ Implementer Output"]
            AUDIT["🔍 Auditor"]
            VERIFY["✔️ Verifier"]
            RECON["🧾 Reconciliation"]
        end
    end

    %% ============================
    %% RIGHT SIDE — HIERARCHY
    %% ============================

    subgraph HIER["🏗️ Governance Hierarchy (Horizontal Layers)"]
        PROJECT["🏛️ Project"]
        BRANCH["🌿 Branch"]
        THEME["🎨 Theme"]
        TRANCHE["📦 Tranche"]
        TICKET_H["🎫 Ticket"]
    end

    PROJECT --> BRANCH
    BRANCH --> THEME
    THEME --> TRANCHE
    TRANCHE --> TICKET_H

    %% ============================
    %% CROSS-LINKS — STACK → HIERARCHY
    %% ============================

    %% Structural contracts apply to all hierarchy layers
    DECOR --> PROJECT
    DECOR --> BRANCH
    DECOR --> THEME
    DECOR --> TRANCHE

    LIFECYCLE --> PROJECT
    LIFECYCLE --> BRANCH
    LIFECYCLE --> THEME
    LIFECYCLE --> TRANCHE

    IDENTITY --> PROJECT
    IDENTITY --> BRANCH
    IDENTITY --> THEME
    IDENTITY --> TRANCHE

    NAMING --> PROJECT
    NAMING --> BRANCH
    NAMING --> THEME
    NAMING --> TRANCHE

    NAMESPACE --> PROJECT
    NAMESPACE --> BRANCH
    NAMESPACE --> THEME
    NAMESPACE --> TRANCHE

    DOCS --> PROJECT
    DOCS --> BRANCH
    DOCS --> THEME
    DOCS --> TRANCHE

    DETERMINISM --> PROJECT
    DETERMINISM --> BRANCH
    DETERMINISM --> THEME
    DETERMINISM --> TRANCHE

    %% Execution contracts apply from Tranche downward
    TR_CON --> TMAP
    TMAP --> TICKET_H
    TICKET --> TICKET_H
    REPLAY --> TICKET_H

    %% Runtime contracts apply to Tranche + Ticket
    IMPLEMENT --> TRANCHE
    IMPLEMENT --> TICKET_H

    AUDIT --> TRANCHE
    AUDIT --> TICKET_H

    VERIFY --> TRANCHE
    VERIFY --> TICKET_H

    RECON --> TRANCHE
```

---

# **How to Read the Hybrid Diagram**

## **1. Left side = Governance Stack (vertical)**
This is the **method architecture**:

- Layer 0 → Governance Envelope  
- Layer 1 → Structural Contracts  
- Layer 2 → Hierarchy Contracts  
- Layer 3 → Execution Contracts  
- Layer 4 → Runtime Contracts  

This is the **“what governs the system”** axis.

---

## **2. Right side = Governance Hierarchy (horizontal)**
This is the **governed object hierarchy**:

```
Project → Branch → Theme → Tranche → Ticket
```

This is the **“what is being governed”** axis.

---

## **3. Cross‑links = Contract Applicability**
These show:

- which contracts apply at which hierarchy layer  
- how DECOR propagates downward  
- how runtime contracts apply only at Tranche + Ticket  
- how structural contracts apply everywhere  
- how execution contracts apply from Tranche downward  

This is the **“how governance flows”** axis.

---
