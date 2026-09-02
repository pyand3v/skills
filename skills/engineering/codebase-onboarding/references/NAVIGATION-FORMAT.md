# NAVIGATION.md Format

`NAVIGATION.md` answers practical “where do I look?” questions for the relevant codebase scope.

## Template

```md
# {Codebase name} Navigation

## Start here
- `{path}` — {why this is the useful first landmark}

## By task
- **{Task or question}**: inspect `{path or symbol}`, then `{next path or symbol}`.

## Conventions
- {Naming, module boundary, configuration, test, or generated-file convention}

## High-signal commands
- `{read-only command}` — {what it reveals}

## Avoid or treat carefully
- `{generated, vendored, legacy, or sensitive area}` — {reason}
```

## Rules

- Include only landmarks that help the stated onboarding goal.
- Distinguish a documented convention from an observed local pattern.
- Do not prescribe mutating commands by default.
