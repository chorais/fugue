# **preamble.md (v2.4)**  
**Tranche Preamble — Tranche `<tranche-name>`**  
Version: 2.4  
Persona: Curator  
Mode: Intake Mode  
Lifecycle Phase: Phase 0 — Intake  
Authority: Governance‑Level (Non‑Technical)  

---

# 0. Metadata

```yaml
metadata:
  tranche-name: "<tranche-name>"
  curator: "<identity>"
  intent-type: "Product|Governance|Technical|Hybrid"

  governance-posture: "<summary>"
  identity-propagation-rules: "<summary>"
  acceptance-criteria-governance: "<summary>"

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  governance-envelope: "<id>"
  evaluator-categories: []
  evaluator-diagnostics: []

  persona-routing-summary: "Curator"

  lifecycle-phase: "intake"
  lifecycle-context: "phase-0"

  status: "Draft|Active"
  last-updated: "<YYYY-MM-DD>"

  # Namespace reference (updated)
  namespace:
    preamble-path: "/fugue_docs/specs/<tranche-name>/preamble.md"
```

---

# 1. Mission  
Define the **governance‑level mission** of the tranche.

The mission MUST:

- define the purpose of the tranche  
- define the governance intent  
- define the expected outcome  
- define the non‑negotiable constraints  
- align with naming/namespace/identity propagation posture  
- align with governance envelopes  

The mission MUST NOT:

- include implementation detail  
- include architectural decisions  
- include ticket‑level requirements  
- include DECOR content  
- contradict DECOR schema  

---

# 2. Scope & Boundaries  

## 2.1 In Scope  
List governance‑level surfaces included in the tranche.

## 2.2 Out of Scope  
List surfaces explicitly excluded from the tranche.

## 2.3 Constraints  
List governance constraints that MUST be respected, including:

- naming/namespace constraints  
- identity propagation constraints  
- documentation envelope constraints  
- governance envelope constraints  

---

# 3. Governance Posture  
Define the governance posture for the tranche.

Governance posture MUST include:

- governance expectations  
- risk posture  
- compliance requirements  
- persona boundaries  
- documentation expectations  
- metadata expectations  
- naming/namespace/identity propagation expectations  
- evaluator metadata expectations  

Governance posture MUST NOT include:

- DECOR invariants  
- architectural constraints  
- implementation constraints  

---

# 4. Identity Propagation Rules  
Define naming and identity lineage rules for:

- tranche artefacts  
- documentation  
- DECOR  
- tickets  
- logs  
- diagrams  
- namespaces  
- evaluator metadata  
- replay traces  

Identity rules MUST be:

- deterministic  
- stable  
- unambiguous  
- governance‑aligned  
- aligned with the Identity Propagation Contract (v2.4)  

---

# 5. Acceptance Criteria (Governance‑Level)  
Define the governance‑level acceptance criteria for tranche closure.

Acceptance criteria MUST include:

- governance alignment  
- documentation completeness  
- DECOR correctness  
- persona boundary compliance  
- metadata correctness  
- naming/namespace/identity propagation correctness  
- evaluator metadata correctness  
- lifecycle correctness  
- governance envelope compliance  

Acceptance criteria MUST NOT include:

- implementation‑level acceptance criteria  
- test‑level acceptance criteria  

---

# 6. Risks & Assumptions  

## 6.1 Risks  
List governance‑level risks, including:

- naming/namespace risks  
- identity propagation risks  
- documentation envelope risks  
- governance envelope risks  
- evaluator metadata risks  

## 6.2 Assumptions  
List assumptions regarding:

- system state  
- architectural context  
- product context  
- governance context  
- naming/namespace/identity propagation posture  

---

# 7. Clarifications (Optional)  
Record any clarifications provided by the Curator during Intake.

Clarifications MUST NOT:

- contain implementation detail  
- contain architectural decisions  
- modify the template structure  
- contradict governance envelopes  
- contradict naming/namespace/identity propagation rules  

---

# 8. Outputs  
The preamble MUST produce:

- tranche mission  
- governance posture  
- identity propagation rules  
- governance‑level acceptance criteria  
- scope and boundaries  
- risks and assumptions  
- naming/namespace/identity propagation posture  
- evaluator metadata posture  

These outputs MUST be stored under:

```
/fugue_docs/specs/<tranche-name>/preamble.md
```

---

# 9. Handoff to Initiator  
The Curator MUST hand off the following to the Initiator:

- tranche preamble  
- governance posture  
- identity propagation rules  
- naming/namespace posture  
- evaluator metadata posture  
- tranche identifier  

This begins **Phase 1 — Bootstrap**.
