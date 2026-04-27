# **tranche-lifecycle-workflow.md (v2.4)**  
**Tranche Lifecycle Workflow**  
Version: 2.4  
Status: Active  
Purpose: Define the deterministic, persona‑isolated lifecycle of a tranche.  
Methodology: Fugue Orchestration Method  
Implementation: Chorais  

---

# 1. Purpose

The Tranche Lifecycle Workflow defines how a tranche:

- is planned  
- is grounded in product and/or technical truth  
- generates its Ticket Map  
- produces **Initial DECOR**  
- executes its Ticket Loop  
- reconciles implementation with DECOR  
- closes deterministically  

This workflow ensures:

- governance‑first development  
- deterministic persona behaviour  
- DECOR‑anchored architecture  
- reproducible execution  
- auditability  
- replayability  

The **Curator** acts as the tranche’s upstream governance authority throughout the lifecycle.

---

# 2. Overview of Tranche Lifecycle

A tranche proceeds through the following deterministic phases:

1. **Bootstrap** (separate workflow)  
2. **Tranche Synopsis Creation**  
3. **Ticket Map Creation**  
4. **Initial DECOR Generation**  
5. **Ticket Loop Execution**  
6. **Reconciliation**  
7. **Epilogue Ticket Execution**  
8. **Tranche Closure**  

The key bifurcation occurs in **Phase 2 and 3**, depending on **Method A** or **Method B**.

The **Curator** provides governance approval at key checkpoints across these phases.

---

# 3. Method A vs Method B

Fugue supports two execution methods:

## 3.1 Method A — Product‑First (Conductor‑Led)

Used when:

- the tranche is product‑facing  
- the tranche defines new capabilities  
- the tranche is conceptual or architectural  
- the tranche is driven by business intent  

In Method A:

- Conductor creates the Tranche Synopsis  
- Orchestrator creates the Ticket Map  
- Architect generates Initial DECOR from the synopsis  
- Implementer executes tickets  
- Auditor reconciles  
- **Curator approves governance posture and key artefacts**  

## 3.2 Method B — Technical‑First (Implementer‑Led)

Used when:

- the tranche is deeply technical  
- the tranche depends on current implementation state  
- the tranche requires grounding in runtime behaviour  
- the tranche is a refactor, migration, or enforcement tranche  

In Method B:

- Implementer creates the Tranche Synopsis  
- Implementer creates the Ticket Map  
- Architect generates Initial DECOR from technical grounding  
- Conductor generates tickets  
- Auditor reconciles  
- **Curator approves governance posture and key artefacts**  

---

# 4. Phase 2 — Tranche Synopsis Creation

The Tranche Synopsis is the **high‑level definition** of the tranche.

It MUST include:

- tranche purpose  
- expected outcomes  
- dependencies on previous tranches  
- cross‑tranche impacts  
- tests that must be re‑run  
- architectural or product themes  
- governance posture  
- risks  
- assumptions  
- constraints  

The synopsis MUST be stored in:

```
/fugue_docs/specs/<tranche-name>/00-intake.md
```

---

## 4.1 Human Operator Role

The human operator is an authoritative governance actor.  
They may provide clarifications, corrections, or direction during synopsis creation.

Human clarifications MUST be treated as **governance‑level truth**.

---

## 4.2 Curator Role in Synopsis Creation (v2.4)

The **Curator** MUST:

- approve the Tranche Synopsis  
- validate governance posture  
- validate alignment with organisational intent  
- validate naming/namespace/identity propagation posture  
- validate evaluator metadata posture  
- confirm that human clarifications have been applied correctly  

The Curator MUST NOT:

- write the synopsis  
- generate technical content  
- override DECOR invariants  

Curator approval MUST be logged in:

```
/fugue_docs/specs/<tranche-name>/00-intake.md
```

---

## 4.3 Method A — Conductor Creates Synopsis  
*(unchanged except for Curator approval)*

## 4.4 Method B — Implementer Creates Synopsis  
*(unchanged except for Curator approval)*

---

# 5. Phase 3 — Ticket Map Creation

The Ticket Map is the **structured list of tickets** that the tranche will contain.

It MUST include:

- ticket IDs  
- ticket titles  
- short synopsis for each ticket  
- dependencies between tickets  
- dependencies on previous tranches  
- expected artefacts  
- expected test impacts  

