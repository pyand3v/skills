# Learning Record Format

Learning records live in a topic's `learning-records/` directory and use sequential filenames such as `0001-interfaces-are-contracts.md`. Create the directory only when writing the first record.

They capture decision-grade evidence about what the learner knows and why future teaching should adapt. They complement `PROGRESS.md`: records preserve history, while progress summarizes the current state and next steps.

## Template

```md
# {What was learned or established}

{One to three sentences explaining what the learner demonstrated or disclosed, and why it matters for future sessions.}
```

## Optional sections

Include these only when useful:

- `Status: active` or `Status: superseded by 0004-<slug>` frontmatter when an earlier understanding is replaced.
- **Evidence** describing a completed exercise, correct explanation, successful check, or prior experience.
- **Implications** describing what this enables or rules out in future teaching.

## Rules

- Number each new record one higher than the greatest existing record number.
- Write one for demonstrated non-trivial understanding, stated prior knowledge, corrected misconceptions, or meaningful mission changes.
- Do not write records for material merely covered, glossary definitions, or session-by-session activity.
- Mark contradicted records as superseded rather than deleting them.
