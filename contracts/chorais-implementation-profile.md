### chorais-implementation-profile.md (v2.4)

**Chorais Implementation Profile — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Authority: Governance Contract  
Scope: Chorais Project (All Branches, Themes, Tranches)  
Lifecycle: Bootstrap → Orchestration → Implementation → Verification → Reconciliation → Closure  

---

## 0. Metadata

```yaml
metadata:
  contract-id: "chorais-implementation-profile"
  version: "2.4"
  authoritative: true

  applies-to:
    - chorais-project
    - chorais-orchestration
    - chorais-personas
    - chorais-governance
    - chorais-replay
    - chorais-ticketing
    - chorais-decor-integration

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  governance-envelope: "<id>"
  documentation-envelope: "<id>"
  determinism-envelope: "<id>"
  decor-contract: "<id>"
  reconciled-decor-contract: "<id>"
  ticket-template-contract: "<id>"
  ticket-map-contract: "<id>"
  replay-trace-contract: "<id>"
  lifecycle-contract: "<id>"
```
# Placeholder Semantics
# Fields containing "<id>" or "<self>" are canonical placeholders.
# They MUST be concretised in project/branch/theme/tranche governance envelopes.
# They MUST NOT be replaced in methodology-level contracts.
# The Auditor Persona MUST treat these placeholders as intentional and NOT as metadata drift.

---

## 1. Purpose

Chorais is the **reference implementation** and first field‑test adopter of the **Fugue Orchestration Method v2.4**.

This profile:

- defines how Chorais **interprets**, **applies**, and **extends** Fugue v2.4  
- binds Chorais to the **Naming Scheme**, **Namespace Scheme**, **Identity Propagation**, **DECOR**, and **Documentation Envelope** contracts  
- constrains Chorais’ orchestration engine, personas, and runtime to **governance‑first, deterministic behaviour**  
- codifies how Chorais handles **mixed‑era artefacts** (v2.3 residue, v2.4 canonical) without weakening governance  

Chorais MUST comply with all v2.4 governance contracts and MAY add stricter local rules, but MUST NOT weaken or contradict Fugue v2.4.

---

## 2. Chorais and the Fugue Method

### 2.1 Role as reference implementation

Chorais is:

- the **reference orchestration engine** for multi‑persona Fugue workflows  
- the **canonical testbed** for applying v2.4 contracts to real projects  
- the **primary environment** for validating replay, determinism, and governance envelopes  

Chorais MUST:

- treat Fugue v2.4 contracts as **normative**  
- surface any divergence as **governance drift**  
- record drift in governed verification artefacts under `/fugue_docs/verification/` and `/fugue_docs/replay/`  

### 2.2 Personas as musical voices

Chorais interprets Fugue personas as **voices in a computational fugue**:

- **Conductor Persona** → orchestration and governance voice  
- **Architect Persona** → structural and DECOR voice  
- **Implementer Persona** → execution and implementation voice  
- **Auditor Persona** → verification and reconciliation voice  
- **Verifier Persona** → final validation voice  

This mapping is conceptual only; all persona rules remain governed by Fugue v2.4 contracts.

---

## 3. Persona Isolation and Orchestration Model

### 3.1 One persona per thread

Chorais enforces:

- **one persona per conversational thread**  
- no persona switching within a thread  
- no implicit cross‑thread memory  

All persona interactions MUST occur via governed artefacts:

- DECOR (all forms)  
- ticket bundles  
- tranche logs  
- replay traces  
- verification and reconciliation artefacts  

### 3.2 Deterministic artefact handoff

Persona communication MUST be mediated by:

- tranche preambles and DECOR under `/fugue_docs/decors/<tranche-name>/`  
- ticket bundles under `/fugue_docs/tickets/<tranche-name>/`  
- logs, replay, verification, and closure artefacts under their governed namespaces  

No persona may rely on:

- implicit conversational context  
- non‑governed memory  
- ad‑hoc artefact placement  

### 3.3 Chorais thread mapping

Chorais maps personas to execution threads:

- **Conductor** → orchestration and ticket‑map reasoning  
- **Architect** → DECOR derivation and updates  
- **Implementer** → implementation and runtime artefacts  
- **Auditor** → drift classification and verification  
- **Verifier** → final reconciliation and closure readiness  

This mapping is **platform‑agnostic** and may be executed by:

- a single AI substrate  
- multiple AI substrates  
- hybrid human/AI actors  

Persona isolation MUST be preserved regardless of substrate.

---

## 4. Identity Propagation in Chorais

Chorais adopts the **Identity Propagation Contract (v2.4)** as normative.

### 4.1 Identity surfaces

