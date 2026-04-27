# **Fugue Glossary (v2.4)**  
Version: 2.4  
Status: Active (Frozen)  
A complete reference of core terms, concepts, personas, artefacts, governance objects, and lifecycle constructs in the Fugue Orchestration Method.

---

# **A**

### **Architect (Conceptual Persona)**  
A governance‑layer persona responsible for **DECOR formalisation**, invariants, constraints, structural reasoning, and reconciliation alignment.  
The Architect alone formalises DECOR and DECOR updates.

### **Architectural Invariant**  
A rule or constraint defined in DECOR that MUST hold across all implementation and reconciliation phases.

### **Artefact**  
Any governed output produced during a tranche, including preamble, DECOR, Ticket Map, tickets, logs, traces, drift surfaces, reconciliation logs, and Reconciled DECOR.

---

# **B**

### **Bootstrap (Phase 1)**  
The first lifecycle phase where the Curator defines tranche mission and the Initiator produces the tranche preamble.  
Metadata and namespace setup validated by the Conductor.

### **Branch (Governance Object)**  
An **execution lane** inside a Project.  
Branches define:

- execution direction  
- governance envelope subset  
- naming + namespace subset  
- identity propagation root  
- persona routing subset  

A Branch **realises Themes**.  
A Theme may span multiple Branches over the life of a Project.

**Identity root:** `B<id>`  
**Namespace root:** `project/<id>/branch/<id>/…`

---

# **C**

### **Category‑Based Namespace**  
The v2.4 namespace model that organises governed artefacts by category (e.g., `decors/`, `tickets/`, `logs/`, `replay/`, `drift/`, `reconciliation/`) rather than numeric tranche identifiers.

### **Closure (Phase 6)**  
The final lifecycle phase where the Curator approves closure and the tranche is archived as immutable lineage.

### **Conductor (Conceptual Persona)**  
The lifecycle orchestrator responsible for persona routing, metadata enforcement, governance alignment, and lifecycle transitions.

### **Curator (Conceptual Persona)**  
The governance authority responsible for tranche mission, boundaries, acceptance criteria, and final approval of closure.

---

# **D**

### **DECOR (Declarative Contract of Record)**  
The canonical architectural contract for a tranche.  
Defines architectural intent, invariants, constraints, metadata, evaluator surfaces, and reconciliation surfaces.  
Schema‑validated and immutable except via governed updates.

### **DECOR Update**  
A governed modification to DECOR, formalised exclusively by the Architect during Interpretation or Reconciliation.

### **Determinism Envelope**  
A contract enforcing deterministic execution, replay correctness, evaluator alignment, and metadata propagation.

### **Drift**  
Any deviation between implementation outputs and DECOR.  
Classified by the Auditor as **Minor**, **Major**, or **Critical**.

---

# **E**

### **closure-report.md**  
The canonical tranche closure artefact in v2.4.  
Records closure decisions, final validations, reconciled outcomes, and governance sign-off.

### **Evaluator**  
A deterministic governance component that validates invariants, metadata, naming, namespace, identity propagation, and replay correctness.  
Evaluators do not modify artefacts.

---

# **F**

### **Fugue Method**  
A governance‑first orchestration methodology for AI‑assisted software development, built on persona isolation, deterministic artefacts, schema‑validated metadata, and a six‑phase lifecycle.

---

# **G**

### **Governance Envelope**  
A contract enforcing persona boundaries, lifecycle boundaries, metadata correctness, and governance posture.

### **Governance Drift**  
A deviation from governance rules, metadata, or persona boundaries detected by the Auditor.

---

# **I**

### **Identity Propagation**  
The v2.4 contract governing how identifiers (e.g., ticket IDs, DECOR IDs, tranche IDs) propagate deterministically across artefacts.

### **Human Operator**
The human governance actor who provides intent clarifications, business context, and final business-level judgement.  
Not a persona. Replaces legacy intake-role terminology in active v2.4 documentation.

### **Implementer (Practical Persona)**  
Executes tickets, produces code, tests, logs, and replay traces.  
Must follow DECOR and Ticket Map constraints exactly.

### **Initiator (Practical Persona)**  
Starts a tranche and produces the tranche preamble.  
Does not perform architectural or implementation reasoning.

