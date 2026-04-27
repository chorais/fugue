# **Fugue Restarting Guide (v2.4)**  
Version: 2.4  
Status: Active (Frozen)  
*A lightweight, deterministic pattern for safely resuming work after time away*

Fugue is designed for long‑running, multi‑tranche, multi‑month projects.  
This guide explains how to **restart a project or tranche** after days, weeks, or months — without re‑deriving context, architecture, or governance.

Restarting is **not** a new phase or persona.  
It is a **safe operational pattern** for re‑establishing continuity.

---

# **1. When to Use This Guide**

Use this restart process when:

- you are returning to a project after time away  
- you are resuming a paused tranche  
- you are switching between multiple long‑running projects  
- a new engineer is picking up an existing Fugue project  
- you want to re‑establish context before starting the next tranche  

This guide ensures you restart safely, predictably, and without drift.

---

# **2. What You Need Before Restarting**

To restart a project or tranche, gather the following artefacts from the last completed tranche:

- **Preamble** (if continuing the same Theme)  
- **Reconciled DECOR**  
- **Closure Report**  
- **Ticket Map**  
- **Implementation Logs** (optional but helpful)  
- **Replay Traces** (optional but helpful)  

If the tranche was *mid‑execution*, also gather:

- the **last executed ticket**  
- the **Implementer’s output** for that ticket  

These artefacts re‑establish the full state of the project.

---

# **3. Restarting a Project (Beginning a New Tranche)**

If you are starting a **new tranche** after a break:

### **Step 1 — Start a fresh Orchestrator conversation**  
Attach:

- Preamble  
- Reconciled DECOR  
- Closure Report  

### **Step 2 — Use this restart prompt**

> **“You are the Orchestrator for this project.  
> I am returning after a break.  
> Please re‑establish context by summarising the current architectural state, the last tranche’s outcomes, and the next logical tranche.  
> Validate continuity with the Reconciled DECOR and propose the next tranche mission.”**

### **Step 3 — Review the Orchestrator’s summary**  
Confirm:

- architectural continuity  
- theme continuity  
- no drift  
- correct understanding of the last tranche  

### **Step 4 — Approve the next tranche**  
Then proceed with the standard v2.4 lifecycle:

```
Initiator → Orchestrator → Architect → Implementer → Auditor → Verifier → Closure
```

---

# **4. Restarting a Paused Tranche (Mid‑Execution)**

If you paused *mid‑tranche*, use this pattern.

### **Step 1 — Start a fresh Orchestrator conversation**  
Attach:

- the last executed ticket  
- the Implementer’s output  
- the Ticket Map  
- the Initial DECOR subset (if relevant)  

### **Step 2 — Use this restart prompt**

> **“You are the Orchestrator for this tranche.  
> I am returning after a break.  
> Please reconstruct the current execution state, identify the next ticket, and validate alignment with DECOR and the Ticket Map.”**

### **Step 3 — Review the Orchestrator’s reconstruction**  
Confirm:

- correct identification of the next ticket  
- correct interpretation of DECOR  
- no drift in understanding  
- no skipped acceptance criteria  

### **Step 4 — Resume the Implementer conversation**  
Start a fresh Implementer conversation with:

- the next ticket  
- the DECOR subset  
- any clarifications from the Orchestrator  

---

# **5. Restarting as a New Engineer (Handoff Scenario)**

If someone new is picking up the project:

### **Step 1 — Provide them with the artefact bundle**  
At minimum:

- Preamble  
- Reconciled DECOR  
- Closure Report  
- Ticket Map  

### **Step 2 — They run the same restart process**  
This ensures they inherit:

- architectural intent  
- decision history  
- execution state  
- remaining work  

### **Outcome:**  
A new engineer can safely resume a complex project without re‑deriving context.

---

# **6. What the Restart Process Guarantees**

This restart pattern ensures:

- **architectural continuity**  
- **intent continuity**  
- **ticket continuity**  
- **no re‑derivation of decisions**  
- **no re‑derivation of architecture**  
- **no re‑derivation of scope**  
- **no re‑derivation of execution state**  

It is intentionally lightweight — just enough structure to make restart safe and predictable.

---

# **7. Optional: Quick Restart Checklist**

- [ ] Gather Preamble  
- [ ] Gather Reconciled DECOR  
- [ ] Gather Closure Report  
- [ ] Gather Ticket Map  
- [ ] Gather last ticket + output (if mid‑tranche)  
- [ ] Start fresh Orchestrator  
- [ ] Use restart prompt  
- [ ] Validate summary  
- [ ] Resume next tranche or next ticket  

---

# **8. Summary**

The Restarting Guide ensures that:

- you never lose context  
- you never re‑derive architecture  
- you never re‑derive decisions  
- you can resume work in minutes, not hours  
- Fugue remains viable for long‑running, multi‑month, multi‑year projects  

This is what makes Fugue sustainable for real engineering work.

---
