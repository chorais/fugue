# **Fugue Onboarding Guide (v2.4)**  
Version: 2.4  
Status: Active (Frozen)  
*A practical introduction for new contributors*

Welcome to **Fugue** — a governance‑first methodology for running complex AI‑assisted software development in a deterministic, auditable, and scalable way.

This guide gives you everything you need to understand:

- how Fugue structures work  
- how personas and conversations operate  
- how the human operator participates  
- how to run a tranche from start to finish  
- where to find the right documents  
- how to avoid common mistakes  

It’s intentionally short, friendly, and practical.

---

# **1. What Fugue Is (and Why It Exists)**

Modern AI models are powerful, but they struggle when:

- conversations get too long  
- instructions mix across roles  
- architecture and implementation blur together  
- context becomes overloaded  
- the model is asked to “do everything at once”  

This leads to:

- drift  
- hallucination  
- inconsistent outputs  
- loss of structure  
- token inefficiency  

**Fugue solves this by splitting work into structured phases, each handled by a dedicated AI persona with strict boundaries.**

This gives you:

- deterministic outputs  
- reproducible lifecycles  
- clean artefacts  
- auditability  
- low drift  
- low token usage  
- predictable behaviour  

Fugue is not just a workflow — it’s a *governance system* for AI‑assisted engineering.

---

# **2. How Work Is Structured: Project → Branch → Theme → Tranche → Ticket**

Fugue uses a **five‑level governance hierarchy**:

```
Project
  → Branch
      → Theme
          → Tranche
              → Ticket
```

### **Projects**  
Long‑running missions with architectural identity and governance posture.

### **Branches**  
Execution lanes inside a project.  
Branches *realise* Themes.

### **Themes**  
Conceptual groupings of related work.  
Themes are conceptual under the Project, but structurally live inside Branches.

### **Tranches**  
The atomic **lifecycle unit** in Fugue.  
A tranche executes the full 6‑phase lifecycle and contains multiple Tickets.  
Each tranche has:

- a mission  
- a scope  
- boundaries  
- acceptance criteria  
- risks  
- dependencies  

Each tranche produces:

- a **preamble**  
- **Initial DECOR (`decor.md`)**  
- a **Ticket Map**  
- **implementation outputs**  
- **Reconciled DECOR**  
- a **Closure Report**

### Tickets
The atomic **execution unit** in Fugue.
Each ticket specifies a single piece of work and is assigned to an Implementer or Architect.
Tickets produce:
- code and tests
- implementation logs
- replay traces
- determinism validation

## Important Distinction: Tranche vs. Ticket

Fugue distinguishes between **lifecycle units** and **execution units**:

- **Tranche = Atomic Lifecycle Unit**
  - Executes the complete 6‑phase lifecycle
  - Produces DECOR, Ticket Map, reconciliation, closure
  - Managed by the Orchestrator

- **Ticket = Atomic Execution Unit**
  - Executes a single piece of work
  - Produces code, tests, logs, traces
  - Assigned to Implementers or Architects

A single tranche may contain many tickets.

---

# **3. The Personas (What They Do and Why They Exist)**

Fugue personas are not different models — they are **different reasoning modes** with strict boundaries.

## **Conceptual Personas (Governance Layer)**  
- **Curator** — defines tranche mission, boundaries, acceptance criteria  
- **Conductor** — orchestrates lifecycle, metadata, persona routing  
- **Architect** — formalises DECOR, invariants, constraints  
- **Methodologist** — evolves the methodology itself  

## **Practical Personas (Execution Layer)**  
- **Initiator** — prepares the tranche workspace and validates the preamble  
- **Orchestrator** — runs the lifecycle and manages the Ticket Map  
- **Implementer** — executes tickets deterministically  
- **Auditor** — performs drift classification and reconciliation  
- **Verifier** — validates correctness before closure  

**Why personas?**  
Because mixing reasoning modes causes drift.  
Persona isolation keeps the system deterministic.

---

# **4. The Human Operator (Human‑in‑the‑Loop Role)**  
### *Where the human participates, corrects, clarifies, and governs*

Fugue is explicitly **human‑in‑the‑loop**.  
The human operator ensures the system stays aligned with real‑world goals.

The human intercedes at every phase:

---

## **4.1 During Bootstrap (Initiator Phase)**  
The human operator:

- provides the background intent  
- reviews the generated preamble  
- ensures mission, scope, and boundaries are correct  
- clarifies ambiguities  
- approves the preamble before orchestration begins  

---

## **4.2 During Interpretation (Architect Phase)**  
The human operator:

- confirms the Architect’s interpretation of the preamble  
- validates the Initial DECOR  
- requests corrections if DECOR misinterprets intent  

---

## **4.3 During Implementation (Implementer Phase)**  
The human operator:

- reviews tickets before implementation  
- clarifies ambiguous requirements  
- provides missing domain knowledge  
- checks implementation outputs at checkpoints  
- requests rework if outputs deviate from DECOR or intent  

