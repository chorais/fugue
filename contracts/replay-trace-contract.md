# **replay-trace-contract.md (v2.4 — Hierarchy‑Complete)**  
**Replay Trace Contract — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Authority: Governance Contract  
Scope: All Replay Traces, All Personas, All Governance Layers  
Lifecycle: Bootstrap → Implementation → Verification → Reconciliation  

---

# 0. Metadata

```yaml
metadata:
  contract-id: "replay-trace-contract"
  version: "2.4"
  authoritative: true

  applies-to:
    - all-replay-traces
    - all-project-replay-traces
    - all-branch-replay-traces
    - all-theme-replay-traces
    - all-tranche-replay-traces
    - all-implementation-logs
    - all-evaluator-invocations
    - all-determinism-surfaces
    - all-verification-artefacts
    - all-reconciliation-artefacts

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  governance-envelope: "<id>"
  determinism-envelope: "<id>"
  documentation-envelope: "<id>"
  identity-propagation-contract: "<id>"
  namespace-scheme-contract: "<id>"
  lifecycle-contract: "<id>"
  evaluator-contract: "<id>"
```
# Placeholder Semantics
# Fields containing "<id>" or "<self>" are canonical placeholders.
# They MUST be concretised in project/branch/theme/tranche governance envelopes.
# They MUST NOT be replaced in methodology-level contracts.
# The Auditor Persona MUST treat these placeholders as intentional and NOT as metadata drift.

---

# 1. Purpose

The Replay Trace Contract defines the **structure, determinism rules, ordering rules, metadata rules, identity rules, evaluator rules, and lifecycle rules** for replay traces across the full Fugue hierarchy:

> **Project → Branch → Theme → Tranche → Ticket**

Replay traces ensure:

- deterministic reproduction of implementation  
- deterministic reproduction of bootstrap steps  
- deterministic evaluator behaviour  
- deterministic metadata propagation  
- deterministic identity propagation  
- deterministic state transitions  
- deterministic ordering  
- deterministic reconciliation  

Replay traces are the **ground truth** for:

- determinism validation  
- drift classification  
- reconciliation  
- final DECOR validation  
- closure readiness  
- bootstrap correctness  

Replay traces MUST NOT:

- vary between runs  
- depend on conversational context  
- depend on implicit memory  
- depend on non‑governed state  

---

# 2. Replay Trace Principles

Replay traces MUST be:

- deterministic  
- reproducible  
- complete  
- identity‑aligned  
- metadata‑aligned  
- namespace‑aligned  
- evaluator‑aligned  
- governance‑aligned  
- lifecycle‑aligned  
- hierarchy‑aligned  

Replay traces MUST NOT:

- omit steps  
- reorder steps  
- regenerate metadata  
- regenerate identity  
- infer missing information  

Replay traces MUST be reconstructable from:

- implementation logs  
- evaluator metadata  
- evaluator diagnostics  
- DECOR (all layers)  
- Ticket Maps (all layers)  
- documentation  
- bootstrap logs  
- tranche logs  

---

# 3. Replay Trace Structure (v2.4 — Hierarchy‑Complete)

A replay trace MUST include:

1. **Trace Metadata**  
2. **Hierarchy Metadata**  
3. **Identity Lineage**  
4. **Namespace Lineage**  
5. **Evaluator Metadata**  
6. **Evaluator Diagnostics**  
7. **Implementation Steps**  
8. **Bootstrap Steps (if applicable)**  
9. **State Transitions**  
10. **Deterministic Ordering**  
11. **Deterministic Metadata Propagation**  
12. **Deterministic Identity Propagation**  
13. **Deterministic Evaluator Behaviour**  
14. **Deterministic Replay Outcome**  

Replay traces MUST follow the canonical structure:

```
/fugue_docs/replay/<hierarchy-level>/<entity-name>/<ticket-id>-replay-trace.json
```

Where `<hierarchy-level>` ∈:

- project  
- branch  
- theme  
- tranche  

---

# 4. Replay Trace Metadata Rules

Replay trace metadata MUST include:

```yaml
trace:
  hierarchy-level: "<project|branch|theme|tranche>"
  entity: "<project-name|branch-name|theme-name|tranche-name>"
  ticket: "<ticket-id>"
  implementer: "<persona-id>"
  evaluator: "<persona-id>"
  version: "v2.4"
  determinism-level: "strict"
  ordering: "deterministic"
  namespace: "<namespace>"
  identity:
    initiator: "<persona-id>"
    owner: "<persona-id>"
    effective-execution: "<persona-id>"
```

