# CODEBASE.md Format

`CODEBASE.md` anchors one onboarding workspace so later maps and traces have a clear target and scope.

## Template

```md
# {Codebase name}

## Target
- Local path: {absolute or repository-relative path}
- Repository: {name or remote when known}
- Revision: {commit, tag, branch, or not checked}

## Onboarding goal
{What the learner needs to understand and why.}

## Scope
- Include: {subsystems, features, or questions}
- Exclude: {intentionally deferred areas}

## Constraints
- {Read-only boundary, available time, access limits, or assumptions}

## Open questions
- {Question requiring more inspection}
```

## Rules

- Record the revision only when it is observed; never imply that notes describe a different revision.
- Keep the scope bounded and revise it when the learner's goal changes.
- Separate observed facts from questions and assumptions.
