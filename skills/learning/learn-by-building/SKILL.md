---
name: learn-by-building
description: Guide deliberate learning through small, verified project increments and durable build records. Use only when explicitly invoked to learn by making a concrete outcome.
---

# Learn by Building

Turn a concrete outcome into a small project-based learning path. The goal is demonstrated capability through an incrementally working artifact, not merely shipping a result or receiving a long tutorial.

Use this skill only for an explicit `$learn-by-building` request. Ordinary implementation requests should remain ordinary implementation work.

## Build workspace

Treat the current repository as the learning workspace. Persist the learning record beneath `.learn-by-building/`:

```text
.learn-by-building/
  SETTINGS.md
  <project-slug>/
    PROJECT.md
    PROGRESS.md
    DECISIONS.md
    increments/
      0001-<increment>.md
    learning-records/
      0001-<learning-record>.md
```

`SETTINGS.md` is repository-wide, human-readable operational state. It records only confirmed preferences such as whether `.learn-by-building/` is tracked in Git and typical session length. Do not put secrets, credentials, or personal data in it. Use `references/SETTINGS-FORMAT.md`.

Each project directory begins with these core artifacts:

- `PROJECT.md`: the intended outcome, project boundary, target location, learning goals, constraints, and observable success criteria. Use `references/PROJECT-FORMAT.md`.
- `PROGRESS.md`: current capabilities, completed increments, the next one or two increments, and blockers. Use `references/PROGRESS-FORMAT.md`.
- `DECISIONS.md`: decisions that matter to future build steps, with their reason and trade-off. Use `references/DECISIONS-FORMAT.md`.
- `increments/`: concise plans and outcomes for completed or actively proposed increments. Use `references/INCREMENT-FORMAT.md`.

Create `learning-records/` only for demonstrated non-trivial understanding, stated prior knowledge, corrected misconceptions, or a material change to the project mission. Use `references/LEARNING-RECORD-FORMAT.md`.

Create and update files inside `.learn-by-building/` as normal learning output. When `SETTINGS.md` is first needed, ask whether `.learn-by-building/` should be tracked or ignored. Keep the preference separate from its effective state: if ignoring requires a `.gitignore` edit, explain that and request explicit approval before editing it. Do not stage or commit anything unless explicitly asked.

The artifact may live in a real project or an isolated location. Ask before creating or editing project source or configuration, adding dependencies, starting networked services, using credentials, making destructive changes, or changing `.gitignore`. Read-only inspection, builds, and tests are allowed when appropriate.

## Start or resume a project

Require a concrete outcome: an artifact to build, an improvement to make, or a bounded behavior to achieve. If the request is broad, help the learner choose a small outcome before creating a project workspace.

1. Look for relevant existing project directories. Resume an unambiguous match. If several could match, list them briefly and let the learner choose one or create a new project.
2. For a new project, establish the outcome, learner's reason for building it, target location or isolated-practice choice, time budget, constraints, and observable success criteria. Ask two to four diagnostic questions or use a tiny task only when it will shape the first increment. Record this in `PROJECT.md` and `PROGRESS.md`.
3. For a resumed project, read `PROJECT.md`, `PROGRESS.md`, `DECISIONS.md`, `SETTINGS.md`, and the relevant latest increment or learning record. Begin with a short recall or inspection prompt unless the learner asks to skip it.

Plan only the next two to four useful increments. Choose the smallest vertical slice that produces observable behavior early; do not write a fixed, end-to-end curriculum. Use the stored duration preference, otherwise ask for a time budget, otherwise prefer a 10–20 minute increment.

## Increment loop

For each increment:

1. State its narrow outcome, capability it practices, boundary, and verification before changing the artifact.
2. Explain only the concepts or decision context needed for this increment.
3. Let the learner make meaningful choices and attempt the work. Provide proportionate guidance; do not silently complete the learning-critical part for them.
4. Verify the stated behavior with an appropriate observable check: a test, build, command output, manual scenario, reviewable diff, or concrete explanation. Follow `references/VERIFICATION-GUIDELINES.md`.
5. Record the increment outcome, evidence, remaining gap, and next smallest step in `increments/` and `PROGRESS.md`. Record important trade-offs in `DECISIONS.md`.

Do not call an increment complete because code was written. Mark a capability **introduced**, **practiced**, or **demonstrated** only with appropriate evidence. A learner's correct explanation, successful application, or verified behavior can be evidence; receiving instructions or copying code is not. Create a learning record only for durable evidence that changes the remaining path.

## Completion

Complete the project learning mission when its agreed success criteria have observable evidence and the learner can explain the important choices. End with a short retrieval or transfer prompt and a final verification. Keep limitations, unresolved risks, and sensible next extensions in `PROGRESS.md`; do not overstate completion when evidence is partial.
