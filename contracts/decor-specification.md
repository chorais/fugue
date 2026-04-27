# **DECOR Specification (v2.4 — Hierarchy‑Complete)**  
Version: 2.4  
Status: Active  
Methodology: Fugue Orchestration Method v2.4  
Governance Authority: Curator  

---
# 0. Metadata

```yaml
metadata:
  contract-id: "decor-specification"
  version: "2.4"
  authoritative: true

  applies-to:
    - decor
    - decor-derivation
    - decor-updates
    - reconciled-decor
    - governance-envelopes
    - persona-routing
    - identity-propagation
    - naming-and-namespace-alignment
    - tranche-lifecycle-governance

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  governance-envelope: "<id>"
  documentation-envelope: "<id>"
  determinism-envelope: "<id>"
  reconciled-decor-contract: "<id>"
  ticket-map-contract: "<id>"
  lifecycle-contract: "<id>"
  replay-trace-contract: "<id>"
```

# Placeholder Semantics
# Fields containing "<id>" or "<self>" are canonical placeholders.
# They MUST be concretised in project/branch/theme/tranche governance envelopes.
# They MUST NOT be replaced in methodology-level contracts.
# The Auditor Persona MUST treat these placeholders as intentional and NOT as metadata drift.

---

# 1. Purpose  

This contract defines **DECOR** — the Declarative Contract of Record — the structural, architectural, governance, and requirements‑consideration foundation for **every governance layer** in the Fugue Method:

> **Project → Branch → Theme → Tranche**

DECOR is the **single semantic anchor** across all personas, conversations, and substrates.  
It ensures deterministic execution, stable reasoning, and auditable governance.

DECOR governs:

- persona routing  
- metadata‑driven lifecycle transitions  
- Architect Fill Phase scope  
- Ticket Map metadata  
- documentation routing  
- reconciliation drift classification  
- identity propagation  
- naming and namespace alignment  
- governance inheritance across layers  

---

# 2. What DECOR Is  

DECOR stands for:

- **D — Design**  
- **E — Extensions**  
- **C — Considerations**  
- **O — Opportunities**  
- **R — Risks**

DECOR is **not** a design document.  
It is a **structural + governance + constraint + risk + requirements‑consideration artefact**.

DECOR is the **source of truth** for:

- invariants  
- governance envelopes  
- architectural constraints  
- identity propagation rules  
- structural risks  
- feasibility boundaries  
- metadata‑driven persona routing  
- Ticket Map metadata  
- documentation requirements  
- naming and namespace constraints  
- hierarchy‑level inheritance  

---

# 3. DECOR Across the Hierarchy (v2.4)

DECOR now exists at **four governance layers**, each with its own scope and inheritance rules.

## 3.1 Project DECOR  
Defines:

- global invariants  
- global architectural constraints  
- global governance envelopes  
- global naming + namespace roots  
- global identity propagation rules  
- global documentation envelopes  
- global risks and considerations  

Project DECOR is the **root architectural and governance substrate**.

All lower layers MUST inherit from it.

---

## 3.2 Branch DECOR  
Defines:

- branch‑specific invariants  
- branch‑specific architectural constraints  
- branch‑specific governance envelopes  
- branch‑specific naming + namespace rules  
- branch‑specific identity propagation rules  
- branch‑specific risks and considerations  

Branch DECOR MUST:

- inherit from Project DECOR  
- refine but NOT contradict Project DECOR  

---

## 3.3 Theme DECOR  
Defines:

- theme‑specific invariants  
- theme‑specific architectural constraints  
- theme‑specific governance envelopes  
- theme‑specific naming + namespace rules  
- theme‑specific identity propagation rules  
- theme‑specific risks and considerations  

Theme DECOR MUST:

- inherit from Branch DECOR  
- refine but NOT contradict Branch or Project DECOR  

---

## 3.4 Tranche DECOR  
Defines:

- tranche‑specific invariants  
- tranche‑specific architectural constraints  
- tranche‑specific governance envelopes  
- tranche‑specific naming + namespace rules  
- tranche‑specific identity propagation rules  
- tranche‑specific risks and considerations  

Tranche DECOR MUST:

- inherit from Theme DECOR  
- refine but NOT contradict Theme, Branch, or Project DECOR  

---

# 4. DECOR as Cross‑Substrate Semantic Protocol  

DECOR is the **cross‑substrate semantic protocol** that preserves meaning across:

- orchestration reasoning  
- implementation execution  
- verification and reconciliation  
- multiple AI substrates  
- multiple conversations  
- multiple personas  
- multiple governance layers  

