---
id: cicd-standards-v1
version: "1.0.0"
title: CI/CD Standards
scope: global
status: active
---

# CI/CD Standards

## Pre-Commit

:::rule id="STD-CI-001" severity="error" category="pre-commit" domain="cicd"
title: Git Pre-Commit Hooks

All repositories shall use git pre-commit hooks to check code quality before commits.
:::

## Pipeline Gates

:::rule id="STD-CI-010" severity="error" category="pipeline" domain="cicd"
title: Pipeline Execution Stages

When a pipeline runs, it shall execute the following stages in order and all shall pass before merge or deployment:
1. Restore and build (fail on warnings on `main`).
2. Lint and analyse (Roslyn analysers, ESLint, Stylelint).
3. Test (unit, integration, contract) with coverage enforcement.
4. Format check (`dotnet format`, Prettier).
5. Type check (TypeScript strict, C# nullable).
6. Security scan (dependency and container scanning).
7. SBOM generation.
8. Static asset audit (bundle size, accessibility).
9. Code complexity checks.
:::
