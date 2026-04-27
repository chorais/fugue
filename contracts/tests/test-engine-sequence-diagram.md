# **test-engine-sequence-diagram.md (v2.4)**  
**Test Execution Engine — Sequence Diagram (v2.4)**  
Version: 2.4  
Status: Active  
Authority: Test Engine Contract (v2.4)  
Lifecycle Phase: Verification  
Persona: Auditor → Verifier  

---

## 0. Metadata

```yaml
metadata:
  diagram-id: "test-engine-sequence-diagram"
  version: "2.4"
  authoritative: true

  applies-to:
    - test-execution-engine
    - test-runner
    - evaluator-engine
    - replay-engine
    - metadata-engine
    - identity-engine
    - namespace-engine
    - drift-engine
    - diagnostics-engine

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  lifecycle-phase: "verification"
  persona: "auditor|verifier"

  last-updated: "<YYYY-MM-DD>"
```

---

## 1. Purpose

This diagram provides the **deterministic execution flow** of the Test Execution Engine (TEE) during Phase 4 — Verification.  
It is required by:

- Test Engine Contract  
- Test Suite Contract  
- Determinism Envelope Contract  
- Replay Trace Contract  
- Evaluator Contract  
- Identity & Namespace Contracts  

---

## 2. Sequence Diagram (Mermaid)

```mermaid
sequenceDiagram
    autonumber

    participant TR as Test Runner
    participant ME as Metadata Engine
    participant IE as Identity Engine
    participant NE as Namespace Engine
    participant EE as Evaluator Engine
    participant RE as Replay Engine
    participant DE as Drift Engine
    participant DX as Diagnostics Engine

    TR->>TR: Load test template
    TR->>TR: Load test metadata

    TR->>ME: Validate metadata propagation
    ME-->>TR: Metadata validation result

    TR->>IE: Validate identity lineage & propagation
    IE-->>TR: Identity validation result

    TR->>NE: Validate namespace placement & invariants
    NE-->>TR: Namespace validation result

    TR->>EE: Execute evaluator checks
    EE-->>TR: Evaluator diagnostics

    TR->>RE: Execute replay validation
    RE-->>TR: Replay diagnostics

    TR->>DE: Detect & classify drift
    DE-->>TR: Drift artefact

    TR->>DX: Collect diagnostics
    DX-->>TR: Diagnostic bundle

    TR->>TR: Produce test result JSON
    TR->>TR: Produce drift artefacts
    TR->>TR: Produce test run log
```

---

## 3. Determinism Notes

- Ordering MUST match the diagram exactly  
- No component may reorder transitions  
- No component may infer missing metadata  
- No component may regenerate identity  

---

## 4. Governance Notes

- Persona: Auditor → Verifier  
- Lifecycle: Verification only  
- All engines operate under strict envelope governance  

---