All governed artefacts MUST be semantically aligned to DECOR.

DECOR ensures that:

- Implementer ingress analysis  
- Architect formalisation  
- Conductor governance  
- Auditor reconciliation  

all use the **same structured schema**, regardless of layer.

---

# 5. DECOR as Persona‑Agnostic Reasoning Schema  

DECOR defines the **thinking boundaries** for all personas:

- **Architect** derives and updates DECOR  
- **Conductor** interprets and enforces DECOR  
- **Implementer** complies with DECOR  
- **Auditor** compares implementation to DECOR  
- **Sponsor** provides upstream intent but does not interact with DECOR directly  

Persona routing is derived from DECOR metadata and enforced by the Conductor.

---

# 6. DECOR Structure  

DECOR MUST include the following sections at **every governance layer**.

## 6.1 Design  
Structural and architectural intent extracted from:

- preamble (project / branch / theme / tranche)  
- Implementer ingress analysis (tranche only)  
- product and governance context  

Includes:

- system shape  
- architectural direction  
- structural patterns  
- identity propagation model  
- evaluator semantics  
- orchestration implications  
- runtime invariants  

---

## 6.2 Extensions  
Forward‑looking or optional evolutions:

- extension points  
- future capabilities  
- optional refactors  
- potential abstractions  
- scalability considerations  

Extensions MUST NOT be implemented unless explicitly ticketed.

---

## 6.3 Considerations  
The governance and invariants core.

Includes:

- invariants  
- architectural constraints  
- governance envelopes  
- identity propagation rules  
- dependency constraints  
- sequencing constraints  
- trade‑offs  
- assumptions  

Considerations define the **thinking boundaries** for all personas.

---

## 6.4 Opportunities  
Optional improvements or optimisations:

- performance opportunities  
- simplification opportunities  
- consolidation opportunities  
- developer‑experience opportunities  
- test harness opportunities  

Opportunities are **not commitments**.

---

## 6.5 Risks  
Explicit risks including:

- architectural risks  
- governance risks  
- feasibility risks  
- ambiguity risks  
- dependency risks  
- identity propagation risks  
- drift surfaces  

---

## 6.6 Open Questions  
Unresolved issues requiring clarification from the Conductor.

---

# 7. DECOR Surface Metadata (v2.4)  

Each DECOR surface MAY declare the following metadata:

- `content-required: true|false`  
- `implementation-required: true|false`  
- `architect-required: true|false`  

Metadata governs:

- Ticket Map persona routing  
- Architect Fill Phase scope  
- documentation routing  
- Auditor enforcement  
- Conductor lifecycle transitions  

Metadata MUST be included in DECOR and preserved in all updates.

---

# 8. DECOR and Persona Reasoning Boundaries  

## 8.1 Architect Persona — DECOR Derivation and Updates  

The Architect is the **only persona** allowed to derive and update:

- Design  
- Extensions  
- Considerations  
- Opportunities  
- Risks  

The Architect produces:

- DECOR  
- DECOR updates  
- conceptual artefacts for `content-required` surfaces  

## 8.2 Sponsor Persona — Upstream Intent Only  

The Sponsor may define:

- mission  
- boundaries  
- acceptance criteria  
- governance posture  

The Sponsor may **not** derive, modify, or interpret DECOR.

## 8.3 Conductor Persona — DECOR Interpretation Only  

The Conductor may:

- interpret DECOR  
- enforce DECOR  
- route DECOR  
- refine tickets based on DECOR  
- reconcile product intent with DECOR  

The Conductor may **not** modify DECOR.

## 8.4 Implementer Persona — DECOR Compliance Only  

The Implementer may:

- read DECOR  
- follow invariants  
- surface contradictions  
- surface feasibility issues  

The Implementer may **not** derive or modify DECOR.

## 8.5 Auditor Persona — DECOR Comparison Only  

The Auditor may:

- read DECOR  
- classify drift  
- surface contradictions  

The Auditor may **not** modify DECOR.

## 8.6 Implementer Ingress Analysis  

Ingress analysis is **non‑canonical evidence**.

It may inform DECOR but MUST NOT produce or modify DECOR.

---

# 9. DECOR Lifecycle Across Conversations  

## 9.1 Project Bootstrap  
Architect derives Project DECOR from:

- project preamble  
- governance posture  
- naming + namespace roots  
- identity propagation rules  

## 9.2 Branch Bootstrap  
Architect derives Branch DECOR from:

- branch preamble  
- Project DECOR inheritance  
- branch‑specific constraints  

