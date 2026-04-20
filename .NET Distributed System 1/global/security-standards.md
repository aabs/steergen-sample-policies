---
id: security-standards-v1
version: "1.0.0"
title: Security Standards
scope: global
status: active
---

# Security Standards

## Authentication & Authorisation

:::rule id="STD-SEC-001" severity="error" category="authentication" domain="security"
title: API Endpoint Authentication

All API endpoints shall require authentication and authorisation.
:::

:::rule id="STD-SEC-002" severity="error" category="authentication" domain="security"
title: JWT-Based Authentication

The system shall use JWT-based authentication with short-lived tokens and key rotation.
:::

:::rule id="STD-SEC-003" severity="error" category="authorization" domain="security"
title: Principle of Least Privilege

All accounts and roles shall follow the principle of least privilege.
:::

## Network Boundaries

:::rule id="STD-SEC-010" severity="error" category="network" domain="security"
title: DMZ API Database Access

DMZ-tier APIs (UI-facing) shall not access databases directly; they shall proxy requests to secure-tier APIs.
:::

:::rule id="STD-SEC-011" severity="error" category="network" domain="security"
title: Secure-Tier Database Access

Only secure-tier APIs shall interact directly with databases.
:::

## Secrets Management

:::rule id="STD-SEC-020" severity="error" category="secrets" domain="security"
title: Credential Storage

All credentials shall be stored in AWS Secrets Manager or sealed secrets.
:::

:::rule id="STD-SEC-021" severity="error" category="secrets" domain="security"
title: No Secrets in Source Code

No secrets shall be committed to source code or configuration files.
:::

:::rule id="STD-SEC-022" severity="error" category="secrets" domain="security"
title: Local Development Secrets

While developing locally, developers shall use `dotnet user-secrets` for credential storage.
:::

## Data Protection

:::rule id="STD-SEC-030" severity="error" category="encryption" domain="security"
title: Data Encryption

All user data shall be encrypted at rest and in transit.
:::

:::rule id="STD-SEC-031" severity="error" category="data-classification" domain="security"
title: Data Classification in Logging

Data classification (PII, telemetry) shall be respected in logging and storage.
:::
