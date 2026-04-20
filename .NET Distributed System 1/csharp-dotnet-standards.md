---
id: csharp-dotnet-standards-v1
version: "1.0.0"
title: C# / .NET Standards
scope: global
status: active
---

# C# / .NET Standards

## Language & Framework

:::rule id="STD-CS-001" category="language" domain="csharp" tags="csharp, language, target, net, sdk, version"
The C# codebase shall target .NET SDK ≥ 10.0 and C# language version ≥ 14.
:::

:::rule id="STD-CS-002" category="language" domain="csharp" tags="csharp, language, file-scoped, namespaces, enforced, editorconfig"
All C# files shall use file-scoped namespaces as enforced by `.editorconfig`.
:::

:::rule id="STD-CS-003" category="language" domain="csharp" tags="csharp, language, enable, nullable, reference, types"
All C# projects shall enable nullable reference types and treat nullable warnings as errors.
:::

:::rule id="STD-CS-004" category="language" domain="csharp" tags="csharp, language, io-bound, operations, async-await"
All IO-bound operations in C# shall use async/await.
:::

:::rule id="STD-CS-005" category="language" domain="csharp" tags="csharp, language, configureawait, calls, relying, default"
The C# codebase shall not use `ConfigureAwait` calls, relying on the default ASP.NET Core synchronisation context.
:::

:::rule id="STD-CS-006" category="language" domain="csharp" tags="csharp, language, directives, commonly, shared, global"
All C# projects shall use global using directives for commonly shared namespaces.
:::

:::rule id="STD-CS-007" category="language" domain="csharp" tags="csharp, language, expression-bodied, members, body, expression"
C# code shall use expression-bodied members where the body is a single expression.
:::

## Architecture & Patterns

:::rule id="STD-CS-010" category="architecture" domain="csharp" tags="csharp, architecture, controllers, thin, delegating, business"
All API controllers shall be thin, delegating business logic to handlers or services.
:::

:::rule id="STD-CS-011" category="architecture" domain="csharp" tags="csharp, architecture, ef, core, entity, configurations"
All EF Core entity configurations shall use the Fluent API (no data annotations for schema configuration).
:::

:::rule id="STD-CS-012" category="architecture" domain="csharp" tags="csharp, architecture, repository, classes, inherit, repositorybase"
All repository classes shall inherit from `RepositoryBase<T>` with soft-delete support.
:::

:::rule id="STD-CS-013" category="architecture" domain="csharp" tags="csharp, architecture, registering, reflection-based, registration, addimplementedinterfaces"
When registering services, the codebase shall use reflection-based registration via `AddImplementedInterfaces<T>`.
:::

:::rule id="STD-CS-014" category="architecture" domain="csharp" tags="csharp, architecture, aspire"
All distributed system shall use the latest stable version of .NET Aspire.
:::

:::rule id="STD-CS-015" category="architecture" domain="csharp" tags="csharp, architecture, aspire"
All distributed system services shall call `builder.AddServiceDefaults()` for OpenTelemetry, health checks, service discovery, and resilience policies.
:::

## Formatting & Linting

:::rule id="STD-CS-020" category="quality" severity="warning" domain="csharp" tags="csharp, quality, committing, run, dotnet, format"
When committing C# code, the developer shall run `dotnet format` and resolve all findings.
:::

:::rule id="STD-CS-021" category="quality" domain="csharp" tags="csharp, quality, have, zero, roslyn, analyser"
The C# codebase shall have zero Roslyn analyser warnings on the `main` branch.
:::

## Testing

:::rule id="STD-CS-030" category="testing" domain="csharp" tags="csharp, testing, test, xunit, framework"
All C# test projects shall use xUnit ≥ 2.9.3 as the test framework.
:::

:::rule id="STD-CS-031" category="testing" domain="csharp" tags="csharp, testing, tests, fact, single-case, theory"
All C# tests shall use `[Fact]` for single-case tests and `[Theory]` for parameterised tests.
:::

:::rule id="STD-CS-032" category="testing" domain="csharp" tags="csharp, testing, tests, xunit, traits, categorisation"
All C# tests shall use xUnit traits for categorisation (`Category=Unit`, `Category=Integration`, `Category=Aspire`).
:::

:::rule id="STD-CS-033" category="testing" domain="csharp" tags="csharp, testing, tests, nsubstitute, mocking, fluentassertions"
All C# tests shall use NSubstitute for mocking and FluentAssertions for assertions.
:::

:::rule id="STD-CS-034" category="testing" domain="csharp" tags="csharp, testing, line, coverage, measured, coverlet"
The C# codebase shall maintain ≥ 85% line and branch coverage as measured by coverlet.
:::

## Package Management

:::rule id="STD-CS-040" category="dependencies" domain="csharp" tags="csharp, dependencies, nuget, package, versions, defined"
All NuGet package versions shall be defined centrally in `Directory.Packages.props`.
:::

:::rule id="STD-CS-041" category="dependencies" domain="csharp" tags="csharp, dependencies, individual, reference, packages, specifying"
Individual C# project files shall reference packages without specifying version numbers.
:::

## Minimum Library Versions

:::rule id="STD-CS-050" category="dependencies" domain="csharp" tags="csharp, dependencies, ef, core"
The codebase shall use EF Core ≥ 9.0.
:::

:::rule id="STD-CS-051" category="dependencies" domain="csharp" tags="csharp, dependencies, marten, event, sourcing"
The codebase shall use Marten ≥ 8.13.2 for event sourcing.
:::

:::rule id="STD-CS-052" category="dependencies" domain="csharp" tags="csharp, dependencies, wolverine, durable, messaging"
The codebase shall use Wolverine ≥ 5.0.0 for durable messaging.
:::

:::rule id="STD-CS-053" category="dependencies" domain="csharp" tags="csharp, dependencies, fluentvalidation, input, validation"
The codebase shall use FluentValidation ≥ 12.0.0 for input validation.
:::