---

## **4.4 During Reconciliation (Auditor Phase)**  
The human operator:

- reviews reconciliation results  
- validates drift classifications  
- approves Reconciled DECOR  
- approves the Closure Report  

---

## **4.5 Between Tranches**  
The human operator:

- defines the next tranche  
- sequences tranches within a theme  
- maintains long‑term product vision  
- prevents scope creep  

---

## **4.6 Drift Correction (Across All Phases)**  
The human operator intervenes when:

- a persona begins reasoning outside its boundaries  
- a conversation mixes roles  
- an artefact contradicts the preamble  
- DECOR becomes too implementation‑specific  
- implementation deviates from DECOR  
- verification misses discrepancies  

---

# **5. The Fugue Lifecycle (What Actually Happens)**

Fugue uses a **six‑phase deterministic lifecycle**:

```
Bootstrap
→ Interpretation
→ Implementation
→ Reconciliation
→ Verification
→ Closure
```

Here’s the lifecycle in plain English:

### **1. Initiator → Preamble**  
“What are we trying to do?”

### **2. Orchestrator → Bootstrap**  
“Prepare the workspace and envelopes.”

### **3. Architect → Initial DECOR (`decor.md`)**  
“What are the architectural invariants?”

### **4. Orchestrator → Ticket Map**  
“What work needs to be done?”

### **5. Implementer → Ticket Loop**  
“Let’s build it.”

### **6. Auditor → Reconciliation**  
“Did we do what we said we would do?”

### **7. Verifier → Final Validation**  
“Does everything pass?”

### **8. Orchestrator → Closure**  
“Everything is complete.”

This cycle repeats for each tranche.

---

# **6. What You Actually Do as an Operator**

Here’s the minimal workflow you’ll follow:

### **Step 1 — Start the Initiator conversation**  
Generate the preamble.

### **Step 2 — Start the Orchestrator conversation**  
Attach the preamble + orchestration substrate.  
Let it run Bootstrap.

### **Step 3 — Let the Orchestrator invoke the Architect**  
Architect produces **Initial DECOR (`decor.md`)**.

### **Step 4 — Start the Implementer conversation**  
Attach the DECOR subset.  
Execute tickets one by one.

### **Step 5 — Start the Auditor conversation**  
Attach all tranche artefacts.  
Perform reconciliation.

### **Step 6 — Start the Verifier conversation**  
Validate correctness.

### **Step 7 — Move to the next tranche**  
Repeat.

That’s it.

---

# **7. Where Everything Lives (Your Mental Map)**

### **Seeding Guides**  
How to start each persona conversation:

```
/fugue/seeding/initiator-seeding.md
/fugue/seeding/orchestrator-seeding.md
/fugue/seeding/architect-seeding.md
/fugue/seeding/implementer-seeding.md
/fugue/seeding/auditor-seeding.md
/fugue/seeding/verifier-seeding.md
```

### **Conceptual Docs**  
How Fugue works:

```
/fugue/docs/methodology-overview.md
/fugue/docs/fugue-orchestration-method.md
/fugue/docs/new-contributors-guide.md
/fugue/docs/fugue-glossary.md
```

### **Tranche Artefacts**  
Outputs of each tranche:

```
/fugue_docs/tranches/tranche-<ID>/
```

---

# **8. Common Mistakes (and How to Avoid Them)**

### **❌ Mixing personas in one conversation**  
Always start a new conversation for each persona.

### **❌ Reusing Orchestrator or Implementer across tranches**  
They are tranche‑scoped.

### **❌ Giving the Implementer too much context**  
It should only see the DECOR subset + ticket.

### **❌ Giving the Architect implementation artefacts**  
It must only see the preamble + DECOR spec.

### **❌ Forgetting to attach files during seeding**  
Each persona needs its substrate.

### **❌ Letting conversations drift**  
If a persona starts doing the wrong kind of reasoning, reseed.

---

# **9. Quick Start Checklist**

Here’s your “start a tranche in 60 seconds” guide:

- [ ] Open Initiator → generate preamble  
- [ ] Open Orchestrator → attach preamble + substrate  
- [ ] Let Orchestrator invoke Architect  
- [ ] Open Architect → produce Initial DECOR (`decor.md`)  
- [ ] Orchestrator → generate Ticket Map  
- [ ] Open Implementer → attach DECOR subset  
- [ ] Implement tickets  
- [ ] Open Auditor → attach all artefacts  
- [ ] Reconcile  
- [ ] Open Verifier → validate correctness  
- [ ] Close tranche  

You’re now running Fugue correctly.

---

# **10. What to Read Next**

If you’re new, read these in order:

1. **Methodology Overview**  
2. **Fugue Orchestration Method**  
3. **New Contributors Guide**  
4. **Fugue Glossary**  
5. **Seeding Guides** (as needed)

---
