---
id: observability-standards-v1
version: "1.0.0"
title: Observability Standards
scope: global
status: active
---

# Observability Standards

## Logging

:::rule id="STD-OBS-001" severity="error" category="logging" domain="observability"
title: Structured JSON Logging

All services shall emit structured JSON logs via `Microsoft.Extensions.Logging` with OpenTelemetry exporters.
:::

:::rule id="STD-OBS-002" severity="error" category="logging" domain="observability"
title: Trace and Span ID Correlation

All log entries shall include trace and span IDs for end-to-end correlation.
:::

:::rule id="STD-OBS-003" severity="error" category="logging" domain="observability"
title: Structured Log Key-Value Pairs

All structured log entries shall use key/value pairs for queryable data.
:::

## Metrics & Tracing

:::rule id="STD-OBS-010" severity="error" category="instrumentation" domain="observability"
title: OpenTelemetry Instrumentation

All services shall be instrumented with OpenTelemetry SDKs for traces and metrics.
:::

:::rule id="STD-OBS-011" severity="error" category="metrics" domain="observability"
title: RED Metrics

All services shall publish RED metrics (Rate, Errors, Duration).
:::

:::rule id="STD-OBS-012" severity="error" category="tracing" domain="observability"
title: Distributed Tracing Propagation

Distributed tracing shall propagate across all service boundaries.
:::

:::rule id="STD-OBS-013" severity="error" category="monitoring" domain="observability"
title: Service Dashboards and SLOs

Each service shall publish a dashboard and define SLOs.
:::

## Health Checks

:::rule id="STD-OBS-020" severity="error" category="health" domain="observability"
title: Health and Readiness Probes

All services shall expose health and readiness probes.
:::

:::rule id="STD-OBS-021" severity="error" category="health" domain="observability"
title: Aspire Default Endpoints

All services shall use Aspire's `MapDefaultEndpoints()` for standard health endpoints.
:::