Metadata MUST be:

- complete  
- deterministic  
- identity‑aligned  
- namespace‑aligned  
- governance‑aligned  

Metadata MUST NOT:

- be omitted  
- be mutated implicitly  
- be inferred  

---

# 5. Replay Trace Ordering Rules

Replay traces MUST follow deterministic ordering across:

- project bootstrap steps  
- branch bootstrap steps  
- theme bootstrap steps  
- tranche bootstrap steps  
- implementation steps  
- evaluator invocations  
- metadata propagation  
- identity propagation  
- state transitions  

Ordering MUST NOT:

- depend on persona interpretation  
- depend on conversational flow  
- depend on runtime randomness  

Ordering MUST be validated by:

- Auditor  
- Verifier  

---

# 6. Replay Trace Identity Rules

Replay traces MUST include:

- implementer identity  
- evaluator identity  
- identity lineage  

Identity MUST:

- propagate deterministically  
- preserve lineage  
- be included in every step  
- be included in every evaluator invocation  

Identity MUST NOT:

- drift  
- be regenerated  
- be inferred  

Identity MUST follow the Identity Propagation Contract.

---

# 7. Replay Trace Namespace Rules

Replay traces MUST:

- follow the Namespace Scheme Contract  
- include namespace metadata  
- preserve namespace lineage  

Replay traces MUST NOT:

- be stored outside `/fugue_docs/replay/`  
- embed governed artefacts inside other artefacts  

---

# 8. Replay Trace Evaluator Rules

Replay traces MUST include:

- evaluator identity  
- evaluator category  
- evaluator metadata  
- evaluator diagnostics  
- evaluator determinism metadata  
- evaluator identity lineage  
- evaluator namespace lineage  

Evaluator behaviour MUST be:

- deterministic  
- reproducible  
- metadata‑aligned  
- identity‑aligned  
- namespace‑aligned  

Evaluator behaviour MUST NOT:

- vary between runs  
- depend on conversational context  
- depend on implicit memory  

Evaluator behaviour MUST follow the Evaluator Contract.

---

# 9. Replay Trace State Transition Rules

Replay traces MUST include:

- explicit state transitions  
- deterministic state transitions  
- metadata‑preserving transitions  
- identity‑preserving transitions  

State transitions MUST NOT:

- be inferred  
- be omitted  
- be mutated implicitly  

State transitions MUST follow:

- Determinism Envelope  
- Lifecycle Contract  

---

# 10. Replay Trace Determinism Rules

Replay traces MUST:

- reflect deterministic ordering  
- reflect deterministic evaluator behaviour  
- reflect deterministic metadata propagation  
- reflect deterministic identity propagation  
- reflect deterministic state transitions  

Replay traces MUST NOT:

- contain non‑deterministic values  
- depend on conversational context  
- depend on runtime randomness  

Replay traces MUST follow the Determinism Envelope.

---

# 11. Replay Trace Drift Classification

Replay trace drift MUST be classified as:

### **Critical**
- non‑deterministic ordering  
- missing evaluator behaviour  
- missing identity lineage  
- missing metadata lineage  
- corrupted namespace lineage  
- corrupted state transitions  
- missing bootstrap steps (project/branch/theme/tranche)  

### **Major**
- incomplete evaluator diagnostics  
- incomplete metadata  
- inconsistent ordering  

### **Minor**
- formatting issues  
- non‑blocking metadata issues  

All drift MUST be recorded in:

- auditor notes  
- reconciliation log  
- reconciled DECOR  

---

# 12. Replay Trace Validation Rules

Replay traces MUST be validated by:

## 12.1 Auditor  
- determinism  
- ordering  
- evaluator behaviour  
- metadata propagation  
- identity propagation  
- namespace correctness  
- state transitions  
- bootstrap correctness (if applicable)  

## 12.2 Verifier  
- reconciliation completeness  
- governance alignment  
- lifecycle alignment  
- DECOR alignment  
- metadata lineage  
- identity lineage  
- namespace lineage  
- hierarchy correctness  

---

# 13. Replay Trace Integration with Reconciliation

Replay traces MUST be included in:

- reconciliation logs  
- reconciled DECOR  
- verification reports  
- closure artefacts  
- bootstrap validation (project/branch/theme)  

Replay traces MUST NOT:

- be modified after reconciliation  
- be regenerated after reconciliation  

Replay traces are **immutable** once validated.

---