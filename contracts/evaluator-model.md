# **Evaluator Model Contract (v2.4)**  
Version: 2.4  
Status: Active  
Governance Authority: Curator  
Methodology: Fugue Orchestration Method v2.4  
Scope: Evaluator Governance  
Personas Bound: Architect, Conductor, Auditor  

---

# 1. Purpose  
The Evaluator Model Contract defines the **canonical structure, semantics, metadata, lifecycle, and governance boundaries** for all evaluators in the Fugue Orchestration Method v2.4.

Evaluators are **deterministic, metadata‑driven governance components** that:

- enforce invariants  
- validate structural correctness  
- validate persona routing  
- validate metadata  
- validate naming and namespace correctness  
- validate identity propagation  
- validate DECOR alignment  
- validate implementation artefacts  
- classify evaluator‑level drift  
- support reconciliation  

Evaluators are **not personas**.  
They are **governed execution units** that operate within the orchestration substrate.

This contract ensures:

- deterministic evaluator behaviour  
- cross‑persona consistency  
- cross‑substrate consistency  
- metadata‑aligned execution  
- naming‑aligned execution  
- namespace‑aligned execution  
- identity‑aligned execution  
- replayability  
- auditability  

---

# 2. Evaluator Authority and Boundaries  

## 2.1 Evaluator Authority  
Evaluators MAY:

- read DECOR  
- read metadata  
- read Ticket Map  
- read naming metadata  
- read namespace metadata  
- read identity propagation metadata  
- read implementation artefacts  
- read conceptual artefacts  
- enforce invariants  
- enforce metadata  
- enforce persona routing  
- enforce naming correctness  
- enforce namespace correctness  
- enforce identity propagation  
- enforce evaluator‑specific rules  
- emit evaluator diagnostics  
- block execution when invariants are violated  

Evaluators MAY NOT:

- modify DECOR  
- modify metadata  
- modify naming  
- modify namespaces  
- modify identity propagation  
- modify Ticket Map  
- modify implementation artefacts  
- modify conceptual artefacts  
- generate tickets  
- generate code  
- generate documentation  
- act as personas  

Evaluators are **pure governance logic**, not agents.

## 2.2 Evaluator Non‑Authority  
Evaluators MUST NOT:

- derive DECOR  
- reinterpret DECOR  
- override DECOR  
- perform reconciliation  
- classify tranche‑level drift  
- modify lifecycle transitions  
- modify folder structure  

These responsibilities belong to the Architect, Conductor, and Auditor personas.

---

# 3. Evaluator Categories  
All evaluators MUST belong to one of the following canonical categories:

- **Governance Evaluator** — governance envelopes, invariants, persona boundaries  
- **Security Evaluator** — security posture, access boundaries, sensitive surfaces  
- **Precedence Evaluator** — dependency ordering, sequencing, cross‑tranche precedence  
- **Federation Evaluator** — multi‑persona, multi‑provider, multi‑node semantics  
- **Performance Evaluator** — caching, replay, determinism, performance invariants  
- **Diagnostic Evaluator** — structured diagnostics, error domains, evaluator metadata  

Each evaluator MUST implement the canonical evaluator interface.

---

# 4. Evaluator Canonical Interface  

All evaluators MUST implement:

```
evaluate(input: EvaluatorInput) → EvaluatorResult
```

## 4.1 EvaluatorInput  
Includes:

- DECOR subset  
- Ticket Map subset  
- metadata  
- naming metadata  
- namespace metadata  
- identity propagation metadata  
- persona routing  
- implementation artefacts  
- conceptual artefacts  
- evaluator‑specific context  
- evaluator configuration  

## 4.2 EvaluatorResult  
Includes:

- `status: pass | fail | warn`  
- `diagnostics: EvaluatorDiagnostic[]`  
- `metadata: EvaluatorMetadata`  
- `blocking: boolean`  

Evaluators MUST be deterministic:

```
same input → same output
```

---

# 5. Evaluator Metadata (v2.4)  

Evaluators MUST declare:

- **`blocking: true|false`**  
  Whether evaluator failure halts execution.

- **`scope: governance|security|precedence|federation|performance|diagnostic`**  
  Evaluator category.