All Chorais‑governed artefacts MUST include:

```yaml
identity:
  initiator: "<persona-id>"
  owner: "<persona-id>"
  effective-execution: "<persona-id>"
  lineage:
    - "<identity-event>"
```

Identity MUST:

- propagate deterministically across **Project → Branch → Theme → Tranche → Ticket**  
- be preserved across **Implementation → Replay → Verification → Reconciliation → Closure**  
- be reconstructable from governed artefacts alone  

### 4.2 Chorais‑specific identity rules

Chorais additionally requires:

- **orchestration engine events** (e.g., routing decisions, evaluator invocations) to be recorded in identity lineage where they affect execution  
- **multi‑substrate execution** (e.g., multiple AIs) to record effective execution identity per substrate  

Identity MUST NOT:

- be regenerated by Chorais  
- be inferred from non‑governed logs or conversation history  
- be mutated outside persona boundaries  

---

## 5. Naming and Namespace Alignment

Chorais adopts the **Naming Scheme Contract (v2.4)** and **Namespace Scheme Contract (v2.4)** without modification.

### 5.1 Tranche naming

Chorais tranche names MUST follow:

```text
<branch>.<theme>.<semantic-name>
```

Tranche names MUST NOT:

- use `tranche-` prefixes  
- encode numeric tranche identifiers as primary identity  
- encode persona or implementation detail  

### 5.2 Namespace alignment

All Chorais‑governed artefacts MUST live under `/fugue_docs/` using:

```text
/fugue_docs/<category>/<tranche-name>/
```

Where `<category>` is one of the governed categories defined in the Namespace Scheme Contract (v2.4).

Chorais MUST NOT:

- introduce new governed categories without updating the Namespace Scheme Contract  
- store governed artefacts in `/docs`, `/public-docs`, or persona folders  
- create ad‑hoc tranche folders outside the governed category model  

### 5.3 Mixed‑era artefacts

Chorais MAY host:

- legacy v2.3 artefacts under `/fugue_docs/archive/` or `/fugue/archive/`  
- non‑governed conversation history outside `/fugue_docs/`  

These MUST be treated as:

- **Expected Drift — Legacy** (for v2.3)  
- **Non‑Governed** (for conversation history)  

They MUST NOT:

- influence naming or namespace rules for v2.4 governed artefacts  
- be used as normative references in governance decisions  

---

## 6. DECOR Integration

Chorais adopts the **DECOR Specification (v2.4)** and **Reconciled DECOR Contract (v2.4)** as normative.

### 6.1 DECOR hierarchy

Chorais MUST maintain:

- `/fugue_docs/project/project-decor.md`  
- `/fugue_docs/branches/<branch-name>/branch-decor.md`  
- `/fugue_docs/themes/<theme-name>/theme-decor.md`  
- `/fugue_docs/decors/<tranche-name>/decor.md`  
- `/fugue_docs/decors/<tranche-name>/decor-updates/`  
- `/fugue_docs/decors/<tranche-name>/reconciled-decor.md`  

### 6.2 DECOR template and schema

Chorais MUST:

- use `/fugue/templates/decor.md` as the **canonical DECOR authoring template**  
- validate DECOR against `/schemas/decor-schema.json`  
- preserve all schema‑aligned sections and metadata  

The `metadata.schema` field in DECOR MUST reference:

```yaml
schema: "/schemas/decor-schema.json"
```

### 6.3 DECOR → ticket mapping

Chorais MUST apply the DECOR → ticket mapping defined in the Ticket Template Contract and DECOR Specification:

- **Design** → ticket objectives, scope, determinism requirements  
- **Extensions** → out‑of‑scope or future work (ticketed explicitly)  
- **Considerations** → invariants, constraints, governance envelopes  
- **Opportunities** → optional enhancements (not implemented unless ticketed)  
- **Risks** → diagnostics, test requirements, determinism rules  

Chorais MUST NOT reshape the canonical ticket template to accommodate DECOR; mapping MUST be **one‑way and deterministic**.

---

## 7. Ticket Template Fidelity

Chorais treats the canonical ticket template as a **governance invariant**.

### 7.1 Canonical template

All tickets MUST be generated from:

```text
/fugue/templates/ticket.md
```

Chorais MUST:

- preserve all section headings and ordering  
- include all required sections  
- avoid adding or removing structural sections  
- enforce template fidelity across all personas and tools  

Any deviation is **governance drift** and MUST be classified by the Auditor.

### 7.2 Ticket naming

Chorais MUST follow:

```text
T<number>   (primary tickets)
C<number>   (conceptual tickets)
E<number>   (epilogue tickets)
```

Ticket names MUST NOT:

