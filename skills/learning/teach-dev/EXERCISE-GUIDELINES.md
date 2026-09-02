# Exercise Guidelines

Exercises live in a topic's `exercises/` directory. They do not require a fixed Markdown format: the right artifact may be a source file, a small runnable project, a command sequence, a test, or a task in the learner's agreed project.

## Choosing an artifact

- Default to the smallest isolated artifact that lets the learner practice one capability.
- Use a descriptive, sequentially numbered filename for a single-file exercise, or a numbered directory for a multi-file exercise, such as `0001-parse-config/`.
- Use the learner's real project only when it is part of the mission or they explicitly choose it.
- Follow the project's existing conventions when an exercise belongs in that project.

## Designing practice

- State the task, relevant starting point, and observable success condition in the associated lesson or a short exercise readme when the artifact needs it.
- Make the learner produce or change something; do not use passive reading as an exercise.
- Provide a proportionate verification method: a test, build, command output, observed behavior, explanation, or shared result.
- Keep feedback close to the attempt and make the next corrective action clear when verification fails.
- Avoid scaffolding that completes the meaningful part of the task for the learner.

## Boundaries

- Keep exercises isolated from project source and configuration by default.
- Ask before adding dependencies, changing configuration, using credentials, starting networked services, making destructive changes, or altering `.gitignore`.
- Record only demonstrated learning in `PROGRESS.md` and `learning-records/`; an exercise being created does not count as evidence.
