# **Tranche Resume Pattern (TRP) — v2.4**  
Version: 2.4  
Status: Active  
Methodology: Fugue Orchestration Method v2.4  
Governance Authority: Curator  

---

# 1. Purpose  

The Tranche Resume Pattern (TRP) defines the deterministic, governed procedure for resuming a paused tranche mid‑execution.

TRP ensures that:

- the Orchestrator reconstructs the tranche state  
- architectural continuity is preserved  
- execution continuity is preserved  
- naming, namespace, and identity propagation continuity is preserved  
- the next ticket is identified deterministically  
- no re‑derivation of architecture or intent occurs  
- the Implementer resumes safely and predictably  

TRP is a **continuity wrapper** around the Orchestrator’s context‑reconstruction responsibilities.  
It does **not** introduce new personas or lifecycle stages.

---

# 2. Scope  

TRP applies when:

- a tranche was paused mid‑execution  
- some tickets were completed but not all  
- the Orchestrator must re‑establish context  
- the next ticket must be identified  
- the tranche must resume without re‑derivation  

TRP does **not** apply to:

- restarting a new tranche (use RCC)  
- verification  
- initial bootstrap  
- ticket execution  
- governance events  

---

# 3. Required Inputs (Resume Substrate)  

To resume a paused tranche, the operator MUST attach:

## 3.1 Ticket Map  
Defines the full set of planned work.

## 3.2 Ticket Bundle  
Defines the executed work and ticket definitions.

## 3.3 Last Executed Ticket  
The most recent ticket completed before the pause.

## 3.4 Implementer Output for the Last Ticket  
Provides execution evidence.

## 3.5 DECOR  
The authoritative architectural ledger for the tranche.

## 3.6 DECOR Updates *(if applicable)*  
If the tranche had DECOR deltas.

## 3.7 Preamble *(optional)*  
Useful if the pause was long.

## 3.8 Persona Boundaries  
Ensures the Orchestrator remains in Resume Mode.

## 3.9 Documentation Envelope  
Defines where resume outputs MUST be written under `/fugue_docs`.

## 3.10 Naming / Namespace / Identity Metadata  
Ensures continuity of v2.4 governance surfaces.

---

# 4. Orchestrator Responsibilities Under TRP  

When operating under TRP, the Orchestrator MUST:

## 4.1 Reconstruct Tranche State  
Rebuild the tranche state from governed artefacts:

- Ticket Map  
- Ticket Bundle  
- last ticket output  
- DECOR and DECOR updates  

## 4.2 Validate Architectural Continuity  
Ensure the next ticket aligns with DECOR and DECOR updates.

## 4.3 Validate Execution Continuity  
Ensure the last ticket’s output is consistent with:

- Ticket Map  
- dependencies  
- sequencing  
- metadata  

## 4.4 Validate Naming / Namespace / Identity Continuity  
Ensure all governed surfaces remain consistent with v2.4 rules.

## 4.5 Identify the Next Ticket  
The Orchestrator MUST:

- determine which tickets remain  
- confirm ordering  
- confirm dependencies  
- select the next executable ticket  
- ensure persona routing correctness  

## 4.6 Remain Persona‑Bounded  
The Orchestrator MUST NOT:

- modify DECOR  
- reinterpret DECOR  
- generate new tickets  
- modify the Ticket Map  
- perform implementation  
- perform verification  
- enforce governance  
- reason about evaluator mechanics  
- drift into other personas  

## 4.7 Produce a Resume Summary  
A deterministic summary containing:

- completed tickets  
- remaining tickets  
- next ticket  
- continuity validation  
- naming / namespace / identity continuity status  

---

# 5. Operator Responsibilities Under TRP  

The operator MUST:

- attach all required artefacts  
- start a **fresh Orchestrator conversation**  
- use the Resume Seed Prompt  
- validate the Orchestrator’s reconstruction  
- approve the next ticket  
- start a fresh Implementer conversation  

The operator MUST NOT:

- reuse old Orchestrator conversations  
- attach artefacts from other tranches  
- manually re‑derive architecture or execution state  

---

# 6. Resume Seed Prompt  

Paste this into Copilot Chat after attaching the resume substrate.

---

## **RESUME SEED PROMPT**

You are operating as the **Orchestrator persona** in **Resume Mode**, as defined by the attached methodology and persona contracts.

I am resuming tranche <ID> after a pause.  
Your task is to reconstruct the tranche state and identify the next ticket.

You MUST:

- summarise completed work  
- summarise remaining work  
- validate continuity with DECOR  
- validate naming, namespace, and identity propagation continuity  
- identify the next executable ticket  
- remain strictly within Orchestrator persona boundaries  
- avoid architectural design  
- avoid implementation  
- avoid verification  
- avoid governance enforcement  
- avoid persona drift  

Begin by acknowledging the artefacts and confirming readiness to reconstruct the tranche state.

---

# 7. Main Prompt  

After sending the seed prompt:

> **“Reconstruct the tranche state and identify the next ticket.”**

---

# 8. Expected Orchestrator Behaviour  

The Orchestrator MUST:

1. Acknowledge the artefacts  
2. Confirm persona boundaries  
3. Reconstruct the tranche state  
4. Validate architectural continuity  
5. Validate execution continuity  
6. Validate naming / namespace / identity continuity  
7. Identify the next ticket  
8. Produce a deterministic Resume Summary  

This completes the Resume Pattern.

---

# 9. Outputs of TRP  

The Orchestrator MUST produce:

## 9.1 Resume Summary  
A deterministic reconstruction of:

- completed tickets  
- remaining tickets  
- next ticket  

## 9.2 Continuity Validation  
Confirmation that:

- DECOR is aligned  
- Ticket Map and Ticket Bundle are consistent  
- the last ticket’s output is valid  
- naming / namespace / identity propagation rules remain intact  

## 9.3 Next Ticket Identification  
The authoritative next step.

## 9.4 Resume Log  
A traceable record of the resume process stored under:

```
/fugue_docs/logs/<tranche-name>/resume-log.md
```

---

# 10. Guarantees  

TRP guarantees:

- no re‑derivation of architecture  
- no re‑derivation of intent  
- no re‑derivation of execution state  
- deterministic resumption  
- safe continuation  
- persona‑bounded behaviour  
- lifecycle alignment  
- naming / namespace / identity propagation continuity  
- audit‑ready reconstruction  

---