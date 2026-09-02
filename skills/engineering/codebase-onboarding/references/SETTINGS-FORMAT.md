# SETTINGS.md Format

`SETTINGS.md` is repository-wide operational state for `.codebase-onboarding/`. It records confirmed preferences that carry across onboarding workspaces. It must not contain secrets, credentials, or personal data.

## Template

```md
# Codebase Onboarding Settings

## Storage
- Preference: {track | ignore | undecided}
- Effective state: {tracked | ignored | no applicable Git rule | not checked}

## Onboarding preferences
- Detail: {overview | subsystem | deep trace}
- Notes style: {concise | explanatory}
- Revision handling: {confirm on resume | recheck relevant paths}
```

## Rules

- Record only preferences the learner has confirmed; omit unknown fields.
- A preference to ignore the workspace is not effective until an applicable Git rule exists.
- Keep target-specific identity, scope, and discoveries in that target's directory.