### **Interpretation (Phase 2)**  
The lifecycle phase where the Architect formalises DECOR, validates schema, aligns naming/namespace/identity propagation, and selects Method A or Method B grounding.

---

# **L**

### **Lifecycle (Fugue Lifecycle)**  
The six‑phase deterministic sequence:  
**Bootstrap → Interpretation → Implementation → Reconciliation → Verification → Closure**

### **Log (Implementation Log)**  
A deterministic record of implementation decisions, evidence, and execution traces produced by the Implementer.

---

# **M**

### **Method A (Product‑First Grounding)**  
A DECOR grounding strategy selected by the Architect during Interpretation when product intent is clear and DECOR can be formalised early.

### **Method B (Technical‑First Grounding)**  
A DECOR grounding strategy selected by the Architect during Interpretation when architecture must be discovered through ingress analysis.

### **Methodologist (Conceptual Persona)**  
Responsible for evolving the methodology itself.  
Does not participate in project execution.

---

# **N**

### **Naming Scheme Contract**  
The v2.4 contract defining canonical naming rules for all governed artefacts (e.g., `T<number>`, `C<number>`, `E<number>`).

### **Namespace Scheme Contract**  
The v2.4 contract defining canonical category‑based namespaces for all governed artefacts.

---

# **O**

### **Orchestrator (Practical Persona)**  
Manages the ticket loop, dispatches tickets, validates outputs, and enforces governance during implementation.

---

# **P**

### **Preamble (Tranche Preamble)**  
The authoritative expression of tranche mission, scope, boundaries, risks, and acceptance criteria, produced by the Initiator.

### **Persona**  
A constrained reasoning mode with strict boundaries and responsibilities.  
Fugue uses **four conceptual personas** and **five practical personas**.

### **Project (Governance Object)**  
The highest‑level governance container.  
Defines long‑term mission, architectural domain, governance envelope, naming + namespace roots, and identity propagation root.

**Conceptually:**  
A Project contains many Themes.

**Structurally:**  
A Project contains Branches, which realise Themes.

**Identity root:** `P<id>`  
**Namespace root:** `project/<id>/…`

---

# **R**

### **Reconciled DECOR**  
The final architectural artefact produced during Reconciliation after drift classification and structural correction.

### **Reconciliation (Phase 4)**  
The lifecycle phase where the Auditor classifies drift and the Architect performs structural reconciliation.

### **Replay Trace**  
A deterministic execution trace produced by the Implementer and validated by the Auditor and Verifier.

---

# **S**

### **Schema (DECOR Schema)**  
The JSON Schema defining the structure, metadata, and invariants required for DECOR and DECOR updates.

---

# **T**

### **Theme (Governance Object)**  
A conceptual grouping of related work inside a Project.  
Themes represent architectural narratives and problem‑space groupings.

**Conceptually:**  
A Project contains many Themes.

**Structurally:**  
Themes are realised inside Branches and contain Tranches.

**Identity root:** `T<id>`  
**Namespace root:** `project/<id>/branch/<id>/theme/<id>/…`

### **Ticket**  
A discrete unit of implementation work derived from DECOR and the Ticket Map.  
The Ticket is the atomic execution unit.

### **Ticket Loop**  
The iterative process where the Orchestrator dispatches tickets and the Implementer executes them in isolated conversations.

### **Ticket Map**  
A structured list of all tickets required to satisfy DECOR.  
Derived from DECOR during Interpretation.

### **Ticket Set**
The canonical v2.4 term for the Ticket Map and its implementation tickets as a governed execution surface.  
Replaces legacy bundle terminology.

### **Tranche (Execution Object)**  
The atomic lifecycle unit in Fugue.  
Contains preamble, DECOR, Ticket Map, implementation outputs, reconciliation, verification, and closure.

**Identity root:** `C<id>`  
**Namespace root:** `…/tranche/<id>/…`

---

# **V**

### **Verification (Phase 5)**  
The lifecycle phase where the Verifier executes the test suite (golden, dark, governance, replay) and validates correctness.

### **Verifier (Practical Persona)**  
Performs final validation before closure.  
Ensures all tests pass and all envelopes are satisfied.

---

# **Z**

### **Zero‑Drift Goal**  
The objective of ensuring implementation outputs match DECOR exactly, with all deviations classified and reconciled.

---
