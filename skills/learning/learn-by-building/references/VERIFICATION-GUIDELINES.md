# Verification Guidelines

Choose the lightest check that directly establishes the increment's claimed behavior.

- Prefer an automated test or build when it exercises the intended behavior reliably.
- Use a manual scenario when automation would exceed the increment's scope; state the input, expected result, and observed result.
- Use a reviewable diff or inspection for configuration, structure, or documentation changes where execution is not meaningful.
- Ask the learner to explain a key choice when the learning mission includes reasoning, not only behavior.
- Treat a failed or inconclusive check as information: record it, narrow the next step, and do not mark the capability demonstrated.

Verification may inspect an existing project, but do not run changes with material side effects without the required approval.
