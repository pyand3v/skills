# SETTINGS.md Format

`SETTINGS.md` is repository-wide operational state for `.teach-dev/`. It records confirmed preferences that should carry across topics. It must not contain secrets, credentials, or personal data.

## Template

```md
# Teach Dev Settings

## Storage
- Preference: {track | ignore | undecided}
- Effective state: {tracked | ignored | no applicable Git rule | not checked}

## Lesson preferences
- Typical duration: {for example, 15 minutes}
- Depth: {overview | practical | in-depth}
- Recall: {for example, begin resumed sessions with prompts}

## Practice
- Default location: {isolated exercises | named project}

## Safety boundaries
- {Commands or project changes that require confirmation}
```

## Rules

- Record only preferences the learner has confirmed; omit unknown fields instead of guessing.
- Keep the Git preference separate from its effective state. A preference to ignore `.teach-dev/` is not effective until an applicable `.gitignore` rule exists.
- Update settings when the learner changes a cross-topic preference.
- Keep topic-specific goals, progress, sources, and learning evidence in that topic's directory instead.