- embed tranche names  
- embed semantic descriptors  
- encode persona identity  

---

## 8. Documentation Model for Chorais

Chorais adopts the **Documentation Envelope Contract (v2.4)** and the v2.4 namespace model.

### 8.1 Governed documentation

Chorais‑governed documentation MUST live under:

```text
/fugue_docs/
```

including:

- governance artefacts  
- DECORs and reconciled DECORs  
- ticket bundles  
- tranche logs  
- replay traces  
- verification and closure reports  
- architecture artefacts and concerns  

### 8.2 Developer and user documentation

Chorais MUST treat:

- `/docs` as developer‑facing, non‑governed documentation  
- `/public-docs` as user‑facing, non‑governed documentation  

Governance MUST NOT enforce structure in these namespaces, but governed artefacts MAY reference them.

### 8.3 Conversation history

Chorais MAY maintain non‑governed conversation history (e.g., orchestration transcripts) outside `/fugue_docs/`.

These MUST:

- be treated as **non‑canonical evidence**  
- never override DECOR, tickets, or governed documentation  
- never be used as the sole basis for governance decisions  

---

## 9. Chorais Orchestration Engine Extensions

Chorais extends Fugue v2.4 with a multi‑persona orchestration engine, subject to all governance contracts.

### 9.1 Multi‑persona orchestration

Chorais supports:

- multiple AI identities  
- multiple concurrent conversational threads  
- persona‑specific governance envelopes  
- persona‑specific capabilities and tools  

All orchestration flows MUST:

- respect persona isolation  
- record identity and metadata lineage  
- be reconstructable from governed artefacts  

### 9.2 Deterministic replay

Chorais MUST:

- produce replay traces under `/fugue_docs/replay/<tranche-name>/`  
- align replay artefacts with the Replay Trace Contract (v2.4)  
- support deterministic re‑execution of orchestration flows  

Replay MUST NOT depend on:

- implicit conversational context  
- non‑governed logs  
- transient runtime state  

---

## 10. Mixed‑Era Operation (v2.3 → v2.4)

Chorais operates in an environment where:

- some historical tranches and tickets are **v2.3‑aligned**  
- new tranches and tickets are **v2.4‑aligned**  

Chorais MUST:

- treat v2.3 artefacts under archive namespaces as **immutable legacy**  
- avoid retrofitting v2.4 rules onto archived v2.3 artefacts  
- ensure all **new** governed artefacts comply with v2.4 contracts  

Where migration is required, Chorais MUST follow the **Migration Rules** in the Naming Scheme Contract and record lineage in governed reconciliation artefacts.

---

## 11. Governance and Drift Classification

Chorais MUST classify drift according to:

- Naming Scheme Contract  
- Namespace Scheme Contract  
- Identity Propagation Contract  
- DECOR Specification  
- Documentation Envelope Contract  
- Replay Trace Contract  

Drift categories include:

- structural  
- naming  
- namespace  
- identity  
- determinism  
- documentation  
- governance  

All drift MUST be:

- recorded under `/fugue_docs/verification/<tranche-name>/` and `/fugue_docs/replay/<tranche-name>/`  
- reconciled via tickets and Reconciled DECOR  
- validated by Auditor and Verifier personas  

---

## 12. Long‑Term Vision: Chorais as Fugue Engine

Chorais’ long‑term direction is to:

- **model** Fugue v2.4 contracts as first‑class orchestration entities  
- **simulate** multi‑persona workflows deterministically  
- **compose** orchestration flows from governed metadata and DECOR  
- **enforce** governance envelopes at runtime  
- **replay** tranches and tickets deterministically  
- **integrate** identity, naming, namespace, and documentation envelopes into a single orchestration substrate  

In this role, Chorais is:

> A system that **performs** the Fugue Orchestration Method v2.4  
> rather than merely **using** it.

---

## 13. Compliance Summary

Chorais MUST comply with:

- DECOR Specification (v2.4)  
- Reconciled DECOR Contract (v2.4)  
- Naming Scheme Contract (v2.4)  
- Namespace Scheme Contract (v2.4)  
- Identity Propagation Contract (v2.4)  
- Documentation Envelope Contract (v2.4)  
- Ticket Template and Ticket Map Contracts (v2.4)  
- Replay Trace Contract (v2.4)  
- Lifecycle Contract (v2.4)  

Chorais MUST ensure:

- ticket template fidelity  
- DECOR schema alignment  
- persona‑isolated orchestration  
- deterministic replay  
- auditability of all governed artefacts  

Any deviation from these contracts in Chorais is **governance drift** and MUST be surfaced, classified, and reconciled through governed workflows.