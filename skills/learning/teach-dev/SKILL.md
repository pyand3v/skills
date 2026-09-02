---
name: teach-dev
description: Teach developer tools, languages, and practices through stateful Markdown lessons and exercises. Use only when explicitly invoked to start or continue deliberate technical learning.
---

# Teach Dev

Teach development and technical topics over multiple sessions. The goal is demonstrated capability, not a long explanation or a generic curriculum.

Use this skill only for an explicit `$teach-dev` request. It covers programming languages, frameworks, tools, workflows, processes, and other developer-facing technical subjects. Ordinary technical questions should remain ordinary answers.

## Teaching workspace

Treat the current repository as a teaching workspace. Persist learning material beneath `.teach-dev/`:

```text
.teach-dev/
  SETTINGS.md
  <topic-slug>/
    MISSION.md
    PROGRESS.md
    GLOSSARY.md
    RESOURCES.md
    learning-records/
      0001-<learning-record>.md
    lessons/
      0001-<lesson>.md
    exercises/
```

`SETTINGS.md` is repository-wide, human-readable operational state. It records confirmed preferences such as whether `.teach-dev/` is tracked in Git, default lesson length, recall preferences, practice location, and command-safety boundaries. Do not put secrets, credentials, or personal data in it. Use [SETTINGS-FORMAT.md](./SETTINGS-FORMAT.md).

Each topic directory holds its own learning state:

- `MISSION.md`: the learner's desired outcome, why it matters, and any target project. Use [MISSION-FORMAT.md](./MISSION-FORMAT.md).
- `PROGRESS.md`: baseline, capabilities marked introduced/practiced/demonstrated, the next 2–4 likely lessons, and the most appropriate next step. Use [PROGRESS-FORMAT.md](./PROGRESS-FORMAT.md).
- `GLOSSARY.md`: canonical terminology the learner has demonstrated understanding of. Use [GLOSSARY-FORMAT.md](./GLOSSARY-FORMAT.md).
- `RESOURCES.md`: trusted sources for the topic, with relevance notes and the lessons that use them. Use [RESOURCES-FORMAT.md](./RESOURCES-FORMAT.md).
- `learning-records/`: numbered records of demonstrated understanding, stated prior knowledge, corrected misconceptions, and meaningful mission changes. Use [LEARNING-RECORD-FORMAT.md](./LEARNING-RECORD-FORMAT.md).
- `lessons/`: compact Markdown lessons, numbered sequentially. Use [LESSON-FORMAT.md](./LESSON-FORMAT.md).
- `exercises/`: isolated runnable examples or practice work when needed. Follow [EXERCISE-GUIDELINES.md](./EXERCISE-GUIDELINES.md).

Create and update files inside `.teach-dev/` as normal teaching output. Ask before editing project source or configuration, adding dependencies, starting networked services, using credentials, performing destructive operations, or changing `.gitignore`. When `SETTINGS.md` is first needed, ask whether `.teach-dev/` should be tracked or ignored. Do not stage or commit anything unless explicitly asked.

Treat a Git preference separately from its effective state. If the learner chooses to ignore `.teach-dev/`, inspect `.gitignore`; when no applicable rule exists, explain that ignoring requires an edit and ask for explicit approval before making it. If they decline, record that ignoring is preferred but not enacted. If they choose to track it, record the preference but do not stage or commit files.

## Start or resume a topic

When the learner invokes the skill with a topic:

1. Look for relevant existing topic directories.
2. If one is an unambiguous match, resume it. If several could match, list them briefly and let the learner choose one or create a new topic. Do not guess.
3. For a new topic, establish the mission, target outcome, available time, preferred depth, and whether to use a real project or isolated exercises. Assess the learner with 2–4 diagnostic questions or a tiny practical task before choosing the first lesson; follow [ASSESSMENT-GUIDELINES.md](./ASSESSMENT-GUIDELINES.md).
4. For a resumed topic, read `MISSION.md`, `PROGRESS.md`, and `SETTINGS.md`; consult the glossary, resources, and learning records needed to understand the learner's current state. Start with 2–3 targeted recall or application prompts unless the learner asks to skip them.

Keep only a short adaptive learning path in `PROGRESS.md`. Revise it as the learner demonstrates understanding or changes their mission; do not commit them to a rigid, long curriculum.

Write a learning record only after evidence of learning, stated prior knowledge, a corrected misconception, or a meaningful mission change. Learning records preserve why future teaching should change; `PROGRESS.md` remains the concise current-state and next-steps summary.

## Lessons and practice

Each lesson teaches one capability and provides one tangible win. Keep it short enough to fit the learner's stated time budget; if they do not provide one, prefer a 10–20 minute lesson.

Write each lesson in Markdown using [LESSON-FORMAT.md](./LESSON-FORMAT.md). It defines the standard teaching flow while allowing sections that add no value for a particular lesson to be omitted.

Explain unfamiliar concepts clearly before using questions to test them. Then use retrieval, application, and immediate feedback to build durable learning. Adapt between direct explanation and Socratic questioning; do not turn a lesson into an interrogation when a clear mental model is needed.

Default to an isolated exercise in `exercises/`. Use the learner's real project only when that project is part of the mission or they choose it. Follow [EXERCISE-GUIDELINES.md](./EXERCISE-GUIDELINES.md) to choose the appropriate artifact and verification. Running read-only checks, builds, or tests is allowed when appropriate; ask before actions with side effects beyond the agreed workspace or project boundary.

Update `PROGRESS.md` only after evidence: a completed exercise, a correct explanation, a successful check, or the learner's explicit confirmation. Apply [ASSESSMENT-GUIDELINES.md](./ASSESSMENT-GUIDELINES.md) and the capability states in [PROGRESS-FORMAT.md](./PROGRESS-FORMAT.md) so reading material is not mistaken for mastery.

## Research and references

For version-sensitive technologies, APIs, tools, libraries, and processes, research current primary sources before teaching: official documentation, specifications, release notes, or maintainers' material. Use other reputable sources when primary sources do not teach the needed idea well. Record sources in `RESOURCES.md` and link them from the relevant lesson.

For stable fundamentals, teach directly when appropriate and state meaningful assumptions. Do not invent version-specific details or present unsupported claims as current fact.

## Completion

When the mission has been met, finish with a short retrieval review and a practical capstone or application task tied to it. Follow [ASSESSMENT-GUIDELINES.md](./ASSESSMENT-GUIDELINES.md), then record demonstrated capabilities and sensible next topics in `PROGRESS.md`.
