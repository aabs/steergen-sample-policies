---
id: security-standards-v1
version: "1.0.0"
title: Security Standards
scope: global
status: active
---

# Security Standards

## Authentication & Authorisation

:::rule id="STD-SEC-001" severity="error" category="authentication" domain="security" tags="security, authentication, endpoints, authorisation"
All API endpoints shall require authentication and authorisation.
:::

:::rule id="STD-SEC-002" severity="error" category="authentication" domain="security" tags="security, authentication, jwt-based, short-lived, tokens, key"
The system shall use JWT-based authentication with short-lived tokens and key rotation.
:::

:::rule id="STD-SEC-003" severity="error" category="authorization" domain="security" tags="security, authorization, accounts, roles, principle, least"
All accounts and roles shall follow the principle of least privilege.
:::

## Network Boundaries

:::rule id="STD-SEC-010" severity="error" category="network" domain="security" tags="security, network, dmz-tier, ui-facing, access, databases"
DMZ-tier APIs (UI-facing) shall not access databases directly; they shall proxy requests to secure-tier APIs.
:::

:::rule id="STD-SEC-011" severity="error" category="network" domain="security" tags="security, network, secure-tier, interact, directly, databases"
Only secure-tier APIs shall interact directly with databases.
:::

## Secrets Management

:::rule id="STD-SEC-020" severity="error" category="secrets" domain="security" tags="security, secrets, credentials, stored, aws, manager"
All credentials shall be stored in AWS Secrets Manager or sealed secrets.
:::

:::rule id="STD-SEC-021" severity="error" category="secrets" domain="security" tags="security, secrets, committed, source, configuration"
No secrets shall be committed to source code or configuration files.
:::

:::rule id="STD-SEC-022" severity="error" category="secrets" domain="security" tags="security, secrets, developing, locally, dotnet, user-secrets"
While developing locally, developers shall use `dotnet user-secrets` for credential storage.
:::

## Data Protection

:::rule id="STD-SEC-030" severity="error" category="encryption" domain="security" tags="security, encryption, user, data, encrypted, at"
All user data shall be encrypted at rest and in transit.
:::

:::rule id="STD-SEC-031" severity="error" category="data-classification" domain="security" tags="security, data-classification, data, classification, pii, telemetry"
Data classification (PII, telemetry) shall be respected in logging and storage.
:::
