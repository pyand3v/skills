# Increment Format

Increment files live in a project's `increments/` directory and use sequential names such as `0001-show-a-greeting.md`. Create the directory when the first increment is proposed or completed.

## Template

```md
# {Increment title}

## Outcome
{The smallest observable behavior this increment should add.}

## Capability
{What the learner practices or learns by making it.}

## Boundary
{What is intentionally included and excluded.}

## Plan
1. {A small learner-facing step.}
2. {Another step only when needed.}

## Verification
{Exact test, command, manual scenario, review, or explanation that will establish the outcome.}

## Result
{Completed | partial | blocked, with observed evidence.}

## Next smallest step
{The next useful action or open question.}
```

## Rules

- Define verification before work starts and record actual evidence afterwards.
- Keep each increment small enough to complete or diagnose in the session budget.
- If an increment is partial or blocked, retain the useful evidence and boundary instead of rewriting history as success.
