# Learning Record Format

Learning records live in a source workspace's `learning-records/` directory and use sequential filenames such as `0001-structural-sharing-is-not-copying.md`. Create the directory only when writing the first record.

They preserve durable evidence that should change future study. `PROGRESS.md` summarizes current state and next steps; records retain why that state changed.

## Template

```md
# {What was learned or established}

{One to three sentences explaining what the learner demonstrated, disclosed, or corrected, and why it matters for future study.}
```

## Optional sections

- **Evidence**: a correct explanation, successful application, completed exercise, or stated prior knowledge.
- **Implications**: what this enables, rules out, or changes in the next study step.
- `Status: superseded by 0004-<slug>` when a prior understanding is replaced.

## Rules

- Number each new record one higher than the greatest existing record number.
- Write one only for demonstrated non-trivial understanding, stated prior knowledge, corrected misconceptions, or a meaningful mission/scope change.
- Do not write records for material merely covered, glossary definitions, or routine session activity.
- Mark contradicted records as superseded rather than deleting them.
