---
id: documentation-standards-v1
version: "1.0.0"
title: Documentation Standards
scope: global
status: active
---

# Documentation Standards

:::rule id="STD-DOC-001" severity="error" category="api-docs" domain="documentation" tags="documentation, api-docs, openapi, specifications"
All APIs shall provide OpenAPI specifications.
:::

:::rule id="STD-DOC-002" severity="error" category="adr" domain="documentation" tags="documentation, adr, architectural, decisions, recorded, adrs"
All major architectural decisions shall be recorded as ADRs in `specs/system/adr/`.
:::

:::rule id="STD-DOC-003" severity="error" category="feature-flags" domain="documentation" tags="documentation, feature-flags, feature, flags, introduced, they"
Where feature flags are introduced, they shall be documented with purpose, rollout plan, and owner.
:::

:::rule id="STD-DOC-004" severity="error" category="api-docs" domain="documentation" tags="documentation, api-docs, documented"
All public APIs shall be documented.
:::

:::rule id="STD-DOC-005" severity="error" category="tutorials" domain="documentation" tags="documentation, tutorials, module, added, how, extend"
When a new module is added, a "How to extend" tutorial shall be provided.
:::

:::rule id="STD-DOC-006" severity="error" category="portal" domain="documentation" tags="documentation, portal, auto-publish, specs, schemas, adrs"
The documentation portal shall auto-publish API specs, schemas, ADRs, and runbooks.
:::