## 9.3 Theme Bootstrap  
Architect derives Theme DECOR from:

- theme preamble  
- Branch DECOR inheritance  
- theme‑specific constraints  

## 9.4 Tranche Bootstrap  
Architect derives Tranche DECOR from:

- tranche preamble  
- Theme DECOR inheritance  
- ingress analysis (optional)  

## 9.4.1 Intake (Sponsor Preamble)  

- Sponsor defines mission, boundaries, acceptance criteria  
- Provides upstream intent for DECOR derivation  

## 9.4.2  Implementer Ingress Analysis (Non‑Canonical)  

- Extracts invariants and constraints from code  
- Identifies risks and opportunities  
- Informs Architect formalisation  

## 9.4.3  Architect Formalisation (Canonical DECOR)  

- Architect produces DECOR in the Conductor Conversation  
- Conductor aligns DECOR with product intent  
- DECOR becomes the architectural ledger for the tranche  

## 9.5 DECOR Updates  

- Triggered by contradictions or new evidence  
- Architect formalises updates  
- Stored as governed artefacts  
- Metadata and identity MUST be preserved  

## 9.6 Architect Fill Phase  

- Architect populates all `content-required` surfaces  
- Ensures conceptual completeness  
- Produces updated DECOR and conceptual artefacts  
- Conductor validates completeness before ticket generation or evolution  

## 9.7 Reconciled DECOR  

- Auditor validates DECOR alignment  
- Architect resolves inconsistencies  
- Auditor produces final Reconciled DECOR  

---

# 10. Method A vs Method B DECOR Timing  

## Method A — Product Grounding  

- DECOR is product‑first  
- Implementer ingress analysis optional  
- Architect leads DECOR creation  
- DECOR reflects product intent  
- Architect Fill Phase focuses on product‑level conceptual surfaces  

## Method B — Technical Grounding  

- DECOR is architecture‑first  
- Implementer ingress analysis mandatory  
- Architect formalises DECOR from technical evidence  
- DECOR reflects system reality  
- Architect Fill Phase focuses on system‑level conceptual surfaces  

Both methods converge at Reconciliation.

---

# 11. DECOR in Reconciliation  

Reconciliation compares:

- DECOR  
- DECOR updates  
- conceptual artefacts  
- implementation logs  
- replay traces  
- ticket bundle  
- clarifications  
- governance envelopes  

The Auditor identifies drift.  
The Conductor issues epilogue tickets.  
The Implementer corrects drift.  
The Architect clarifies DECOR if needed.

## 11.1 DECOR as Reconciliation Baseline  

DECOR is the baseline for drift classification.

Drift categories include:

- structural drift  
- conceptual drift  
- metadata drift  
- implementation drift  
- documentation drift  
- architecture drift  
- governance drift  

---

# 12. DECOR Evolution Rules  

- Project DECOR evolves rarely  
- Branch DECOR evolves only when branch‑level invariants change  
- Theme DECOR evolves when thematic constraints change  
- Tranche DECOR evolves within the tranche via governed updates  
- DECOR may evolve across tranches  
- DECOR may evolve within a tranche only through governed updates  
- DECOR updates MUST be formalised by the Architect persona  
- DECOR updates MUST be stored as governed artefacts  

All DECOR evolution MUST:

- preserve metadata  
- preserve identity lineage  
- preserve naming + namespace alignment  
- preserve governance envelopes  
- preserve inheritance rules
- preserve conceptual artefacts from the Fill Phase

---

# 13. DECOR Folder Structure  


Each project MUST maintain:
```text
/fugue_docs/project/
    project-decor.md
```

Each branch MUST maintain:
```text
/fugue_docs/branches/<branch-name>/
    branch-decor.md
```

Each theme MUST maintain:
```text
/fugue_docs/themes/<theme-name>/
    theme-decor.md
```

Each tranche MUST maintain:
```text
/fugue_docs/decors/<tranche-name>/
    preamble-interpretation.md
    decor.md
    decor-updates/
    conceptual-artefacts/
    reconciled-decor.md

```

DECOR artefacts MUST NOT be stored outside governed namespaces.

---

# 14. DECOR and Premium‑Efficient Execution  

DECOR prevents:

- re‑derivation of architecture  
- re‑derivation of invariants  
- re‑derivation of governance  
- unnecessary reasoning  
- persona boundary violations  

DECOR ensures:

- deterministic execution  
- predictable ticket generation  
- predictable implementation  
- predictable reconciliation  
- metadata‑driven persona routing  
- metadata‑driven documentation routing  
- naming and namespace consistency  

---