- **`lifecycle: bootstrap|fill-phase|ticket-loop|reconciliation`**  
  When the evaluator runs.

- **`persona-impact: architect|conductor|implementer|auditor|none`**  
  Which persona is affected by evaluator output.

- **`naming-impact: true|false`**  
  Whether evaluator enforces naming correctness.

- **`namespace-impact: true|false`**  
  Whether evaluator enforces namespace correctness.

- **`identity-impact: true|false`**  
  Whether evaluator enforces identity propagation.

Evaluator metadata MUST be:

- declared in evaluator definition  
- preserved across updates  
- validated by the Auditor  
- enforced by the Conductor  

---

# 6. Evaluator Lifecycle Integration  

Evaluators run at specific lifecycle stages:

## 6.1 Bootstrap  
Evaluators validate:

- DECOR structure  
- metadata correctness  
- naming correctness  
- namespace correctness  
- identity propagation correctness  
- Ticket Map correctness  
- persona routing correctness  
- governance envelopes  

## 6.2 Architect Fill Phase  
Evaluators validate:

- conceptual completeness  
- metadata propagation  
- DECOR updates  
- naming correctness  
- namespace correctness  
- identity propagation correctness  
- persona routing for conceptual tickets  

## 6.3 Ticket Loop  
Evaluators validate:

- implementation artefacts  
- metadata preservation  
- naming preservation  
- namespace preservation  
- identity propagation preservation  
- DECOR invariants  
- dependency correctness  
- persona routing correctness  

## 6.4 Reconciliation  
Evaluators validate:

- final DECOR alignment  
- metadata correctness  
- naming correctness  
- namespace correctness  
- identity propagation correctness  
- implementation correctness  
- documentation correctness  
- evaluator‑level drift  

Evaluator output feeds into Auditor drift classification.

---

# 7. Evaluator Drift Classification  

Evaluators MUST classify evaluator‑level drift:

## 7.1 Structural Evaluator Drift  
- evaluator logic contradicts DECOR  
- evaluator logic contradicts metadata  
- evaluator logic contradicts naming rules  
- evaluator logic contradicts namespace rules  
- evaluator logic contradicts identity propagation rules  
- evaluator logic contradicts governance envelopes  

## 7.2 Metadata Evaluator Drift  
- evaluator metadata missing  
- evaluator metadata incorrect  
- evaluator metadata not preserved  

## 7.3 Execution Evaluator Drift  
- evaluator produces non‑deterministic output  
- evaluator produces contradictory diagnostics  
- evaluator fails to enforce invariants  

## 7.4 Severity  
- **Critical:** blocking evaluator fails  
- **Major:** evaluator metadata incorrect  
- **Minor:** diagnostic formatting issues  

Evaluator drift MUST be surfaced to the Auditor.

---

# 8. Evaluator Diagnostics  

Evaluator diagnostics MUST include:

- `code` — stable identifier  
- `message` — human‑readable explanation  
- `severity` — info | warn | error  
- `surface` — DECOR | Ticket Map | metadata | naming | namespace | identity | implementation | documentation  
- `persona-impact` — architect | conductor | implementer | auditor  

Diagnostics MUST be:

- deterministic  
- structured  
- metadata‑aligned  
- naming‑aligned  
- namespace‑aligned  
- identity‑aligned  
- preserved for audit  

---

# 9. Evaluator Governance Rules  

Evaluators MUST:

- run deterministically  
- preserve metadata  
- preserve naming  
- preserve namespaces  
- preserve identity propagation  
- enforce DECOR invariants  
- enforce persona routing  
- enforce governance envelopes  
- produce structured diagnostics  
- block execution when required  

Evaluators MUST NOT:

- modify artefacts  
- modify metadata  
- modify naming  
- modify namespaces  
- modify identity propagation  
- modify DECOR  
- modify Ticket Map  
- modify documentation  

Evaluators are **pure governance logic**.

---

# 10. Evaluator Folder Structure  

Evaluator artefacts MUST be stored under:

```
/fugue_docs/specs/evaluators/
    definitions/
    metadata/
    diagnostics/
    logs/
    replay/
```

Evaluator definitions MUST be immutable once published.

Evaluator artefacts MUST NOT be stored outside governed namespaces.
