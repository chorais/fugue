# 🎼 **concern.md (v2.4)**  
**Concern — DC‑<number>**  
Version: 2.4  
Personas: Implementer (Author), Architect (Triager), Orchestrator (Scheduler)  
Mode: Implementation Mode  
Lifecycle Context: Cross‑Phase (Forward‑Looking)  

---

# 0. Metadata

```yaml
metadata:
  concern-id: "DC-<number>"
  detected-during: "<ticket-id>"
  detected-by: "<implementer-identity>"
  severity: "Low|Medium|High|Critical"
  status: "Open|Triaged|Scheduled|Closed"
  triage-owner: "<architect-identity>"
  scheduled-in: "<tranche-or-ticket-id|null>"
  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"
  governance-envelope: "<id>"
  evaluator-categories: []
  evaluator-diagnostics: []
  persona-routing-summary: "Implementer|Architect|Orchestrator"
  lifecycle-context: "cross-phase"
  last-updated: "<YYYY-MM-DD>"
```

---

# 1. Concern Summary  
A concise description of the concern.

Summary MUST:

- describe the issue  
- describe the affected surfaces  
- describe the forward impact  
- describe naming/namespace/identity propagation implications  
- reference relevant DECOR surfaces  

Summary MUST NOT:

- include implementation detail  
- include architectural decisions  
- include governance commentary  
- contradict DECOR  
- contradict naming/namespace/identity propagation rules  

---

# 2. Why This Matters  
Define the relevance of the concern.

This section MUST:

- describe the operational impact  
- describe the developer impact  
- describe the forward risk  
- describe naming/namespace/identity propagation risk  
- describe determinism envelope implications  
- describe evaluator metadata implications  

This section MUST NOT:

- introduce requirements  
- introduce architectural reasoning  
- introduce governance reasoning  

---

# 3. Draft Follow‑Up Ticket  
Define the draft ticket that would resolve the concern.

This section MUST include:

- draft ticket ID (unassigned)  
- draft ticket title  
- draft ticket scope  
- naming/namespace/identity propagation considerations  
- determinism envelope considerations  
- evaluator metadata considerations  

Draft ticket MUST align with the **Ticket Template (v2.4)**.

This section MUST NOT:

- assign a persona  
- assign acceptance criteria beyond draft form  
- assign lifecycle phase  

---

# 4. Business Requirements  
Define business‑level requirements for resolving the concern.

Requirements MUST be:

- deterministic  
- non‑narrative  
- non‑architectural  
- non‑implementation  
- aligned with naming/namespace/identity propagation rules  
- aligned with governance envelopes  
- aligned with DECOR schema  

Requirements MUST NOT:

- contradict governance posture  
- contradict DECOR  
- contradict identity propagation rules  

---

# 5. Technical Requirements  
Define technical requirements for resolving the concern.

Requirements MUST include:

- required surfaces  
- required behaviours  
- required metadata  
- required determinism guarantees  
- required naming/namespace/identity propagation guarantees  
- required evaluator metadata guarantees  

Requirements MUST NOT:

- include implementation detail  
- include persona‑specific instructions  
- contradict DECOR  

---

# 6. Acceptance Criteria  
Define acceptance criteria for resolving the concern.

Acceptance criteria MUST be:

- deterministic  
- testable  
- unambiguous  
- aligned with DECOR  
- aligned with governance posture  
- aligned with naming/namespace/identity propagation rules  
- aligned with determinism envelope  
- aligned with evaluator metadata schema  

Acceptance criteria MUST NOT:

- include implementation detail  
- include architectural decisions  

---

# 7. Notes (Optional)  
Record any additional notes relevant to the concern.

Notes MUST NOT:

- modify the concern  
- modify requirements  
- modify acceptance criteria  
- introduce architectural or governance reasoning  

---

# 8. Lifecycle Integration  
Record lifecycle‑level integration.

This section MUST include:

- Implementer raised  
- Architect triaged  
- Orchestrator scheduled (if applicable)  
- Ticket reference (if scheduled)  
- naming/namespace/identity propagation lifecycle impact  
- evaluator metadata lifecycle impact  
- Closure status  

This section MUST NOT:

- include implementation detail  
- include architectural decisions  