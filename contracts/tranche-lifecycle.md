# **Tranche Lifecycle Contract (v2.4)**  
Version: 2.4  
Status: Active  
Methodology: Fugue Orchestration Method

---

# 1. Purpose

This contract defines the **deterministic, governed lifecycle** of a Fugue tranche.

It establishes:

- the six‑phase lifecycle  
- strict persona isolation  
- governed DECOR derivation and updates  
- metadata‑driven lifecycle transitions  
- deterministic ticket execution  
- governed documentation routing  
- two‑stage reconciliation (Auditor → Verifier)  
- publication of **Reconciled DECOR** as the final governed artefact  
- Curator approval as the final governance gate  

This lifecycle is substrate‑agnostic and applies across all AI systems participating in orchestration.

---

# 2. Lifecycle Phases (v2.4)

Fugue v2.4 defines **six governed phases**:

1. **Intake** — Curator defines intent  
2. **Bootstrap** — Curator prepares the tranche  
3. **Orchestration** — Conductor (Conceptual) + Orchestrator (Practical)  
4. **Implementation** — Implementer executes tickets  
5. **Verification** — Auditor detects drift → Verifier validates corrections  
6. **Closure** — Conductor + Curator approve tranche closure  

Each phase has strict persona boundaries, metadata requirements, and governed artefacts.

---

# 2.0 Phase 0 — Intake  
**Conversation:** Intake Conversation  
**Mode:** Intake Mode  
**Persona:** Curator  

Intake produces the **tranche preamble**, the root artefact defining:

- mission  
- scope  
- boundaries  
- governance posture  
- acceptance criteria  
- identity propagation rules  

## 2.0.1 Inputs  
- human intent  
- tranche identifier  
- governance constraints  

## 2.0.2 Activities  
- generate the tranche preamble  
- clarify intent when requested  
- refine the preamble if ambiguities are surfaced  

## 2.0.3 Outputs  
- tranche preamble (governed artefact)

---

# 2.1 Phase 1 — Bootstrap  
**Conversation:** Bootstrap Conversation  
**Mode:** Intake Mode (Bootstrap Stage)   
**Persona:** Curator  

Bootstrap prepares the deterministic workspace for the tranche.

## 2.1.1 Inputs  
- tranche preamble  
- governance posture  
- identity propagation rules  

## 2.1.2 Activities  
The Curator MUST:

- validate the preamble  
- create the tranche folder structure  
- create the documentation envelope  
- create the DECOR envelope  
- create the Ticket Map skeleton  
- initialise tranche logs  
- register the tranche  

## 2.1.3 Outputs  
- tranche folder structure  
- documentation envelope  
- DECOR envelope  
- Ticket Map skeleton  
- bootstrap log  

---

# 2.2 Phase 2 — Orchestration  
**Conversation:** Orchestrator Conversation  
**Mode:** Orchestration Mode  
**Personas:** Conductor (Conceptual), Orchestrator (Practical), Architect  

Orchestration formalises DECOR, generates the Ticket Map, and governs lifecycle transitions.

## 2.2.1 Inputs  
- tranche preamble  
- bootstrap artefacts  
- governance posture  
- identity propagation rules  
- prior DECOR (if applicable)  

## 2.2.2 Activities

### A. Preamble Interpretation (Conductor)  
Interpret tranche intent, scope, boundaries, and risks.

### B. DECOR Derivation (Architect)  
Architect derives **DECOR**, including:

- Design  
- Extensions  
- Considerations  
- Opportunities  
- Risks  
- DECOR metadata  
- invariants  
- constraints  
- governance envelopes  

### C. Ticket Map Creation (Orchestrator)  
The Orchestrator produces the Ticket Map:

- grounded in DECOR  
- sequenced deterministically  
- persona‑routed  
- metadata‑propagated  
- aligned with Method A or Method B  

### D. Conceptual Fill Phase (Architect)  
The Architect MUST:

- populate all `content-required` surfaces  
- complete all `requires-fill` tickets  
- produce conceptual artefacts  
- update DECOR if contradictions appear  

### E. Orchestration Validation (Conductor)  
The Conductor validates:

- conceptual completeness  
- metadata propagation  
- persona routing  
- DECOR correctness
- naming correctness
- namespace correctness
- identity propagation correctness  

## 2.2.3 Outputs  
- DECOR  
- conceptual artefacts  
- Ticket Map  
- orchestration log  

