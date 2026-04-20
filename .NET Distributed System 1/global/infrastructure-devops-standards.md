---
id: infrastructure-devops-standards-v1
version: "1.0.0"
title: Infrastructure & DevOps Standards
scope: global
status: active
---

# Infrastructure & DevOps Standards

## Containerisation

:::rule id="STD-INF-001" severity="error" category="containers" domain="infrastructure" tags="infrastructure, containers, dockerfile, containerised, deployment"
All services shall provide a Dockerfile for containerised deployment.
:::

:::rule id="STD-INF-002" severity="error" category="security" domain="infrastructure" tags="infrastructure, security, container, images, scanned, vulnerabilities"
Container images shall be scanned for vulnerabilities before deployment.
:::

## Orchestration

:::rule id="STD-INF-010" severity="error" category="orchestration" domain="infrastructure" tags="infrastructure, orchestration, developing, locally, net, aspire"
While developing locally, the system shall use .NET Aspire for service orchestration and discovery.
:::

:::rule id="STD-INF-011" severity="error" category="orchestration" domain="infrastructure" tags="infrastructure, orchestration, production, deploy, kubernetes, helm"
In production, the system shall deploy to Kubernetes with Helm charts.
:::

:::rule id="STD-INF-012" severity="error" category="scaling" domain="infrastructure" tags="infrastructure, scaling, horizontal, kubernetes, hpa-keda"
The system shall support horizontal scaling via Kubernetes HPA/KEDA.
:::

## Minimum Tool Versions

:::rule id="STD-INF-020" severity="error" category="tools" domain="infrastructure" tags="infrastructure, tools, development, environment, net, sdk"
The development environment shall use .NET SDK ≥ 9.0.
:::

:::rule id="STD-INF-021" severity="error" category="tools" domain="infrastructure" tags="infrastructure, tools, development, environment, opentelemetry, sdks"
The development environment shall use OpenTelemetry SDKs at the latest stable version.
:::

:::rule id="STD-INF-022" severity="error" category="tools" domain="infrastructure" tags="infrastructure, tools, development, environment, aws, sdks"
The development environment shall use AWS SDKs at the latest stable version.
:::
