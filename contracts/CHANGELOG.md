
# Fugue Contract Suite — Changelog

## 0. Metadata

```yaml
metadata:
  contract-id: "contracts-changelog"
  version: "2.4"
  authoritative: true

  applies-to:
    - fugue-contract-suite
    - methodology-level-governance
    - naming-scheme
    - namespace-scheme
    - identity-propagation
    - documentation-envelope
    - determinism-envelope
    - decor-contracts
    - ticketing-contracts
    - replay-contracts
    - lifecycle-contracts

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  governance-envelope: "<id>"
  documentation-envelope: "<id>"
  determinism-envelope: "<id>"
  lifecycle-contract: "<id>"
  ticket-map-contract: "<id>"
  replay-trace-contract: "<id>"

# Placeholder Semantics
# Fields containing "<id>" or "<self>" are canonical placeholders.
# They MUST be concretised in project/branch/theme/tranche governance envelopes.
# They MUST NOT be replaced in methodology-level contracts.
# The Auditor Persona MUST treat these placeholders as intentional and NOT as metadata drift.
```

---

# **Version 2.4 — 2026‑04‑26**  
**Status:** Active  
**Scope:** Full methodology‑level contract suite  
**Change Type:** Structural uplift, namespace correction, schema alignment, governance tightening

## 1. Overview

Version 2.4 is a **major governance uplift** of the Fugue Methodology.  
It introduces:

- canonical metadata blocks across all methodology‑level contracts  
- placeholder semantics for `<id>` and `<self>`  
- canonical DECOR JSON Schema  
- namespace alignment across all templates and contracts  
- naming‑scheme enforcement across schemas  
- reconciliation of legacy v2.3 drift  
- removal of conversational residue from governed surfaces  
- alignment of Chorais Implementation Profile with v2.4 governance  

This version completes the transition from **v2.3 (legacy)** to **v2.4 (canonical)**.

---

## 2. Contract‑Level Changes

### **2.1 DECOR Specification**
- Added full v2.4 metadata block  
- Added placeholder semantics  
- Added envelope references  
- Ensured alignment with `/schemas/decor-schema.json`  
- Clarified inheritance rules across project/branch/theme/tranche  

### **2.2 Reconciled DECOR Contract**
- Added metadata block  
- Added placeholder semantics  
- Clarified lineage, drift mapping, and reconciliation rules  
- Ensured alignment with DECOR schema  

### **2.3 Naming Scheme Contract**
- Replaced legacy table metadata with v2.4 metadata block  
- Added placeholder semantics  
- Clarified tranche naming rules  
- Clarified ticket naming rules (`T<number>`, `C<number>`, `E<number>`)  
- Removed legacy numeric tranche patterns  

### **2.4 Namespace Scheme Contract**
- Added placeholder semantics  
- Clarified canonical category list  
- Removed legacy categories (`implementation`, `reconciliation`)  
- Ensured alignment with tranche folder template  

### **2.5 Identity Propagation Contract**
- Added metadata block  
- Added placeholder semantics  
- Clarified identity lineage rules  
- Clarified multi‑persona identity propagation  

### **2.6 Documentation Envelope Contract**
- Added metadata block  
- Added placeholder semantics  
- Clarified governed vs non‑governed documentation  
- Clarified documentation routing and persona boundaries  

### **2.7 Determinism Envelope**
- Added metadata block  
- Added placeholder semantics  
- Clarified deterministic replay, ordering, evaluator behaviour  

### **2.8 Ticket Template Contract**
- Added metadata block  
- Added placeholder semantics  
- Clarified template fidelity rules  
- Clarified persona‑scoped responsibilities  

### **2.9 Ticket Map Contract**
- Added metadata block  
- Added placeholder semantics  
- Clarified DECOR → ticket mapping  
- Clarified metadata propagation  

### **2.10 Replay Trace Contract**
- Added metadata block  
- Added placeholder semantics  
- Clarified replay determinism, evaluator behaviour, identity lineage  

### **2.11 Chorais Implementation Profile**
- Fully rewritten for v2.4  
- Removed conversational residue  
- Added metadata block + placeholder semantics  
- Aligned namespaces with v2.4  
- Clarified persona isolation and orchestration model  

---

## 3. Schema & Template Changes

### **3.1 DECOR JSON Schema**
- Added canonical `/schemas/decor-schema.json`  
- Replaced legacy `decor-schema,json`  
- Added hybrid strict/permissive validation model  

### **3.2 Test Schemas**
- Updated tranche patterns to semantic naming  
- Updated ticket patterns to `T<number>`  
- Removed legacy numeric tranche identifiers  

### **3.3 Tranche Folder Template**
- Removed legacy categories (`implementation`, `reconciliation`)  
- Aligned with canonical namespace categories  
- Added metadata block + placeholder semantics  

---

## 4. Drift Resolution (v2.3 → v2.4)

### **Resolved Critical Drift**
- DECOR schema naming drift  
- DECOR schema structural drift  
- Test schema naming drift  
- Namespace drift in tranche template  
- Chorais profile namespace drift  

### **Resolved Major Drift**
- Metadata placeholders now governed  
- v2.3 conversational residue removed  
- v2.3 changelog posture corrected  

### **Remaining Expected Drift**
- `/archive/v2.3/**` (immutable legacy)  

---

# **Version 2.3 — 2026‑04‑20**  
**Status:** Historical (Legacy)  
**Scope:** Global method alignment for the Fugue Method applied to the `contract` directory  
**Change Type:** Structural tightening, metadata alignment, lifecycle clarification

*(This section is preserved exactly for lineage and auditability.)*

## Summary of changes
- Unified global versioning: all Fugue artefacts now carry `Version: 2.3`.  
- Per‑file version headers deprecated in favour of a global method version.  
- Introduced per‑folder changelogs to track local evolution.  
- Applied documentation hygiene and path normalisation.  

## Notes
- Per‑file semantic history preserved in folder‑level changelogs.  
- v2.3 is now archived and MUST NOT be modified.  

---

# 5. Summary

Version 2.4 completes the transition from **legacy v2.3** to a fully governed, metadata‑aligned, namespace‑aligned, schema‑validated methodology.

All methodology‑level contracts are now:

- self‑describing  
- metadata‑complete  
- placeholder‑governed  
- Auditor‑compliant  
- namespace‑aligned  
- naming‑aligned  
- identity‑aligned  
- determinism‑aligned  

This changelog is the authoritative record of the v2.4 uplift.