---

# 2.3 Phase 3 — Implementation  
**Conversations:**  
- Orchestrator Conversation (Practical)  
- Implementer Conversations (one per ticket)  

**Persona:** Implementer  

Implementation executes tickets deterministically and in isolation.

## 2.3.1 Inputs  
- DECOR  
- conceptual artefacts  
- Ticket Map  
- ticket bundle  
- metadata  
- clarifications  

## 2.3.2 Activities

### A. Ticket Dispatch (Orchestrator)  
Dispatch ticket with:

- DECOR subset  
- metadata  
- persona routing  
- documentation requirements  
- acceptance criteria  

### B. Ticket Execution (Implementer)  
Implementer MUST:

- implement code  
- generate tests  
- produce implementation logs  
- produce replay traces  
- produce documentation  
- follow DECOR invariants  
- follow metadata  
- surface contradictions  

### C. Implementer Isolation  
- one ticket per conversation  
- no shared implicit memory  
- deterministic artefact handoff  

### D. Governance Validation (Orchestrator)  
Validate:

- DECOR compliance  
- metadata compliance  
- governance envelope compliance  
- structural consistency
- naming correctness
- namespace correctness
- identity propagation correctness

### E. DECOR Updates (Architect)  
Architect formalises updates when contradictions appear.

### F. Ticket Map Evolution (Orchestrator)  
Update sequencing, dependencies, metadata.

## 2.3.3 Outputs  
- implementation logs  
- replay traces  
- documentation  
- surfaced contradictions  
- DECOR updates  
- updated Ticket Map  

---

# 2.4 Phase 4 — Verification  
**Conversation:** Verifier Conversation  
**Mode:** Verification Mode  
**Personas:** Auditor → Verifier  

Verification validates the tranche and produces the final governed artefacts.

## 2.4.1 Inputs  
- DECOR  
- DECOR updates  
- conceptual artefacts  
- implementation logs  
- replay traces  
- documentation  
- ticket bundle  
- governance envelopes  
- metadata  

## 2.4.2 Activities

### A. Drift Classification (Auditor)  
Classify:

- governance drift  
- invariant drift  
- architectural drift  
- implementation drift  
- documentation drift  
- determinism drift  
- metadata drift
- naming metadata
- namespace metadata
- identity propagation metadata  

### B. Structural Reconciliation (Architect)  
Architect resolves structural contradictions and updates DECOR.

### C. Epilogue Ticketing (Orchestrator → Implementer)  
Correct drift via epilogue tickets.

### D. Final Validation (Verifier)  
Verifier validates:

- drift corrections  
- reconciled DECOR  
- reconciled documentation  
- reconciled tests  
- determinism  
- persona boundary compliance  
- governance compliance  

## 2.4.3 Outputs  
- drift report  
- epilogue tickets  
- reconciled artefacts  
- Reconciled DECOR  
- verification report  

---

# 2.5 Phase 5 — Closure  
**Conversation:** Closure Conversation  
**Personas:** Conductor (Conceptual), Curator  

Closure finalises the tranche.

## 2.5.1 Inputs  
- verification report  
- Reconciled DECOR  
- reconciled documentation  
- reconciled tests  
- governance envelopes  

## 2.5.2 Activities  
- Conductor validates conceptual alignment  
- Curator validates governance alignment  
- Curator approves tranche closure  

## 2.5.3 Outputs  
- tranche closure approval  
- archived tranche artefacts  

---

# 3. Method A vs Method B (v2.4)

## Method A — Product‑First  
- Curator defines product intent  
- Architect derives DECOR from product intent  
- Ticket Map is product‑first  
- DECOR reflects product structure  

## Method B — Technical‑First  
- Implementer surfaces technical truths  
- Architect derives DECOR from technical evidence  
- Ticket Map is architecture‑first  
- DECOR reflects system reality  

Both converge at reconciliation.

---

# 4. Lifecycle Invariants (v2.4)

These MUST always hold:

- DECOR is the single semantic anchor  
- DECOR may only be formalised by the Architect  
- DECOR may only be modified in Orchestration Mode  
- Implementer conversations are isolated  
- Orchestrator enforces metadata  
- Fill Phase MUST complete before implementation  
- Auditor classifies drift  
- Verifier validates corrections  
- Reconciled DECOR is the final baseline  
- Curator approves closure  
- All artefacts must be preserved for audit  
