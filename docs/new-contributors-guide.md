# 1. Welcome to Fugue

Fugue is a **governance‑first orchestration method** for AI‑assisted software development.  
It ensures that:

- work is deterministic  
- reasoning is isolated  
- architecture is governed  
- implementation is auditable  
- documentation is structured  
- metadata drives everything  
- personas never drift  
- the system is reproducible  

This guide gives you everything you need to contribute safely and confidently.

---

# 2. What Makes Fugue Different?

Fugue is not a framework.  
It is not a coding style.  
It is not a project template.

Fugue is a **methodology** that governs:

- how AI personas think  
- how artefacts flow  
- how architecture is formalised  
- how implementation is executed  
- how correctness is validated  
- how drift is classified  
- how documentation is produced  
- how tranches are closed  

It is designed to make AI‑assisted development:

- predictable  
- auditable  
- safe  
- scalable  
- repeatable  

If you follow the rules, Fugue works beautifully.  
If you break the rules, Fugue will catch you — and that’s by design.

---

# 3. The Five Personas

Fugue uses **five conceptual personas**, each with strict cognitive boundaries.

These are *not* job titles.  
They are *thinking modes*.

| Persona | What They Do | What They Never Do |
|---------|--------------|--------------------|
| **Human Operator** | Defines intent, scope, boundaries | Never designs or implements |
| **Architect** | Formalises DECOR, designs structure | Never writes code |
| **Conductor** | Orchestrates lifecycle, routing, metadata | Never implements or design architecture |
| **Implementer** | Writes code, tests, logs, traces | Never designs or governs |
| **Auditor** | Validates correctness, classifies drift | Never implements or design |

Each persona has a **contract** that governs its behaviour.

You will switch personas depending on the task — but **never mix them**.

---

# 4. The Eight Governance Contracts

Fugue is governed by eight contracts:

1. **DECOR Specification**  
2. **Ticket Map Contract**  
3. **Auditor Contract**  
4. **Conductor Contract**  
5. **Implementer Technical Probe Contract**  
6. **Documentation Envelope Contract**  
7. **Tranche Lifecycle Contract**  
8. **Evaluator Model Contract**

These contracts define:

- what each persona must do  
- what each persona must not do  
- how artefacts flow  
- how metadata is preserved  
- how lifecycle transitions occur  
- how drift is classified  

You do not need to memorise them — but you must respect them.

---

# 5. The Tranche Lifecycle

Every tranche follows the same deterministic lifecycle:

```
Intake
→ Bootstrap
→ Architect Fill Phase
→ Ticket Loop
→ Reconciliation
→ Closure
```

### **Intake**  
Human Operator defines intent.

### **Bootstrap**  
Architect formalises DECOR.  
Conductor builds the Ticket Map.  
Implementer performs ingress analysis.

### **Fill Phase**  
Architect completes conceptual surfaces.  
Conductor validates metadata.

### **Ticket Loop**  
Implementer executes tickets in isolated conversations.  
Conductor dispatches and validates.

### **Reconciliation**  
Auditor validates correctness and produces Reconciled DECOR.

### **Closure**  
Conductor publishes final artefacts.

---

# 6. Metadata: The Heart of Fugue

Metadata governs:

- persona routing  
- Fill Phase requirements  
- documentation routing  
- evaluator execution  
- lifecycle transitions  
- drift classification  

Metadata flows through the system like this:

```
DECOR metadata
→ Ticket Map metadata
→ Dispatch metadata
→ Implementation metadata
→ Audit metadata
→ Reconciled DECOR metadata
```

If metadata is wrong, the tranche is wrong.

---

# 7. How to Work on a Ticket

When you receive a ticket:

### **1. Read the Ticket Map entry**  
It tells you:

- persona routing  
- metadata  
- dependencies  
- acceptance criteria  
- documentation requirements  

### **2. Enter the correct persona**  
If the ticket says `implementer`, you must think like an Implementer.  
If it says `architect`, you must think like an Architect.

### **3. Never mix personas**  
If you need architectural clarification, escalate — do not guess.

### **4. Produce deterministic artefacts**  
Implementation logs, replay traces, tests, code.

### **5. Surface contradictions**  
If DECOR is wrong, incomplete, or contradictory, you must report it.

### **6. Never modify DECOR**  
Only the Architect can do that.

---

# 8. How to Avoid Persona Drift

Persona drift is when you accidentally think like the wrong persona.

Examples:

- Implementer suggesting architectural changes  
- Architect writing implementation details  
- Conductor making design decisions  
- Auditor proposing fixes  
- Human Operator suggesting implementation details  

To avoid drift:

- Always check your persona  
- Always check the Ticket Map  
- Always check metadata  
- Always escalate instead of guessing  

Drift is classified by the Auditor and may require epilogue tickets.

---

# 9. How to Read DECOR

DECOR is the **Declarative Contract of Record**.

It contains:

- Design  
- Extensions  
- Considerations  
- Opportunities  
- Risks  
- Open Questions  
- Metadata  

DECOR is:

- canonical  
- authoritative  
- immutable except via governed updates  
- the single source of truth  

If DECOR contradicts implementation, implementation is wrong.  
If DECOR contradicts reality, DECOR must be updated — by the Architect.

---

# 10. Documentation Rules

Documentation is governed by the **Documentation Envelope Contract**.

Key rules:

- All governed docs live in `/fugue_docs/`  
- `/docs` is developer‑owned and protected  
- `/public-docs` is user‑facing and protected  
- Documentation must be persona‑scoped  
- Documentation must be metadata‑aligned  
- Documentation must be deterministic  

Documentation drift is classified by the Auditor.

---

# 11. Evaluators

Evaluators are deterministic governance components that:

- enforce invariants  
- enforce metadata  
- enforce persona routing  
- validate artefacts  
- produce diagnostics  

Evaluators are not personas.  
They are not allowed to modify artefacts.  
They are pure governance logic.

---

# 12. What You Should Do as a New Contributor

- Read the Contract Suite README  
- Read the New Contributors Guide (this document)  
- Read the Ticket Map  
- Read DECOR  
- Read your ticket  
- Enter the correct persona  
- Follow metadata  
- Produce deterministic artefacts  
- Surface contradictions  
- Avoid persona drift  
- Ask questions early  

You do **not** need to understand everything on day one.  
You just need to follow the rules.

---

# 13. What You Should Never Do

- Modify DECOR  
- Modify metadata  
- Mix personas  
- Skip the Fill Phase  
- Change the Ticket Map  
- Add undocumented dependencies  
- Write documentation in the wrong namespace  
- Guess about architecture  
- Guess about governance  
- Ignore evaluator diagnostics  

If you’re unsure — escalate.

---

# 14. Where to Go Next

You should now read:

- **Contract Suite README**  
- **DECOR Specification**  
- **Ticket Map Contract**  
- **Documentation Envelope Contract**  

And then:

- Start with a small Implementer ticket  
- Ask questions  
- Learn the metadata flow  
- Learn the persona boundaries  

You’ll be productive very quickly.

---

# 15. Summary

You now understand:

- the personas  
- the contracts  
- the lifecycle  
- the metadata  
- the governance model  
- how to work on tickets  
- how to avoid drift  
- how to contribute safely  

Welcome to Fugue.  
You’re now ready to participate in a governed, deterministic, auditable orchestration system.

---
