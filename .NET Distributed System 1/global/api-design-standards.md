---
id: api-design-standards-v1
version: "1.0.0"
title: API Design Standards
scope: global
status: active
---

# API Design Standards

## RESTful Conventions

:::rule id="STD-API-001" severity="error" category="design" domain="api"
title: REST Naming and HTTP Status Codes

All API endpoints shall follow REST naming conventions and return appropriate HTTP status codes.
:::

:::rule id="STD-API-002" severity="error" category="errors" domain="api"
title: Problem Details Format

When an API error occurs, the response shall use the Problem Details format (RFC 9457).
:::

:::rule id="STD-API-003" severity="error" category="pagination" domain="api"
title: Pagination Defaults

All paginated endpoints shall default to `pageSize=50` with a maximum of `200`.
:::

:::rule id="STD-API-004" severity="error" category="sorting" domain="api"
title: Sorting Parameter

All sortable endpoints shall accept a `sort` parameter with values `newest` or `oldest`, defaulting to `newest`.
:::

## Idempotency

:::rule id="STD-API-010" severity="error" category="idempotency" domain="api"
title: Idempotency-Key Header

All mutating API endpoints shall require an `Idempotency-Key` request header.
:::

:::rule id="STD-API-011" severity="error" category="idempotency" domain="api"
title: Idempotency-Key Length

The `Idempotency-Key` value shall be ≤ 64 characters (UUID v4 recommended).
:::

:::rule id="STD-API-012" severity="error" category="idempotency" domain="api"
title: Duplicate Idempotency-Key Handling

When a duplicate `Idempotency-Key` is received, the system shall return the original response without reprocessing.
:::

## Versioning & Contracts

:::rule id="STD-API-020" severity="error" category="versioning" domain="api"
title: Explicit API Versioning

All API contracts shall use explicit versioning.
:::

:::rule id="STD-API-021" severity="error" category="contracts" domain="api"
title: OpenAPI as Source of Truth

OpenAPI specifications shall be the source of truth for all API contracts.
:::

:::rule id="STD-API-022" severity="error" category="versioning" domain="api"
title: Breaking Change Versioning

When a breaking change is required, the API shall increment the major version per semantic versioning.
:::

:::rule id="STD-API-023" severity="error" category="deprecation" domain="api"
title: Deprecation Notice

When removing a field or endpoint, the API shall issue a deprecation notice before removal.
:::

:::rule id="STD-API-024" severity="error" category="contracts" domain="api"
title: OpenAPI-First Development

When implementing a new API endpoint, the developer shall create or update the OpenAPI specification before writing code.
:::

:::rule id="STD-API-025" severity="error" category="contracts" domain="api"
title: Event Schema Versioning

All event schemas shall be versioned and treated as first-class API contracts.
:::

## Type Safety

:::rule id="STD-API-030" severity="error" category="types" domain="api"
title: Explicit Type Annotations

All public API methods shall have explicit type annotations (applies to both C# and TypeScript).
:::
