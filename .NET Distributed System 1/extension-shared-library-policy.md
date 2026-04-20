---
id: extension-shared-library-policy-v1
version: "1.0.0"
title: Extension & Shared Library Policy
scope: global
status: active
---

# Extension & Shared Library Policy

## Extension Points

:::rule id="STD-EXT-001" severity="error" category="extensibility" domain="extension" tags="extension, extensibility, adding, capability, register, new"
When adding new capability, the developer shall register new modules rather than modifying core logic.
:::

:::rule id="STD-EXT-002" severity="error" category="extensibility" domain="extension" tags="extension, extensibility, approved, mechanisms, ui, module"
The approved extension mechanisms are: UI module loader, event handler registry, API gateway, shared design system, and client SDK.
:::

## Shared Libraries

:::rule id="STD-EXT-010" severity="error" category="libraries" domain="extension" tags="extension, libraries, approved, shared, auth, sdk"
The approved shared libraries are: AuthN/Z SDK, event schema types, dispatcher core, design system, and infrastructure modules.
:::

:::rule id="STD-EXT-011" severity="error" category="libraries" domain="extension" tags="extension, libraries, other, domain-owned, unnecessary, shared"
All other code shall be domain-owned; unnecessary shared libraries shall not be created.
:::
