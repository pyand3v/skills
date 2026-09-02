# SETTINGS.md Format

`SETTINGS.md` is repository-wide operational state for `.learn-by-building/`. It records confirmed preferences that should carry across build projects. It must not contain secrets, credentials, or personal data.

## Template

```md
# Learn by Building Settings

## Storage
- Preference: {track | ignore | undecided}
- Effective state: {tracked | ignored | no applicable Git rule | not checked}

## Learning preferences
- Typical increment duration: {for example, 20 minutes}
- Guidance: {Socratic | collaborative | direct when blocked}
- Recall prompt on resume: {enabled | disabled}
```

## Rules

- Record only preferences the learner has confirmed; omit unknown fields.
- A preference to ignore the workspace is not effective until an applicable Git rule exists.
- Keep project-specific requirements, choices, and evidence in that project's directory.
