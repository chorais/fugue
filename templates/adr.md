# 🎼 **adr.md (v2.4)**  
**Architectural Decision Record — ADR‑<number>**  
Version: 2.4  
Persona: Architect  
Mode: Orchestration Mode  
Lifecycle Context: Cross‑Phase (Developer‑Facing)  
Authority: Non‑Normative (DECOR is authoritative)  

---

# 0. Metadata

```yaml
metadata:
  adr-id: "ADR-<number>"
  tranche: "<tranche>"
  architect: "<author-identity>"
  status: "Proposed|Accepted|Superseded|Deprecated"
  supersedes: "<ADR-id|null>"
  superseded-by: "<ADR-id|null>"
  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"
  governance-envelope: "<id>"
  evaluator-categories: []
  evaluator-diagnostics: []
  persona-routing-summary: "Architect"
  lifecycle-context: "cross-phase"
  last-updated: "<YYYY-MM-DD>"
```

---

# 1. Context  
Define the architectural context in which the decision is made.

Context MUST:

- describe the architectural environment  
- describe the relevant surfaces  
- describe the motivating conditions  
- describe naming/namespace/identity propagation context  
- reference relevant DECOR surfaces  

Context MUST NOT:

- introduce requirements  
- introduce invariants  
- introduce constraints  
- contradict DECOR  
- contradict naming/namespace/identity propagation rules  
- contradict governance envelopes  

---

# 2. Problem Statement  
Define the architectural problem being addressed.

The problem statement MUST:

- describe the issue  
- describe the architectural gap  
- describe the affected surfaces  
- describe any naming/namespace/identity propagation implications  

The problem statement MUST NOT:

- include implementation detail  
- include governance commentary  
- include persona‑specific instructions  
- contradict DECOR  

---

# 3. Decision  
Define the architectural decision taken.

The decision MUST:

- describe the chosen direction  
- describe the architectural posture  
- describe the intended structural outcome  
- align with DECOR schema  
- align with naming/namespace/identity propagation rules  
- align with governance envelopes  
- align with determinism envelopes  
- align with evaluator metadata constraints  

The decision MUST NOT:

- introduce new invariants  
- introduce new constraints  
- contradict DECOR  
- contradict governance posture  
- contradict naming/namespace/identity propagation rules  

---

# 4. Rationale  
Define the reasoning behind the decision.

Rationale MUST:

- describe architectural trade‑offs  
- describe structural considerations  
- describe determinism considerations  
- describe naming/namespace/identity propagation considerations  
- describe long‑term implications  
- describe evaluator metadata implications  

Rationale MUST NOT:

- introduce normative requirements  
- introduce governance reasoning  
- include implementation detail  

---

# 5. Consequences  
Define the consequences of the decision.

Consequences MUST include:

- positive consequences  
- negative consequences  
- architectural impacts  
- developer impacts  
- naming/namespace/identity propagation impacts  
- determinism impacts  
- evaluator metadata impacts  

Consequences MUST NOT:

- introduce requirements  
- introduce constraints  
- contradict DECOR  

---

# 6. Alternatives Considered  
Define alternative architectural options.

Alternatives MUST:

- describe each alternative  
- describe why it was not chosen  
- describe architectural trade‑offs  
- describe naming/namespace/identity propagation implications  

Alternatives MUST NOT:

- introduce normative requirements  
- contradict DECOR  

---

# 7. Related Artefacts  
List related governed artefacts.

This section MUST include:

- DECOR references  
- ticket references  
- concern references  
- specification references  
- naming/namespace/identity propagation references  
- evaluator metadata references  

This section MUST NOT:

- modify referenced artefacts  
- reinterpret referenced artefacts  

---

# 8. Notes (Optional)  
Record any additional architectural notes.

Notes MUST NOT:

- modify the decision  
- modify rationale  
- modify consequences  
- introduce normative content  

---

# 9. Lifecycle Integration  
Record lifecycle‑level integration.

This section MUST include:

- tranche association  
- orchestration impact  
- implementation impact  
- verification impact  
- closure impact  
- naming/namespace/identity propagation lifecycle impact  
- evaluator metadata lifecycle impact  

This section MUST NOT:

- introduce requirements  
- introduce constraints  

---
