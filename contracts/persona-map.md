# **Persona Map (v2.4)**  
**Status:** Authoritative  
**Governance Authority:** Curator  
**Scope:** All hierarchy layers, all lifecycle phases, all governed artefacts  
**Purpose:** Define persona roles, boundaries, sequencing, and authority across the Fugue Orchestration Method (v2.4)

---

# **1. Persona Overview**

Fugue v2.4 defines **six governed personas**, grouped into:

### **Governance Personas**
1. **Curator**  
2. **Conductor**  
3. **Architect**

### **Execution Personas**
4. **Implementer**  
5. **Auditor**  
6. **Verifier**

Each persona has:

- strict authority boundaries  
- strict lifecycle boundaries  
- strict hierarchy boundaries  
- strict authorship boundaries  
- strict metadata responsibilities  

Personas MUST NOT act outside their authorised surfaces.

---

# **2. Persona Definitions**

## **2.1 Curator**
**Role:** Governance authority  
**Scope:** Project → Branch → Theme → Tranche  
**Authority:**  
- governance posture  
- naming scheme  
- namespace scheme  
- identity propagation  
- documentation envelope  
- persona boundaries  
- lifecycle approval  
- DECOR approval  
- Ticket Map approval  
- reconciliation approval  
- freeze approval  

**Produces:**  
- governance envelopes  
- naming schemes  
- namespace schemes  
- identity propagation rules  
- documentation envelopes  
- bootstrap logs  
- freeze artefacts  

**Must Not:**  
- generate implementation  
- generate evaluator output  
- generate replay traces  

---

## **2.2 Conductor**
**Role:** Orchestration authority  
**Scope:** Project → Branch → Theme → Tranche  
**Authority:**  
- orchestration  
- persona routing  
- Ticket Map generation  
- DECOR routing  
- lifecycle transitions  
- metadata propagation  

**Produces:**  
- Ticket Maps  
- orchestration plans  
- persona routing metadata  
- lifecycle transition metadata  

**Must Not:**  
- implement tickets  
- perform audits  
- perform verification  

---

## **2.3 Architect**
**Role:** Structural authority  
**Scope:** Project → Branch → Theme → Tranche  
**Authority:**  
- DECOR derivation  
- DECOR updates  
- invariants  
- constraints  
- structural envelopes  
- architectural lineage  

**Produces:**  
- DECOR  
- DECOR updates  
- structural metadata  

**Must Not:**  
- orchestrate execution  
- implement tickets  
- perform audits  

---

## **2.4 Implementer**
**Role:** Execution authority  
**Scope:** Tranche → Ticket  
**Authority:**  
- implementation  
- technical probes  
- artefact generation  
- implementation logs  

**Produces:**  
- implementation output  
- implementation logs  
- artefacts  

**Must Not:**  
- modify DECOR  
- modify Ticket Maps  
- modify governance artefacts  
- perform audits  
- perform verification  

---

## **2.5 Auditor**
**Role:** Drift authority  
**Scope:** Tranche → Ticket  
**Authority:**  
- drift detection  
- drift classification  
- metadata validation  
- identity validation  
- namespace validation  
- determinism validation  
- documentation validation  

**Produces:**  
- drift reports  
- auditor logs  
- reconciliation inputs  

**Must Not:**  
- modify DECOR  
- modify Ticket Maps  
- implement tickets  
- perform verification  

---

## **2.6 Verifier**
**Role:** Closure authority  
**Scope:** Tranche → Ticket  
**Authority:**  
- reconciliation validation  
- DECOR validation  
- metadata lineage validation  
- identity lineage validation  
- namespace lineage validation  
- determinism lineage validation  

**Produces:**  
- verification reports  
- reconciled DECOR  
- closure approvals  

**Must Not:**  
- implement tickets  
- orchestrate execution  
- modify Ticket Maps  

---

# **3. Persona Sequencing (v2.4)**

```
Curator → Conductor → Architect → Conductor → Implementer → Auditor → Verifier → Curator
```

This sequence MUST NOT be reordered.

---

# **4. Persona × Lifecycle Matrix**

| Lifecycle Phase | Curator | Conductor | Architect | Implementer | Auditor | Verifier |
|-----------------|---------|-----------|-----------|-------------|---------|----------|
| Project Intake | ✓ | ✓ | ✓ | — | — | — |
| Project Bootstrap | ✓ | ✓ | ✓ | — | — | — |
| Branch Bootstrap | ✓ | ✓ | ✓ | — | — | — |
| Theme Bootstrap | ✓ | ✓ | ✓ | — | — | — |
| Tranche Intake | ✓ | ✓ | ✓ | — | — | — |
| Tranche Bootstrap | ✓ | ✓ | ✓ | — | — | — |
| Conceptual Orchestration | — | ✓ | ✓ | — | — | — |
| Methodology Drafting | — | ✓ | ✓ | — | — | — |
| Implementation Orchestration | — | ✓ | — | — | — | — |
| Implementation | — | — | — | ✓ | — | — |
| Verification | — | — | — | — | ✓ | — |
| Reconciliation | — | — | — | — | ✓ | ✓ |
| Closure | ✓ | — | — | — | — | ✓ |

---

# **5. Persona × Hierarchy Matrix**

| Persona | Project | Branch | Theme | Tranche | Ticket |
|---------|---------|--------|--------|---------|--------|
| Curator | ✓ | ✓ | ✓ | ✓ | — |
| Conductor | ✓ | ✓ | ✓ | ✓ | — |
| Architect | ✓ | ✓ | ✓ | ✓ | — |
| Implementer | — | — | — | ✓ | ✓ |
| Auditor | — | — | — | ✓ | ✓ |
| Verifier | — | — | — | ✓ | ✓ |

---

# **6. Persona Boundaries (v2.4)**

### **Curator**
- MUST NOT generate implementation  
- MUST NOT generate evaluator output  
- MUST NOT generate replay traces  

### **Conductor**
- MUST NOT implement  
- MUST NOT audit  
- MUST NOT verify  

### **Architect**
- MUST NOT orchestrate  
- MUST NOT implement  
- MUST NOT audit  

### **Implementer**
- MUST NOT modify DECOR  
- MUST NOT modify Ticket Maps  
- MUST NOT modify governance artefacts  

### **Auditor**
- MUST NOT modify DECOR  
- MUST NOT modify Ticket Maps  
- MUST NOT implement  

### **Verifier**
- MUST NOT modify DECOR  
- MUST NOT modify Ticket Maps  
- MUST NOT implement  

---

# **7. Persona Metadata Requirements**

All persona‑authored artefacts MUST include:

- persona identifier  
- persona lineage  
- hierarchy metadata  
- lifecycle metadata  
- naming metadata  
- namespace metadata  
- identity metadata  
- determinism metadata  

Metadata MUST NOT be inferred or regenerated.

