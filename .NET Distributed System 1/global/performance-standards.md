---
id: performance-standards-v1
version: "1.0.0"
title: Performance Standards
scope: global
status: active
---

# Performance Standards

:::rule id="STD-PERF-001" severity="error" category="latency" domain="performance"
title: API Response Time

All API endpoints shall respond within 200ms under normal load.
:::

:::rule id="STD-PERF-002" severity="error" category="async" domain="performance"
title: Async-First IO Patterns

All IO-bound workloads shall use async-first patterns.
:::

:::rule id="STD-PERF-003" severity="error" category="backpressure" domain="performance"
title: WebSocket Backpressure

Where WebSocket fan-out is used, the system shall implement backpressure strategies.
:::

:::rule id="STD-PERF-004" severity="error" category="resilience" domain="performance"
title: Downstream Call Resilience

All downstream calls shall use timeouts, retries with exponential backoff, and circuit breakers.
:::

:::rule id="STD-PERF-005" severity="error" category="scalability" domain="performance"
title: Load Capacity

The system shall be designed to handle 10× the current user load.
:::

:::rule id="STD-PERF-006" severity="error" category="stateless" domain="performance"
title: Stateless Workloads

All workloads shall be stateless where possible to support horizontal scaling.
:::
