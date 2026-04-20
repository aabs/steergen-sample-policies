---
id: testing-standards-v1
version: "1.0.0"
title: Testing Standards (Cross-Cutting)
scope: global
status: active
---

# Testing Standards (Cross-Cutting)

## Coverage & Quality Gates

:::rule id="STD-TST-001" severity="error" category="coverage" domain="testing"
title: Code Coverage Requirement

The combined codebase shall maintain ≥ 85% line and branch coverage for merging and deployment.
:::

:::rule id="STD-TST-002" severity="error" category="quality" domain="testing"
title: Test Execution on Merge

When submitting code for merge, all unit, integration, and end-to-end tests shall pass.
:::

## Test Types

:::rule id="STD-TST-010" severity="error" category="unit-testing" domain="testing"
title: Unit Tests for Business Logic

All business logic shall have unit tests.
:::

:::rule id="STD-TST-011" severity="error" category="integration-testing" domain="testing"
title: Integration Tests for Database Operations

All database operations shall have integration tests.
:::

:::rule id="STD-TST-012" severity="error" category="contract-testing" domain="testing"
title: Contract Tests for API Consumers

Where API consumers exist, the codebase shall include contract tests (Pact).
:::

:::rule id="STD-TST-013" severity="error" category="e2e-testing" domain="testing"
title: End-to-End Tests for Critical Flows

All critical user flows shall have end-to-end tests.
:::

## Test-Driven Development

:::rule id="STD-TST-020" severity="error" category="methodology" domain="testing"
title: Test-First Development

When implementing new functionality, the developer shall write tests before production code.
:::
