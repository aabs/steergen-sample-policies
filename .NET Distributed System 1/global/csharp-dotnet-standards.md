---
id: csharp-dotnet-standards-v1
version: "1.0.0"
title: C# / .NET Standards
scope: global
status: active
---

# C# / .NET Standards

## Language & Framework

:::rule id="STD-CS-001" severity="error" category="language" domain="csharp"
title: .NET SDK and C# Version Target

The C# codebase shall target .NET SDK ≥ 9.0 and C# language version ≥ 13.
:::

:::rule id="STD-CS-002" severity="error" category="language" domain="csharp"
title: File-Scoped Namespaces

All C# files shall use file-scoped namespaces as enforced by `.editorconfig`.
:::

:::rule id="STD-CS-003" severity="error" category="language" domain="csharp"
title: Nullable Reference Types

All C# projects shall enable nullable reference types and treat nullable warnings as errors.
:::

:::rule id="STD-CS-004" severity="error" category="language" domain="csharp"
title: Async/Await for IO Operations

All IO-bound operations in C# shall use async/await.
:::

:::rule id="STD-CS-005" severity="error" category="language" domain="csharp"
title: ConfigureAwait Usage

The C# codebase shall not use `ConfigureAwait` calls, relying on the default ASP.NET Core synchronisation context.
:::

:::rule id="STD-CS-006" severity="error" category="language" domain="csharp"
title: Global Using Directives

All C# projects shall use global using directives for commonly shared namespaces.
:::

:::rule id="STD-CS-007" severity="error" category="language" domain="csharp"
title: Expression-Bodied Members

C# code shall use expression-bodied members where the body is a single expression.
:::

## Architecture & Patterns

:::rule id="STD-CS-010" severity="error" category="architecture" domain="csharp"
title: Thin API Controllers

All API controllers shall be thin, delegating business logic to handlers or services.
:::

:::rule id="STD-CS-011" severity="error" category="architecture" domain="csharp"
title: EF Core Fluent API

All EF Core entity configurations shall use the Fluent API (no data annotations for schema configuration).
:::

:::rule id="STD-CS-012" severity="error" category="architecture" domain="csharp"
title: Repository Base Class

All repository classes shall inherit from `RepositoryBase<T>` with soft-delete support.
:::

:::rule id="STD-CS-013" severity="error" category="architecture" domain="csharp"
title: Reflection-Based Service Registration

When registering services, the codebase shall use reflection-based registration via `AddImplementedInterfaces<T>`.
:::

:::rule id="STD-CS-014" severity="error" category="architecture" domain="csharp"
title: Service Defaults Registration

All services shall call `builder.AddServiceDefaults()` for OpenTelemetry, health checks, service discovery, and resilience policies.
:::

## Formatting & Linting

:::rule id="STD-CS-020" severity="error" category="quality" domain="csharp"
title: Code Formatting

When committing C# code, the developer shall run `dotnet format` and resolve all findings.
:::

:::rule id="STD-CS-021" severity="error" category="quality" domain="csharp"
title: Roslyn Analyzer Warnings

The C# codebase shall have zero Roslyn analyser warnings on the `main` branch.
:::

## Testing

:::rule id="STD-CS-030" severity="error" category="testing" domain="csharp"
title: xUnit Test Framework

All C# test projects shall use xUnit ≥ 2.9.3 as the test framework.
:::

:::rule id="STD-CS-031" severity="error" category="testing" domain="csharp"
title: xUnit Test Attributes

All C# tests shall use `[Fact]` for single-case tests and `[Theory]` for parameterised tests.
:::

:::rule id="STD-CS-032" severity="error" category="testing" domain="csharp"
title: xUnit Test Categorisation

All C# tests shall use xUnit traits for categorisation (`Category=Unit`, `Category=Integration`, `Category=Aspire`).
:::

:::rule id="STD-CS-033" severity="error" category="testing" domain="csharp"
title: Mocking and Assertion Libraries

All C# tests shall use NSubstitute for mocking and FluentAssertions for assertions.
:::

:::rule id="STD-CS-034" severity="error" category="testing" domain="csharp"
title: Code Coverage Requirement

The C# codebase shall maintain ≥ 85% line and branch coverage as measured by coverlet.
:::

## Package Management

:::rule id="STD-CS-040" severity="error" category="dependencies" domain="csharp"
title: Centralized Package Versions

All NuGet package versions shall be defined centrally in `Directory.Packages.props`.
:::

:::rule id="STD-CS-041" severity="error" category="dependencies" domain="csharp"
title: Project File Package References

Individual C# project files shall reference packages without specifying version numbers.
:::

## Minimum Library Versions

:::rule id="STD-CS-050" severity="error" category="dependencies" domain="csharp"
title: Entity Framework Core Version

The codebase shall use EF Core ≥ 9.0.
:::

:::rule id="STD-CS-051" severity="error" category="dependencies" domain="csharp"
title: Marten Event Sourcing Version

The codebase shall use Marten ≥ 8.13.2 for event sourcing.
:::

:::rule id="STD-CS-052" severity="error" category="dependencies" domain="csharp"
title: Wolverine Messaging Version

The codebase shall use Wolverine ≥ 5.0.0 for durable messaging.
:::

:::rule id="STD-CS-053" severity="error" category="dependencies" domain="csharp"
title: FluentValidation Version

The codebase shall use FluentValidation ≥ 12.0.0 for input validation.
:::
