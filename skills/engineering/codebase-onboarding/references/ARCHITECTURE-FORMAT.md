# ARCHITECTURE.md Format

`ARCHITECTURE.md` is a concise, evidence-backed map of the parts relevant to the onboarding scope.

## Template

```md
# {Codebase name} Architecture

## System shape
{One short description of the product and its main runtime or build shape.}

## Entry points
- `{path or symbol}` — {what begins here and what it hands off to}

## Components and boundaries
- **{Component}** (`{path}`): {responsibility, inputs, outputs, and key collaborators}

## Data and control flow
{A short path or list connecting the relevant components.}

## External boundaries
- {API, database, file system, queue, third-party service, or build tool and its role}

## Uncertainty and scope limits
- {Unverified relationship, deferred area, or version caveat}
```

## Rules

- Cite paths and symbols for material claims.
- Prefer responsibilities and relationships over a directory inventory.
- Label inference, generated code, and uninspected areas explicitly.
- Update the map when a feature trace materially contradicts it.
