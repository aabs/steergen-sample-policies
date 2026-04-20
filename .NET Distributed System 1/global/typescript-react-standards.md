---
id: typescript-react-standards-v1
version: "1.0.0"
title: TypeScript / React Standards
scope: global
status: active
---

# TypeScript / React Standards

## Language & Framework

:::rule id="STD-TS-001" severity="error" category="language" domain="typescript"
title: TypeScript Version and Strict Mode

The frontend shall target TypeScript ≥ 5 with strict mode enabled.
:::

:::rule id="STD-TS-002" severity="error" category="language" domain="typescript"
title: Implicit Any Types

The TypeScript codebase shall not permit implicit `any` types.
:::

:::rule id="STD-TS-003" severity="error" category="framework" domain="typescript"
title: React Version and Components

The frontend shall use React ≥ 19 with functional components exclusively.
:::

:::rule id="STD-TS-004" severity="error" category="framework" domain="typescript"
title: React Hooks Only

All React components shall use hooks; class components are not permitted.
:::

:::rule id="STD-TS-005" severity="error" category="framework" domain="typescript"
title: Hook Dependency Arrays

All React hooks shall declare exhaustive dependency arrays.
:::

:::rule id="STD-TS-006" severity="error" category="build" domain="typescript"
title: Vite Build Tool

The frontend shall use Vite ≥ 7 as the build tool.
:::

## Styling

:::rule id="STD-TS-010" severity="error" category="styling" domain="typescript"
title: TailwindCSS for Styling

The frontend shall use TailwindCSS for styling.
:::

:::rule id="STD-TS-011" severity="error" category="styling" domain="typescript"
title: SCSS Nesting Depth

Where SCSS is used, selectors shall not exceed 3 levels of nesting.
:::

:::rule id="STD-TS-012" severity="error" category="styling" domain="typescript"
title: SCSS Naming Conventions

Where SCSS is used, the codebase shall follow BEM or design-system token-driven naming.
:::

:::rule id="STD-TS-013" severity="error" category="styling" domain="typescript"
title: Design System Tokens

The frontend shall use design system and Figma-generated tokens for visual consistency.
:::

## Formatting & Linting

:::rule id="STD-TS-020" severity="error" category="quality" domain="typescript"
title: Prettier Code Formatting

The TypeScript codebase shall use Prettier for code formatting.
:::

:::rule id="STD-TS-021" severity="error" category="quality" domain="typescript"
title: ESLint Configuration

The TypeScript codebase shall use ESLint ≥ 9 with TypeScript ESLint rules.
:::

:::rule id="STD-TS-022" severity="error" category="quality" domain="typescript"
title: Stylelint for SCSS

Where SCSS files exist, the codebase shall use Stylelint for linting.
:::

:::rule id="STD-TS-023" severity="error" category="quality" domain="typescript"
title: Linting and Formatting Resolution

When committing frontend code, the developer shall resolve all ESLint and Prettier findings.
:::

## Testing

:::rule id="STD-TS-030" severity="error" category="testing" domain="typescript"
title: Vitest Test Runner

All frontend tests shall use Vitest ≥ 4.0.3 as the test runner.
:::

:::rule id="STD-TS-031" severity="error" category="testing" domain="typescript"
title: Frontend Test Categorisation

Frontend tests shall be categorised with `Category=Frontend` and excluded from backend test runs.
:::

## API Client Generation

:::rule id="STD-TS-040" severity="error" category="api" domain="typescript"
title: Orval for API Client Generation

The frontend shall use Orval to generate typed API clients from OpenAPI specifications.
:::

:::rule id="STD-TS-041" severity="error" category="api" domain="typescript"
title: API Client Regeneration

When an OpenAPI specification changes, the developer shall regenerate API clients via `npm run orval:generate`.
:::
