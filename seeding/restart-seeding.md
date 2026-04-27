# **Fugue Method — Restart Seeding Guide**  
### *How to safely restart a Fugue project or tranche after time away*

Version: 2.4  
This document describes the **exact steps** required to restart a Fugue project or tranche after days, weeks, or months.  
It ensures that the **Conductor** can re‑establish context deterministically, validate architectural continuity, and resume the lifecycle without re‑deriving decisions or intent.

This is a **lightweight operational guide**, not a new persona or phase.  
It aligns with the structure of the other official seeding guides.

---

# **1. Purpose of the Restart Seeding Process**

The Restart Seeding Process is responsible for:

- re‑establishing project or tranche context  
- reconstructing architectural state from artefacts  
- validating continuity with **Reconciled DECOR**  
- identifying the next tranche or next ticket  
- ensuring no drift occurred during the pause  
- enabling safe resumption of work  

Restart Mode must **not**:

- generate new architecture  
- reinterpret DECOR  
- modify tickets  
- perform implementation  
- perform verification  
- perform orchestration beyond context reconstruction  
- reason about future tranches beyond proposing the next logical step  

This guide ensures restart is deterministic, safe, and aligned with the Fugue lifecycle.

---

# **2. Required Files to Attach**

When restarting a project or tranche, attach the following artefacts from the **most recent completed tranche** (or the partially completed tranche if mid‑execution).

These files form the **restart substrate**.

---

### **2.1 Preamble** *(if continuing the same theme)*  
```
/fugue_docs/specs/<tranche-name>/preamble.md
```
Defines the mission and boundaries of the last tranche.

---

### **2.2 Reconciled DECOR**  
```
/fugue_docs/decors/<tranche-name>/reconciled-decor.md
```
The authoritative architectural state at the end of the last tranche.

---

### **2.3 Closure Log**  
```
/fugue_docs/closure/<tranche-name>/closure-log.md
```
Summarises what was completed and why the tranche ended.

---

### **2.4 Ticket Map**  
```
/fugue_docs/tickets/<tranche-name>/ticket-map.md
```
Defines the planned work for the tranche.

---

### **2.5 Ticket Bundle**  
```
/fugue_docs/tickets/<tranche-name>/tickets/*.md
```
Defines the executed work.

---

### **2.6 Implementation Logs** *(optional but recommended)*  
```
/fugue_docs/tickets/<tranche-name>/implementation-logs/*.md
```
Provides execution evidence.

---

### **2.7 Replay Traces** *(optional)*  
```
/fugue_docs/verification/<tranche-name>/replay-traces/*.md
```
Provides runtime behaviour evidence.

---

### **2.8 Persona Boundaries**  
```
/fugue/contracts/persona-boundaries.md
```
Ensures the Conductor remains within Restart Mode.

---

### **2.9 Documentation Envelope**  
```
/fugue/contracts/documentation-envelope.md
```
Defines where restart outputs (if any) should be written.

---

# **3. Restart Seed Prompt**

Paste the following prompt into Copilot Chat **after attaching all required files**.

---

## **RESTART SEED PROMPT (v2.4)**

You are operating as the **Conductor persona** in **Restart Mode**, as defined by the attached methodology and persona contracts.

I am returning to this project after a break.  
Your task is to **re‑establish context** for tranche `<tranche-name>` by reconstructing:

- the architectural state (from Reconciled DECOR)  
- the tranche’s mission and boundaries (from the Preamble)  
- the completed work (from the Ticket Bundle)  
- the remaining work (from the Ticket Map)  
- the final state of the last tranche (from the Closure Log)  

You MUST:

- summarise the current project state  
- validate continuity with Reconciled DECOR  
- identify the next logical tranche OR the next ticket  
- remain strictly within Conductor persona boundaries  
- avoid architectural design  
- avoid implementation  
- avoid verification  
- avoid governance enforcement  
- avoid persona drift  

Your output MUST be:

- deterministic  
- traceable  
- aligned with the Documentation Envelope  
- complete and unambiguous  

Acknowledge the artefacts and confirm readiness to reconstruct context.

---

# **4. Main Prompt**

After sending the seed prompt, provide the restart instruction:

> **“Reconstruct the current state and identify the next tranche or next ticket.”**

The Conductor will then perform context reconstruction.

---

# **5. Expected Conductor Behaviour**

After receiving the seed prompt and files, the Conductor will:

1. Acknowledge the restart artefacts  
2. Confirm persona boundaries  
3. Summarise the architectural state  
4. Summarise the last tranche’s outcomes  
5. Identify remaining work  
6. Validate continuity with Reconciled DECOR  
7. Propose:  
   - the next tranche (if starting fresh), or  
   - the next ticket (if mid‑execution)  

This completes the Restart Phase.

---

# **6. Notes for Operators**

- Always start a **fresh Conductor conversation** for restart  
- Do **not** reuse the Conductor from the previous tranche  
- Do **not** attach artefacts from other tranches  
- If mid‑tranche, attach the last executed ticket + Implementer output  
- Restart Mode is **not** a new persona — it is a constrained Conductor mode  

---

# **7. Summary**

This document provides the complete, deterministic procedure for restarting a Fugue project or tranche.  
Following this process ensures:

- safe resumption  
- architectural continuity  
- no re‑derivation of decisions  
- no loss of context  
- predictable lifecycle progression  

This is the official, end‑user‑facing guide for restarting work in the Fugue Method.

---
