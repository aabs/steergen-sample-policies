---
id: testing-standards-v1
version: "1.0.0"
title: Testing Standards (Cross-Cutting)
scope: global
status: active
---

# Testing Standards (Cross-Cutting)

## Coverage & Quality Gates

:::rule id="STD-TST-001" severity="error" category="coverage" domain="testing" tags="testing, coverage, combined, line, merging, deployment"
The combined codebase shall maintain ≥ 85% line and branch coverage for merging and deployment.
:::

:::rule id="STD-TST-002" severity="error" category="quality" domain="testing" tags="testing, quality, submitting, merge, unit, integration"
When submitting code for merge, all unit, integration, and end-to-end tests shall pass.
:::

## Test Types

:::rule id="STD-TST-010" severity="error" category="unit-testing" domain="testing" tags="testing, unit-testing, business, logic, have, unit"
All business logic shall have unit tests.
:::

:::rule id="STD-TST-011" severity="error" category="integration-testing" domain="testing" tags="testing, integration-testing, database, operations, have, integration"
All database operations shall have integration tests.
:::

:::rule id="STD-TST-012" severity="error" category="contract-testing" domain="testing" tags="testing, contract-testing, consumers, exist, contract, tests"
Where API consumers exist, the codebase shall include contract tests (Pact).
:::

:::rule id="STD-TST-013" severity="error" category="e2e-testing" domain="testing" tags="testing, e2e-testing, user, flows, have, end-to-end"
All critical user flows shall have end-to-end tests.
:::

## Test-Driven Development

:::rule id="STD-TST-020" severity="error" category="methodology" domain="testing" tags="testing, methodology, implementing, functionality, write, new"
When implementing new functionality, the developer shall write tests before production code.
:::
