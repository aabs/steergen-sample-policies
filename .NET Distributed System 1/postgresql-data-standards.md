---
id: postgresql-data-standards-v1
version: "1.0.0"
title: PostgreSQL / Data Standards
scope: global
status: active
---

# PostgreSQL / Data Standards

## Database Configuration

:::rule id="STD-DB-001" severity="error" category="database" domain="data" tags="data, database, postgresql, persistent, storage"
The system shall use PostgreSQL ≥ 14 for all persistent storage.
:::

:::rule id="STD-DB-002" severity="error" category="database" domain="data" tags="data, database, two, separate, databases, ddt-db"
The system shall maintain two separate databases: `ddt-db` (relational via EF Core) and `events-db` (event store via Marten).
:::

## Schema & Migrations

:::rule id="STD-DB-010" severity="error" category="migrations" domain="data" tags="data, migrations, relational, schema, changes, managed"
All relational schema changes shall be managed through EF Core migrations in the `migrater` project.
:::

:::rule id="STD-DB-011" severity="error" category="data-integrity" domain="data" tags="data, data-integrity, relational, model, enforce, soft-delete"
The relational data model shall enforce soft-delete by setting `is_deleted = true`; hard deletes are not permitted except for regulatory compliance.
:::

## Event Sourcing

:::rule id="STD-DB-020" severity="error" category="events" domain="data" tags="data, events, domain, state, changes, captured"
All domain state changes shall be captured as immutable events in the Marten event store.
:::

:::rule id="STD-DB-021" severity="error" category="messaging" domain="data" tags="data, messaging, wolverine, durable, message, queues"
Wolverine durable message queues shall use PostgreSQL-backed storage.
:::
