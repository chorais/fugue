
# **decor.md (v2.4)**  
**Hybrid DECOR Template (v2.4)**  
**Location:** `/fugue/templates/decor.md`  
**Purpose:** Human‑friendly + schema‑aligned DECOR authoring template  
**Authority:** Architect Persona  
**Status:** Canonical once formalised  

---

# 0. Metadata  
*(Structured metadata block — aligns exactly with `/schemas/decor-schema.json`)*

```yaml
metadata:
  tranche-name: "<tranche-name>"
  decor-version: "v2.4"
  author-persona: "Architect"
  source: "Initial|Update"
  method: "A|B"
  requires-fill: <true|false>
  governance-envelope: "<link-or-id>"
  identity-propagation-rules: "<link-or-id>"
  persona-routing-summary: "<Architect|Implementer|Hybrid>"
  documentation-requirements: "<summary>"
  dependencies:
    - "<artefact>"
  status: "Draft|Active|Superseded"
  last-updated: "<YYYY-MM-DD>"

  # Schema reference (updated)
  schema: "/schemas/decor-schema.json"

  # Namespace references (updated)
  namespace:
    decor-root: "/fugue_docs/decors/<tranche-name>/"
    decor-updates: "/fugue_docs/decors/<tranche-name>/decor-updates/"
    reconciled-decor: "/fugue_docs/decors/<tranche-name>/reconciled-decor.md"
```

---

# 1. **Design**  
**Structural intent, boundaries, and required behaviours.**  
*(Narrative + structured items)*

### 1.1 Structural Intent  
Describe the architectural purpose and scope of the tranche.

### 1.2 Required Surfaces  
List the structural surfaces that MUST exist.

### 1.3 Structural Boundaries  
Define what the system MUST NOT do.

### 1.4 Required Behaviours  
Define behaviours that MUST be implemented.

### 1.5 Determinism Requirements  
Define deterministic expectations for:

- behaviour  
- state transitions  
- outputs  
- logs  
- replay traces  

### 1.6 Documentation Requirements  
Define conceptual documentation required for this tranche.

### 1.7 **Design Items (Schema‑Aligned)**

```yaml
design:
  - id: "D-001"
    title: "<design-surface-title>"
    description: "<description>"
    invariants:
      - "<invariant>"
    constraints:
      - "<constraint>"
    determinism:
      behaviour: ["<rule>"]
      state-transitions: ["<rule>"]
      outputs: ["<rule>"]
      logs: ["<rule>"]
      replay-traces: ["<rule>"]
    documentation:
      - "<required-doc>"
    metadata:
      content-required: <true|false>
      implementation-required: <true|false>
      architect-required: <true|false>
      documentation-required: <true|false>
      governance-critical: <true|false>
      determinism-critical: <true|false>
      risk-critical: <true|false>
```

---

# 2. **Extensions**  
**Optional structural surfaces that MUST NOT be implemented unless explicitly ticketed.**

### 2.1 Optional Surfaces  
### 2.2 Optional Behaviours  
### 2.3 Optional Documentation  
### 2.4 Ticketing Requirements  

### 2.5 **Extension Items (Schema‑Aligned)**

```yaml
extensions:
  - id: "E-001"
    title: "<extension-title>"
    description: "<description>"
    opportunities:
      - "<opportunity>"
    risks:
      - "<risk>"
    metadata:
      content-required: <true|false>
      implementation-required: <true|false>
      architect-required: <true|false>
```

---

# 3. **Considerations**  
**Invariants, constraints, governance envelopes, persona boundaries.**

### 3.1 Invariants  
### 3.2 Constraints  
### 3.3 Governance Envelopes  
### 3.4 Persona Boundaries  
### 3.5 Documentation Constraints  
### 3.6 Determinism Constraints  
### 3.7 Identity Propagation Constraints  
### 3.8 Method A / Method B Considerations  

### 3.9 **Consideration Items (Schema‑Aligned)**

```yaml
considerations:
  - id: "C-001"
    title: "<consideration-title>"
    description: "<description>"
    implications:
      - "<implication>"
    invariants:
      - "<invariant>"
    constraints:
      - "<constraint>"
    governance-envelopes:
      - "<envelope>"
    persona-boundaries:
      - "<boundary>"
    documentation-constraints:
      - "<constraint>"
    determinism-constraints:
      - "<constraint>"
    identity-propagation-constraints:
      - "<constraint>"
    method: "A|B"
    metadata:
      content-required: <true|false>
      implementation-required: <true|false>
      architect-required: <true|false>
```

---

# 4. **Opportunities**

```yaml
opportunities:
  - id: "O-001"
    title: "<opportunity-title>"
    description: "<description>"
    benefits:
      - "<benefit>"
    metadata:
      content-required: <true|false>
      implementation-required: <true|false>
      architect-required: <true|false>
```

---

# 5. **Risks**

```yaml
risks:
  - id: "R-001"
    title: "<risk-title>"
    description: "<description>"
    mitigations:
      - "<mitigation>"
    metadata:
      content-required: <true|false>
      implementation-required: <true|false>
      architect-required: <true|false>
```

---

# 6. **Open Questions**

```yaml
open-questions:
  - id: "Q-001"
    title: "<question-title>"
    question: "<question>"
    blocking: <true|false>
    metadata:
      content-required: <true|false>
      implementation-required: <true|false>
      architect-required: <true|false>
```

---

# 7. **Naming Rules**

```yaml
naming:
  rules:
    - "<rule>"
  reserved-prefixes:
    - "<prefix>"
  reserved-suffixes:
    - "<suffix>"
  patterns:
    - "<regex>"
```

---

# 8. **Namespace Rules**

```yaml
namespaces:
  rules:
    - "<rule>"
  hierarchy:
    - "/fugue_docs/decors/<tranche-name>/"
  constraints:
    - "<constraint>"
```

---

# 9. **Identity Propagation Rules**

```yaml
identity-propagation:
  rules:
    - "<rule>"
  anchors:
    - "<anchor>"
  invariants:
    - "<invariant>"
```

---

# 10. **Governance Envelopes**

```yaml
governance:
  envelopes:
    - id: "G-001"
      description: "<governance-surface>"
      enforced-by: "Conductor|Architect|Auditor"
```

---

# 11. **Grounding (Method A/B)**

```yaml
grounding:
  method: "A|B"
  evidence:
    - "<evidence-source>"
  justification: "<why>"
```

---

# 12. **Routing Metadata**

```yaml
routing:
  persona: "architect|implementer|auditor|hybrid"
```

---

# 13. **Evaluator Metadata**

```yaml
evaluator:
  categories:
    - "<category>"
  diagnostics:
    - "<diagnostic>"
```

---

# 14. **Lifecycle Metadata**

```yaml
lifecycle:
  phase: "intake|orchestration|implementation|verification|closure"
```

---

# 15. **Change Log**

```yaml
changelog:
  - version: "<v2.4.x>"
    date: "<YYYY-MM-DD>"
    changes:
      - "<change>"
    updated-by: "<architect>"
```

---
