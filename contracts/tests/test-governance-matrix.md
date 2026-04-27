# **test-governance-matrix.md (v2.4)**  
**Test Governance Matrix — Fugue Orchestration Method**  
Version: 2.4  
Status: Active  
Authority: Test Suite Contract (v2.4)  
Lifecycle Phase: Verification  
Persona: Auditor → Verifier  

---

## 0. Metadata

```yaml
metadata:
  matrix-id: "test-governance-matrix"
  version: "2.4"
  authoritative: true

  applies-to:
    - dark-test
    - golden-test
    - governance-test
    - replay-test

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  lifecycle-phase: "verification"
  persona: "auditor|verifier"

  last-updated: "<YYYY-MM-DD>"
```

---

## 1. Purpose

This matrix defines the **governance surfaces enforced by each test type** in Fugue v2.4.  
It is required by:

- Test Suite Contract  
- Determinism Envelope Contract  
- Governance Envelope Contract  
- Replay Trace Contract  
- Evaluator Contract  

---

## 2. Governance Surface Categories

The matrix covers nine governance surface families:

- Determinism  
- Evaluator  
- Replay  
- Identity  
- Namespace  
- Metadata  
- Documentation  
- Governance  
- Lifecycle  

---

## 3. Governance Matrix

### Legend  
✔ = Required  
✖ = Not applicable  
★ = Primary enforcement surface  

---

### **Matrix Table**

| Governance Surface | Dark Test | Golden Test | Governance Test | Replay Test |
|-------------------|-----------|-------------|------------------|-------------|
| **Determinism** | ★✔ | ★✔ | ✔ | ★✔ |
| **Evaluator** | ✔ | ✔ | ✔ | ★✔ |
| **Replay** | ✔ | ✔ | ✔ | ★✔ |
| **Identity** | ✔ | ✔ | ✔ | ★✔ |
| **Namespace** | ✔ | ✔ | ✔ | ✔ |
| **Metadata** | ✔ | ✔ | ✔ | ✔ |
| **Documentation** | ✔ | ✔ | ★✔ | ✔ |
| **Governance** | ✔ | ✔ | ★✔ | ✔ |
| **Lifecycle** | ✔ | ✔ | ★✔ | ✔ |

---

## 4. Enforcement Notes

### Dark Test  
- Primary purpose: **failure mode detection**  
- Enforces: determinism, evaluator drift, replay drift, identity drift, namespace drift  

### Golden Test  
- Primary purpose: **ideal deterministic behaviour**  
- Enforces: determinism, evaluator correctness, metadata propagation  

### Governance Test  
- Primary purpose: **strict governance alignment**  
- Enforces: persona boundaries, lifecycle boundaries, DECOR, documentation  

### Replay Test  
- Primary purpose: **deterministic replay**  
- Enforces: ordering, state transitions, identity propagation, evaluator behaviour  

---

## 5. Summary

```yaml
summary: >
  The Test Governance Matrix defines the authoritative mapping between test
  types and governance surfaces in Fugue v2.4. It ensures deterministic,
  governed, and auditable verification across all envelopes, personas, and
  lifecycle phases.
```

---