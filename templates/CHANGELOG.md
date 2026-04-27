# Templates Changelog

## 0. Metadata

```yaml
metadata:
  contract-id: "templates-changelog"
  version: "2.4"
  authoritative: true

  applies-to:
    - fugue-templates
    - decor-templates
    - ticket-templates
    - folder-structure-templates
    - reconciled-decor-template
    - tranche-folder-template

  naming-scheme: "v2.4"
  namespace-scheme: "v2.4"
  identity-propagation: "v2.4"

  governance-envelope: "<id>"
  documentation-envelope: "<id>"
  determinism-envelope: "<id>"
  lifecycle-contract: "<id>"
  ticket-map-contract: "<id>"
  replay-trace-contract: "<id>"
```

# Placeholder Semantics
Fields containing "<id>" or "<self>" are canonical placeholders.  
They MUST be concretised in project/branch/theme/tranche governance envelopes.  
They MUST NOT be replaced in methodology-level contracts.  
The Auditor Persona MUST treat these placeholders as intentional and NOT as metadata drift.
```

---

# Version 2.4 — 2026‑04‑26  
**Status:** Active  
**Scope:** All templates under `/fugue/templates/`  
**Change Type:** Namespace alignment, schema alignment, metadata uplift

## Summary of changes

- Added canonical v2.4 metadata blocks to all templates  
- Added placeholder semantics to all methodology-level templates  
- Updated tranche-folder-template to use canonical category-based namespaces  
- Removed legacy `/implementation/` and `/reconciliation/` namespaces  
- Updated reconciled-decor.md template to use `/fugue_docs/decors/<tranche-name>/`  
- Ensured all templates align with `/schemas/decor-schema.json`  
- Removed conversational wrapper text from governed templates  
- Ensured naming alignment with v2.4 (`T<number>`, `C<number>`, `E<number>`)  

---

# Version 2.3 — 2026‑04‑20  
**Status:** Historical (Legacy)  
**Scope:** Global method alignment for the Fugue Method applied to the `templates` directory.

## Summary of changes

- Unified global versioning: all Fugue artefacts now carried `Version: 2.3`.  
- Deprecated per-file version headers in favour of global method version.  
- Introduced per-folder changelogs.  
- Applied documentation hygiene and path normalisation.  

## Notes

- v2.3 entries are preserved for lineage only.  
- v2.3 templates are archived and MUST NOT be modified.  
```

---