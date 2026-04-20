---
id: extension-shared-library-policy-v1
version: "1.0.0"
title: Extension & Shared Library Policy
scope: global
status: active
---

# Extension & Shared Library Policy

## Extension Points

:::rule id="STD-EXT-001" severity="error" category="extensibility" domain="extension"
title: Module Registration for New Capability

When adding new capability, the developer shall register new modules rather than modifying core logic.
:::

:::rule id="STD-EXT-002" severity="error" category="extensibility" domain="extension"
title: Approved Extension Mechanisms

The approved extension mechanisms are: UI module loader, event handler registry, API gateway, shared design system, and client SDK.
:::

## Shared Libraries

:::rule id="STD-EXT-010" severity="error" category="libraries" domain="extension"
title: Approved Shared Libraries

The approved shared libraries are: AuthN/Z SDK, event schema types, dispatcher core, design system, and infrastructure modules.
:::

:::rule id="STD-EXT-011" severity="error" category="libraries" domain="extension"
title: Domain-Owned Code

All other code shall be domain-owned; unnecessary shared libraries shall not be created.
:::
