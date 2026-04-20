---
id: typescript-react-standards-v1
version: "1.0.0"
title: TypeScript / React Standards
scope: global
status: active
---

# TypeScript / React Standards

## Language & Framework

:::rule id="STD-TS-001" category="language" domain="typescript" tags="typescript, language, frontend, target, strict, mode"
The frontend shall target TypeScript ≥ 5 with strict mode enabled.
:::

:::rule id="STD-TS-002" category="language" domain="typescript" tags="typescript, language, permit, implicit, types"
The TypeScript codebase shall not permit implicit `any` types.
:::

:::rule id="STD-TS-003" category="framework" domain="typescript" tags="typescript, framework, frontend, react, functional, components"
The frontend shall use React ≥ 19 with functional components exclusively.
:::

:::rule id="STD-TS-004" category="framework" domain="typescript" tags="typescript, framework, react, components, hooks, class"
All React components shall use hooks; class components are not permitted.
:::

:::rule id="STD-TS-005" category="framework" domain="typescript" tags="typescript, framework, react, hooks, declare, exhaustive"
All React hooks shall declare exhaustive dependency arrays.
:::

:::rule id="STD-TS-006" category="build" domain="typescript" tags="typescript, build, frontend, vite, tool"
The frontend shall use Vite ≥ 7 as the build tool.
:::

## Styling

:::rule id="STD-TS-010" category="styling" domain="typescript" tags="typescript, styling, frontend, tailwindcss"
The frontend shall use TailwindCSS for styling.
:::

:::rule id="STD-TS-011" category="styling" domain="typescript" tags="typescript, styling, scss, selectors, exceed, levels"
Where SCSS is used, selectors shall not exceed 3 levels of nesting.
:::

:::rule id="STD-TS-012" category="styling" domain="typescript" tags="typescript, styling, scss, bem, design-system, token-driven"
Where SCSS is used, the codebase shall follow BEM or design-system token-driven naming.
:::

:::rule id="STD-TS-013" category="styling" domain="typescript" tags="typescript, styling, frontend, design, figma-generated, tokens"
The frontend shall use design system and Figma-generated tokens for visual consistency.
:::

## Formatting & Linting

:::rule id="STD-TS-020" category="quality" domain="typescript" tags="typescript, quality, prettier, formatting"
The TypeScript codebase shall use Prettier for code formatting.
:::

:::rule id="STD-TS-021" category="quality" domain="typescript" tags="typescript, quality, eslint, rules"
The TypeScript codebase shall use ESLint ≥ 9 with TypeScript ESLint rules.
:::

:::rule id="STD-TS-022" category="quality" domain="typescript" tags="typescript, quality, scss, exist, stylelint, linting"
Where SCSS files exist, the codebase shall use Stylelint for linting.
:::

:::rule id="STD-TS-023" category="quality" domain="typescript" tags="typescript, quality, committing, frontend, resolve, eslint"
When committing frontend code, the developer shall resolve all ESLint and Prettier findings.
:::

## Testing

:::rule id="STD-TS-030" category="testing" domain="typescript" tags="typescript, testing, frontend, tests, vitest, test"
All frontend tests shall use Vitest ≥ 4.0.3 as the test runner.
:::

:::rule id="STD-TS-031" category="testing" domain="typescript" tags="typescript, testing, frontend, tests, categorised, category"
Frontend tests shall be categorised with `Category=Frontend` and excluded from backend test runs.
:::

## API Client Generation

:::rule id="STD-TS-040" category="api" domain="typescript" tags="typescript, api, frontend, orval, generate, typed"
The frontend shall use Orval to generate typed API clients from OpenAPI specifications.
:::

:::rule id="STD-TS-041" category="api" domain="typescript" tags="typescript, api, openapi, specification, changes, regenerate"
When an OpenAPI specification changes, the developer shall regenerate API clients via `npm run orval:generate`.
:::
