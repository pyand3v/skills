# DECISIONS.md Format

`DECISIONS.md` retains build choices that affect future increments, so the learner can revisit their reasoning rather than rediscover it.

## Template

```md
# {Project name} Decisions

## {Decision title}
- Decision: {chosen approach}
- Context: {constraint or problem}
- Why: {reason it fits}
- Trade-off: {meaningful cost or alternative declined}
- Evidence: {verification, experiment, or learner rationale}
```

## Rules

- Record decisions with a meaningful alternative or future consequence; do not log routine implementation details.
- Amend a decision when new evidence changes it; retain a concise note explaining the revision.
- Separate confirmed facts from hypotheses that need verification.
