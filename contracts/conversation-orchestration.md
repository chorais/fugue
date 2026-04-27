# **Conversation Orchestration Contract (v2.4)**  
Version: 2.4  
Status: Active  
Governance Authority: Curator  
Methodology: Fugue Orchestration Method v2.4  
Scope: Multi‑Conversation Governance  
Personas Bound: Sponsor, Conductor, Architect, Implementer, Auditor  

---

# 1. Purpose  
The Conversation Orchestration Contract defines the **governed, deterministic, persona‑isolated multi‑conversation execution model** used by Fugue.

This contract ensures:

- strict persona isolation  
- deterministic lifecycle execution  
- governed artefact flow  
- naming and namespace correctness  
- identity propagation correctness  
- DECOR alignment  
- metadata alignment  
- reproducibility and replayability  

This contract is binding across all tranches and substrates.

---

# 2. The Four‑Conversation Model  
Fugue uses exactly **four** persistent conversations.  
Each conversation MUST maintain strict persona isolation and MUST operate only in its assigned Fugue Mode.

---

## 2.1 Initiator Conversation  
**Active Mode:** Intake Mode  
**Active Persona:** Sponsor  
**Purpose:**  
- produce tranche preamble  
- define mission, scope, boundaries, acceptance criteria  
- initialise tranche identity  

The Initiator Conversation MUST NOT perform orchestration, implementation, or verification.

---

## 2.2 Conductor Conversation  
**Active Mode:** Orchestration Mode  
**Active Personas:** Conductor, Architect, Auditor (invoked only when required)  
**Purpose:**  
- interpret tranche intent  
- enforce DECOR  
- generate Ticket Map  
- assign persona routing  
- enforce metadata  
- enforce naming and namespace correctness  
- enforce identity propagation  
- coordinate Architect Fill Phase  
- dispatch tickets  
- validate Implementer outputs  
- manage lifecycle transitions  
- initiate reconciliation  

The Conductor Conversation is the **only** conversation where canonical DECOR may be created or modified.

---

## 2.3 Implementer Conversations  
**Active Mode:** Implementation Mode  
**Active Persona:** Implementer  
**Purpose:**  
- execute tickets  
- generate implementation artefacts  
- generate implementation logs  
- generate replay traces  
- perform ingress analysis  
- surface evidence for Architect  

Implementer Conversations MUST:

- remain persona‑pure  
- remain isolated  
- produce governed artefacts  
- preserve metadata  
- preserve naming and namespace correctness  

Implementer Conversations MUST NOT:

- modify DECOR  
- perform governance  
- perform reconciliation  
- act as Architect or Conductor  
- modify naming or namespaces  
- modify folder structure  

---

## 2.4 Auditor Conversation  
**Active Mode:** Verification Mode  
**Active Personas:** Auditor, Architect (invoked only when required)  
**Purpose:**  
- consume all tranche artefacts  
- validate DECOR alignment  
- validate Ticket Map alignment  
- validate metadata correctness  
- validate naming and namespace correctness  
- validate identity propagation  
- classify drift  
- request corrections  
- produce Reconciled DECOR  
- produce tranche closure artefacts  

The Auditor Conversation is the **final authority** on tranche correctness.

---

# 3. DECOR Flow Across Conversations  
DECOR is the **Requirements Consideration Protocol (RCP)** and MUST follow the governed lifecycle:

## 3.1 Implementer Ingress Analysis  
- non‑canonical  
- evidence‑only  
- informs Architect persona  
- MUST NOT modify DECOR  

## 3.2 Architect Formalisation  
- canonical **DECOR**  
- produced only in the Conductor Conversation  
- MUST follow naming‑scheme contract  
- MUST follow identity propagation rules  

## 3.3 DECOR Updates  
- triggered by ticket execution  
- formalised by Architect persona  
- stored under governed namespaces  
- MUST preserve identity and metadata  

## 3.4 Reconciled DECOR  
- produced only in the Auditor Conversation  
- final authoritative record of the tranche  
- MUST incorporate drift corrections  
- MUST align with naming‑scheme contract  
- MUST align with documentation envelope  

---

# 4. Persona Isolation Rules  
To maintain determinism:

- Each conversation MUST operate only in its assigned Fugue Mode  
- Personas MUST NOT cross conversation boundaries  
- Implementer Conversations MUST NOT contain governance or architectural reasoning  
- DECOR MUST NOT be modified outside the Conductor Conversation  
- Reconciliation MUST NOT occur outside the Auditor Conversation  
- Implementer ingress analysis MUST be treated as evidence, not decisions  
- Naming and namespace correctness MUST be preserved across all conversations  
- Identity propagation MUST be preserved across all conversations  

Persona isolation is mandatory.

---

# 5. Implementer as Technical Probe  
The Implementer acts as a **Technical Lead Ingress Probe**.

The Implementer MAY:

- inspect code  
- extract invariants  
- identify architectural surfaces  
- identify risks, opportunities, constraints  
- identify evaluator semantics  
- identify governance surfaces  

The Implementer MUST NOT:

- produce canonical DECOR  
- make architectural decisions  
- perform governance  
- perform reconciliation  
- modify naming or namespaces  

Ingress analysis is evidence‑only.

---

# 6. Method A vs Method B DECOR Timing  

## Method A — Product Grounding  
- Sponsor provides product‑first preamble  
- Implementer ingress analysis optional  
- Architect produces DECOR  
- DECOR is product‑led  

## Method B — Technical Grounding  
- Implementer ingress analysis mandatory  
- Architect formalises DECOR from technical evidence  
- DECOR is architecture‑led  

Both methods MUST follow the same conversation structure and persona boundaries.

---

# 7. Lifecycle: Bootstrap → Ticket Loop → Reconciliation  

## 7.1 Bootstrap (Conductor Conversation)  
The Conductor MUST:

- interpret tranche intent  
- request ingress analysis (Method B)  
- enforce naming and namespace correctness  
- enforce identity propagation  
- coordinate Architect persona  
- produce DECOR  
- produce Ticket Map  
- initialise tranche logs  

## 7.2 Ticket Loop (Implementer + Conductor Conversations)  
- Implementer executes tickets in isolated conversations  
- Conductor validates outputs  
- Architect updates DECOR when required  
- Conductor enforces naming, namespace, and metadata correctness  
- Ticket Map evolves under governance  

## 7.3 Reconciliation (Auditor Conversation)  
- Auditor consumes all artefacts  
- Auditor validates DECOR alignment  
- Auditor validates naming and namespace correctness  
- Auditor validates identity propagation  
- Architect resolves structural inconsistencies  
- Auditor produces Reconciled DECOR  
- Auditor produces tranche closure artefacts  

Lifecycle execution MUST be deterministic.

---

# 8. Naming, Namespace, and Identity Enforcement  
All conversations MUST enforce:

- naming‑scheme contract  
- canonical folder taxonomy  
- namespace correctness  
- identity propagation rules  

Violations MUST be escalated to the Auditor.

---

# 9. Governed Artefact Flow  
All governed artefacts MUST:

- flow through the correct conversation  
- preserve metadata  
- preserve naming  
- preserve namespaces  
- preserve identity  
- remain persona‑aligned  
- remain deterministic  

Governed artefacts MUST NOT be created or modified outside their authorised conversation.
