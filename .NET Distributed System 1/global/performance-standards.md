---
id: performance-standards-v1
version: "1.0.0"
title: Performance Standards
scope: global
status: active
---

# Performance Standards

:::rule id="STD-PERF-001" severity="error" category="latency" domain="performance" tags="performance, latency, endpoints, respond, 200ms, load"
All API endpoints shall respond within 200ms under normal load.
:::

:::rule id="STD-PERF-002" severity="error" category="async" domain="performance" tags="performance, async, io-bound, workloads, async-first, patterns"
All IO-bound workloads shall use async-first patterns.
:::

:::rule id="STD-PERF-003" severity="error" category="backpressure" domain="performance" tags="performance, backpressure, websocket, fan-out, implement, strategies"
Where WebSocket fan-out is used, the system shall implement backpressure strategies.
:::

:::rule id="STD-PERF-004" severity="error" category="resilience" domain="performance" tags="performance, resilience, downstream, calls, timeouts, retries"
All downstream calls shall use timeouts, retries with exponential backoff, and circuit breakers.
:::

:::rule id="STD-PERF-005" severity="error" category="scalability" domain="performance" tags="performance, scalability, designed, handle, current, user"
The system shall be designed to handle 10× the current user load.
:::

:::rule id="STD-PERF-006" severity="error" category="stateless" domain="performance" tags="performance, stateless, workloads, possible, horizontal, scaling"
All workloads shall be stateless where possible to support horizontal scaling.
:::
