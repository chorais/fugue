# **Restart Continuity Contract (RCC) — v2.4**  
Version: 2.4  
Status: Active  
Methodology: Fugue Orchestration Method v2.4  
Governance Authority: Curator  

---

# 1. Purpose  

The Restart Continuity Contract (RCC) defines the minimal, deterministic rules required to safely restart a Fugue project or tranche after a period of inactivity.

RCC ensures that:

- architectural state is restored from **Reconciled DECOR**  
- tranche intent is restored from the **Preamble**  
- execution state is restored from the **Ticket Map** and **Ticket Bundle**  
- the Orchestrator re‑establishes context deterministically  
- no architectural or intent re‑derivation occurs  
- restart is safe, predictable, and aligned with the Fugue lifecycle  
- naming, namespace, and identity propagation rules remain preserved  

RCC is a **continuity wrapper** around the Orchestrator bootstrap process.  
It does **not** introduce new personas, phases, or lifecycle stages.

---

# 2. Scope  

RCC applies when:

- restarting a **new tranche** after a break  
- resuming a **paused tranche** mid‑execution  
- onboarding a **new engineer** to an existing Fugue project  
- switching between multiple long‑running projects  

RCC does **not** apply to:

- initial project creation  
- normal tranche bootstrap  
- normal ticket execution  
- verification  
- governance events  

---

# 3. Required Inputs (Restart Substrate)  

The Orchestrator MUST be seeded with the following governed artefacts:

## 3.1 Preamble  
Defines the mission, scope, and boundaries of the last tranche.

## 3.2 Reconciled DECOR  
The authoritative architectural ledger at the end of the last tranche.

## 3.3 Closure Report  
Summarises what was completed and why the tranche ended.

## 3.4 Ticket Map  
Defines the planned work for the tranche.

## 3.5 Ticket Bundle  
Defines the executed work.

## 3.6 Implementation Logs *(optional)*  
Provides execution evidence.

## 3.7 Replay Traces *(optional)*  
Provides runtime behaviour evidence.

## 3.8 Persona Boundaries  
Ensures the Orchestrator remains persona‑bounded during restart.

## 3.9 Documentation Envelope  
Defines where restart outputs MUST be written under `/fugue_docs`.

---

# 4. Orchestrator Responsibilities Under RCC  

When operating under RCC, the Orchestrator MUST:

## 4.1 Reconstruct Context  
Rebuild the full project/tranche state from governed artefacts.

## 4.2 Validate Architectural Continuity  
Ensure Reconciled DECOR is internally consistent and aligns with the Preamble.

## 4.3 Validate Execution Continuity  
Ensure the Ticket Map and Ticket Bundle align with the Closure Report.

## 4.4 Validate Naming, Namespace, and Identity Continuity  
Ensure all governed surfaces remain consistent with v2.4 rules.

## 4.5 Identify the Next Action  
Depending on state:

- propose the **next tranche** (if restarting at tranche boundaries), or  
- identify the **next ticket** (if mid‑execution)  

## 4.6 Remain Persona‑Bounded  
The Orchestrator MUST NOT:

- generate new architecture  
- reinterpret DECOR  
- modify DECOR  
- modify tickets  
- modify the Ticket Map  
- perform implementation  
- perform verification  
- enforce governance  
- reason about evaluator mechanics  
- drift into other personas  

## 4.7 Produce a Restart Summary  
A deterministic summary containing:

- current architectural state  
- current execution state  
- remaining work  
- next action  
- continuity validation  

---

# 5. Operator Responsibilities Under RCC  

The operator MUST:

- attach all required artefacts  
- start a **fresh Orchestrator conversation**  
- use the Restart Seed Prompt  
- validate the Orchestrator’s reconstruction  
- approve the next tranche or next ticket  

The operator MUST NOT:

- reuse old Orchestrator conversations  
- attach artefacts from other tranches  
- manually re‑derive architecture or intent  

---

# 6. Outputs of RCC  

The Orchestrator MUST produce:

## 6.1 Restart Summary  
A deterministic reconstruction of:

- architectural state  
- tranche state  
- execution state  

## 6.2 Continuity Validation  
Confirmation that:

- Reconciled DECOR is authoritative  
- Ticket Map and Ticket Bundle align  
- Closure Report is consistent  
- naming, namespace, and identity propagation rules remain intact  

## 6.3 Next Action Proposal  
Either:

- the next tranche mission, or  
- the next ticket  

## 6.4 Restart Log  
A traceable record of the restart process stored under:

```
/fugue_docs/logs/<tranche-name>/restart-log.md
```

---

# 7. Guarantees  

RCC guarantees:

- **no re‑derivation** of architecture  
- **no re‑derivation** of intent  
- **no re‑derivation** of execution state  
- deterministic restart  
- safe continuation  
- persona‑bounded behaviour  
- lifecycle alignment  
- naming, namespace, and identity propagation continuity  
- audit‑ready reconstruction  

---