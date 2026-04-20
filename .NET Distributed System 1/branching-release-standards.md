---
id: branching-release-standards-v1
version: "1.0.0"
title: Branching & Release Standards
scope: global
status: active
---

# Branching & Release Standards

## Git Flow

:::rule id="STD-REL-001" severity="error" category="branching" domain="release" tags="release, branching, changes, developed, feature"
All changes shall be developed on feature branches.
:::

:::rule id="STD-REL-002" severity="error" category="branching" domain="release" tags="release, branching, integration"
The `develop` branch shall be used for integration.
:::

:::rule id="STD-REL-003" severity="error" category="branching" domain="release" tags="release, branching, always, at, quality"
The `main` branch shall always be at release quality.
:::

:::rule id="STD-REL-004" severity="error" category="branching" domain="release" tags="release, branching, production, releases, created"
Production releases shall only be created from the `main` branch.
:::

## Code Review

:::rule id="STD-REL-010" severity="error" category="review" domain="release" tags="release, review, submitting, pull, request, obtain"
When submitting a pull request, the developer shall obtain peer review and approval before merging.
:::

:::rule id="STD-REL-011" severity="error" category="review" domain="release" tags="release, review, reviews, evaluate, architecture, security"
Code reviews shall evaluate architecture, security, performance, and test coverage.
:::

## Deployment

:::rule id="STD-REL-020" severity="error" category="deployment" domain="release" tags="release, deployment, feature, flags, they, managed"
Where feature flags are used, they shall be managed via AWS AppConfig.
:::

:::rule id="STD-REL-021" severity="error" category="deployment" domain="release" tags="release, deployment, high-risk, components, deployed, canary"
Where high-risk components are deployed, the deployment shall use canary or blue-green strategy.
:::

:::rule id="STD-REL-022" severity="error" category="deployment" domain="release" tags="release, deployment, deployments, rollback, helm, revisions"
All deployments shall support rollback via Helm revisions.
:::
