# SETTINGS.md Format

`SETTINGS.md` is repository-wide operational state for `.learn-from-docs/`. It records confirmed preferences that should carry across source studies. It must not contain secrets, credentials, or personal data.

## Template

```md
# Learn from Docs Settings

## Storage
- Preference: {track | ignore | undecided}
- Effective state: {tracked | ignored | no applicable Git rule | not checked}

## Study preferences
- Typical duration: {for example, 20 minutes}
- Depth: {overview | conceptual | in-depth}
- Retrieval checks: {for example, after each section unless skipped}

## Source handling
- Supplemental research: {when needed | ask first}
```

## Rules

- Record only preferences the learner has confirmed; omit unknown fields instead of guessing.
- Keep the Git preference separate from its effective state. A preference to ignore `.learn-from-docs/` is not effective until an applicable `.gitignore` rule exists.
- Keep source-specific scope, notes, progress, and learning evidence in that source's directory.
