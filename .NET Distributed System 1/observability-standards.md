---
id: observability-standards-v1
version: "1.0.0"
title: Observability Standards
scope: global
status: active
---

# Observability Standards

## Logging

:::rule id="STD-OBS-001" category="logging" domain="observability" tags="observability, logging, emit, structured, json, logs"
All services shall emit structured JSON logs via `Microsoft.Extensions.Logging` with OpenTelemetry exporters.
:::

:::rule id="STD-OBS-002" category="logging" domain="observability" tags="observability, logging, log, entries, trace, span"
All log entries shall include trace and span IDs for end-to-end correlation.
:::

:::rule id="STD-OBS-003" category="logging" domain="observability" tags="observability, logging, structured, log, entries, key-value"
All structured log entries shall use key/value pairs for queryable data.
:::

## Metrics & Tracing

:::rule id="STD-OBS-010" category="instrumentation" domain="observability" tags="observability, instrumentation, instrumented, opentelemetry, sdks, traces"
All services shall be instrumented with OpenTelemetry SDKs for traces and metrics.
:::

:::rule id="STD-OBS-011" category="metrics" domain="observability" tags="observability, metrics, publish, red, rate, errors"
All services shall publish RED metrics (Rate, Errors, Duration).
:::

:::rule id="STD-OBS-012" category="tracing" domain="observability" tags="observability, tracing, distributed, propagate, across, boundaries"
Distributed tracing shall propagate across all service boundaries.
:::

:::rule id="STD-OBS-013" category="monitoring" domain="observability" tags="observability, monitoring, publish, dashboard, define, slos"
Each service shall publish a dashboard and define SLOs.
:::

## Health Checks

:::rule id="STD-OBS-020" category="health" domain="observability" tags="observability, health, expose, readiness, probes"
All services shall expose health and readiness probes.
:::

:::rule id="STD-OBS-021" category="health" domain="observability" tags="observability, health, aspire, mapdefaultendpoints, standard, endpoints"
All services shall use Aspire's `MapDefaultEndpoints()` for standard health endpoints.
:::
