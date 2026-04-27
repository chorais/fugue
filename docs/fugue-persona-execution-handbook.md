# **Fugue Persona Execution Handbook**  
Version: 2.4
### *A Practical Guide to Running the Fugue Method Using AI Personas*

This handbook provides a **high‑level, operator‑friendly overview** of how to execute the Fugue Method using its four practical personas:

- **Initiator**  
- **Orchestrator**  
- **Architect**  
- **Implementer**  
- **Auditor**

Each persona has a dedicated seeding guide in:

```
/fugue/seeding/<persona>-seeding.md
```

This handbook explains **when** to use each persona, **how** they interact, and **how the lifecycle flows**, without repeating the detailed seeding instructions.

---

# **1. Overview of the Fugue Persona Model**

Fugue uses four practical personas to execute a tranche:

| Persona | Mode | Purpose | Reusable Across Tranches? |
|--------|------|----------|----------------------------|
| **Initiator** | Intake | Produces the tranche preamble | ✔ Yes |
| **Orchestrator** | Orchestration | Runs Bootstrap + Ticket Loop | ✘ No |
| **Architect** | Architectural | Produces Initial DECOR (decor.md) | ✔ Yes |
| **Implementer** | Implementation | Executes all tickets | ✘ No |
| **Auditor** | Verification | Performs reconciliation | ✔ Yes |

This separation ensures:

- deterministic lifecycle execution  
- persona isolation  
- reproducibility  
- auditability  
- clean handoffs  

---

# **2. The Four Conversations of a Tranche**

A tranche is executed through **four conversations**, each with a specific persona and purpose.

## **2.1 Initiator Conversation (Reusable)**  
**Purpose:** Produce the tranche preamble.  
**When:** Once per tranche.  
**Reused across tranches:** Yes.  
**Inputs:** Preamble template + methodology + persona boundaries.  
**Outputs:** `preamble.md`.

See:  
`/fugue/seeding/initiator-seeding.md`

---

## **2.2 Orchestrator Conversation (Tranche‑Scoped)**  
**Purpose:** Run Bootstrap + Ticket Loop.  
**When:** Once per tranche.  
**Reused across tranches:** No.  
**Inputs:** Preamble + orchestration substrate.  
**Outputs:**  
- Initial DECOR (decor.md)  
- Ticket Map  
- Tranche logs  
- Ticket Loop execution  

See:  
`/fugue/seeding/orchestrator-seeding.md`

---

## **2.3 Architect Conversation (Reusable)**  
**Purpose:** Produce Initial DECOR (decor.md).  
**When:** Once per tranche (invoked by Orchestrator).  
**Reused across tranches:** Yes.  
**Inputs:** Preamble + DECOR spec + persona boundaries.  
**Outputs:** `decor.md`.

See:  
`/fugue/seeding/architect-seeding.md`

---

## **2.4 Implementer Conversation (Tranche‑Scoped)**  
**Purpose:** Execute all tickets in the Ticket Loop.  
**When:** Once per tranche.  
**Reused across tranches:** No.  
**Inputs:** DECOR subset + persona boundaries.  
**Outputs:**  
- code  
- tests  
- logs  
- replay traces  

See:  
`/fugue/seeding/implementer-seeding.md`

---

## **2.5 Auditor Conversation (Reusable)**  
**Purpose:** Perform reconciliation and close the tranche.  
**When:** Once per tranche.  
**Reused across tranches:** Yes.  
**Inputs:**  
- Initial DECOR (decor.md)  
- Ticket Map  
- Ticket Map and sequenced tickets  
- Implementation logs  
- Replay traces  
- Documentation envelope  

**Outputs:**  
- Reconciled DECOR  
- Tranche Closure Report  

See:  
`/fugue/seeding/auditor-seeding.md`

---

# **3. The Fugue Lifecycle (Operator View)**

Below is the **operator‑level flow**, showing how personas interact.

---

## **Step 1 — Initiator (Intake Phase)**  
- Generate the tranche preamble.  
- Save it under:  
  `/fugue_docs/session-logs/tranche-<ID>/preamble.md`

---

## **Step 2 — Orchestrator (Bootstrap Phase)**  
- Start a new Orchestrator conversation.  
- Attach the preamble + orchestration substrate.  
- Orchestrator:  
  - interprets the preamble  
  - invokes Architect  
  - validates Initial DECOR (decor.md)  
  - generates Ticket Map  
  - starts the Ticket Loop  

---

## **Step 3 — Architect (Architectural Phase)**  
- Architect produces Initial DECOR (decor.md).  
- Orchestrator validates it and proceeds.

---

## **Step 4 — Implementer (Ticket Loop Phase)**  
- Start one Implementer conversation for the tranche.  
- Orchestrator sends tickets one by one.  
- Implementer executes each ticket.  
- Orchestrator tracks progress.

---

## **Step 5 — Auditor (Reconciliation Phase)**  
- Start one Auditor conversation.  
- Attach all tranche artefacts.  
- Auditor produces:  
  - Reconciled DECOR  
  - Tranche Closure Report  

---

# **4. Persona Interaction Summary**

### **Initiator → Orchestrator**  
Preamble is handed off.

### **Orchestrator → Architect**  
Architect produces Initial DECOR (decor.md).

### **Orchestrator → Implementer**  
Tickets are handed off one at a time.

### **Implementer → Orchestrator**  
Implementation logs and traces flow back.

### **Orchestrator → Auditor**  
All tranche artefacts are handed off for reconciliation.

---

# **5. What Operators Actually Do**

Here is the **minimal operator workflow**:

1. **Use Initiator** to generate preamble.  
2. **Start Orchestrator** for the tranche.  
3. **Let Orchestrator invoke Architect**.  
4. **Start Implementer** and run the Ticket Loop.  
5. **Start Auditor** to close the tranche.  
6. Repeat for the next tranche.

Everything else is handled by the personas.

---

# **6. Where to Find Detailed Instructions**

Each persona has a dedicated seeding guide:

```
/fugue/seeding/initiator-seeding.md
/fugue/seeding/orchestrator-seeding.md
/fugue/seeding/architect-seeding.md
/fugue/seeding/implementer-seeding.md
/fugue/seeding/auditor-seeding.md
```

This handbook is intentionally concise.  
Operators should refer to the seeding guides for:

- exact file attachments  
- seed prompts  
- persona boundaries  
- output expectations  

---

# **7. Summary**

This handbook provides:

- a high‑level overview of the Fugue persona ecosystem  
- a clear explanation of which personas persist across tranches  
- a practical lifecycle flow  
- a simple operator workflow  
- references to detailed seeding guides  

It is designed to be the **entry point** for anyone learning to run Fugue in practice.

