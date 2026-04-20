---
id: infrastructure-devops-standards-v1
version: "1.0.0"
title: Infrastructure & DevOps Standards
scope: global
status: active
---

# Infrastructure & DevOps Standards

## Containerisation

:::rule id="STD-INF-001" severity="error" category="containers" domain="infrastructure"
title: Dockerfile Requirement

All services shall provide a Dockerfile for containerised deployment.
:::

:::rule id="STD-INF-002" severity="error" category="security" domain="infrastructure"
title: Container Image Scanning

Container images shall be scanned for vulnerabilities before deployment.
:::

## Orchestration

:::rule id="STD-INF-010" severity="error" category="orchestration" domain="infrastructure"
title: Local Development Orchestration

While developing locally, the system shall use .NET Aspire for service orchestration and discovery.
:::

:::rule id="STD-INF-011" severity="error" category="orchestration" domain="infrastructure"
title: Production Kubernetes Deployment

In production, the system shall deploy to Kubernetes with Helm charts.
:::

:::rule id="STD-INF-012" severity="error" category="scaling" domain="infrastructure"
title: Horizontal Scaling Support

The system shall support horizontal scaling via Kubernetes HPA/KEDA.
:::

## Minimum Tool Versions

:::rule id="STD-INF-020" severity="error" category="tools" domain="infrastructure"
title: .NET SDK Version

The development environment shall use .NET SDK ≥ 9.0.
:::

:::rule id="STD-INF-021" severity="error" category="tools" domain="infrastructure"
title: OpenTelemetry SDK Version

The development environment shall use OpenTelemetry SDKs at the latest stable version.
:::

:::rule id="STD-INF-022" severity="error" category="tools" domain="infrastructure"
title: AWS SDK Version

The development environment shall use AWS SDKs at the latest stable version.
:::
