---
id: documentation-standards-v1
version: "1.0.0"
title: Documentation Standards
scope: global
status: active
---

# Documentation Standards

:::rule id="STD-DOC-001" severity="error" category="api-docs" domain="documentation"
title: OpenAPI Specifications

All APIs shall provide OpenAPI specifications.
:::

:::rule id="STD-DOC-002" severity="error" category="adr" domain="documentation"
title: Architectural Decision Records

All major architectural decisions shall be recorded as ADRs in `specs/system/adr/`.
:::

:::rule id="STD-DOC-003" severity="error" category="feature-flags" domain="documentation"
title: Feature Flag Documentation

Where feature flags are introduced, they shall be documented with purpose, rollout plan, and owner.
:::

:::rule id="STD-DOC-004" severity="error" category="api-docs" domain="documentation"
title: Public API Documentation

All public APIs shall be documented.
:::

:::rule id="STD-DOC-005" severity="error" category="tutorials" domain="documentation"
title: Extension Tutorials

When a new module is added, a "How to extend" tutorial shall be provided.
:::

:::rule id="STD-DOC-006" severity="error" category="portal" domain="documentation"
title: Documentation Portal Auto-Publishing

The documentation portal shall auto-publish API specs, schemas, ADRs, and runbooks.
:::