The Ticket Map MUST be stored in:

```
/fugue_docs/tickets/<tranche-name>/ticket-map.md
```

---

## 5.1 Curator Role in Ticket Map Creation (v2.4)

The **Curator** MUST:

- approve the Ticket Map  
- validate governance posture  
- validate naming/namespace/identity propagation posture  
- validate evaluator metadata posture  
- validate cross‑tranche impacts  
- validate that human clarifications were applied correctly  

The Curator MUST NOT:

- write the Ticket Map  
- define technical sequencing  
- override DECOR invariants  

Curator approval MUST be logged in the Ticket Map.

---

## 5.2 Method A — Conductor Creates Ticket Map  
*(unchanged except for Curator approval)*

## 5.3 Method B — Implementer Creates Ticket Map  
*(unchanged except for Curator approval)*

## 5.4 Auditor Validation  
*(unchanged)*

---

# 6. Phase 4 — Initial DECOR Generation (Architect Persona)

The Architect MUST generate:

```
/fugue_docs/decors/<tranche-name>/decor.md
```

Initial DECOR MUST follow the canonical v2.4 DECOR template.

Initial DECOR MUST NOT be modified except through:

- governed DECOR Updates  
- reconciliation  

---

## 6.1 Curator Role in DECOR Approval (v2.4)

The **Curator** MUST:

- approve Initial DECOR  
- validate governance posture  
- validate invariants  
- validate naming/namespace/identity propagation posture  
- validate evaluator metadata posture  
- validate alignment with the Tranche Synopsis  

The Curator MUST NOT:

- write DECOR  
- modify DECOR  
- override architectural invariants  

Curator approval MUST be logged in:

```
/fugue_docs/decors/<tranche-name>/decor.md
```

---

## 6.2 Human Clarifications and DECOR  
*(unchanged)*

---

# 7. Phase 5 — Ticket Loop Execution  
*(unchanged except Curator is not involved)*

The Curator MUST NOT participate in execution.

---

# 8. Documentation Generation  
*(unchanged)*

The Curator may review documentation for governance alignment but does not produce it.

---

# 9. Phase 6 — Reconciliation

The Auditor MUST:

- compare implementation to Initial DECOR  
- classify drift  
- validate governance posture  
- validate determinism  
- validate documentation  

The Architect MUST:

- clarify DECOR  
- validate structural alignment  

The Conductor MUST:

- generate corrective tickets  

---

## 9.1 Curator Role in Reconciliation (v2.4)

The **Curator** MUST:

- approve reconciliation results  
- validate governance posture  
- validate naming/namespace/identity propagation posture  
- validate evaluator metadata posture  
- validate that drift classification is correct  
- validate that drift resolution aligns with governance  

Curator approval MUST be logged in:

```
/fugue_docs/verification/<tranche-name>/drift/drift-summary.md
```

---

# 10. Phase 7 — Epilogue Ticket

The Conductor MUST generate the epilogue ticket.  
The Implementer MUST implement it.  
The Auditor MUST validate it.

---

## 10.1 Curator Role in Epilogue (v2.4)

The **Curator** MUST:

- approve the epilogue ticket  
- approve drift resolution  
- validate governance posture  
- validate naming/namespace/identity propagation posture  

Curator approval MUST be logged in:

```
/fugue_docs/closure/<tranche-name>/closure-report.md
```

---

# 11. Phase 8 — Tranche Closure

A tranche may close only when:

- all tickets are implemented  
- all drift is resolved  
- reconciled DECOR is produced  
- all tests pass  
- governance posture is stable  
- **Curator approves closure**  
- human operator approves closure  

Curator approval MUST be logged in:

```
/fugue_docs/closure/<tranche-name>/closure-log.md
```

---

# 12. Summary

The Tranche Lifecycle Workflow ensures:

- deterministic execution  
- persona isolation  
- DECOR‑anchored architecture  
- governance‑first reasoning  
- reproducibility  
- auditability  
- replayability  

**The Curator provides governance authority across the entire lifecycle**, approving:

- the Tranche Synopsis  
- the Ticket Map  
- Initial DECOR  
- reconciliation  
- epilogue  
- tranche closure  

Method A and Method B provide flexibility for:

- product‑driven tranches  
- technical‑driven tranches  

---
