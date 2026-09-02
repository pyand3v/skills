---
name: teach
description: Teach any topic through stateful lessons, practice, and evidence of learning. Use only when explicitly invoked to start or continue deliberate learning.
---

# Teach

Teach a topic over multiple sessions. The goal is demonstrated capability, not a long explanation or a generic curriculum.

Use this skill only for an explicit `$teach` request, or when a documented specialization directs you here. Ordinary questions should remain ordinary answers.

## Teaching workspace

Treat the current repository as a teaching workspace. Persist learning material beneath `.teach/`:

```text
.teach/
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

Use the following private references for the workspace documents and workflow:

- `SETTINGS.md`: read `references/SETTINGS-FORMAT.md`.
- `MISSION.md`: read `references/MISSION-FORMAT.md`.
- `PROGRESS.md`: read `references/PROGRESS-FORMAT.md`.
- `GLOSSARY.md`: read `references/GLOSSARY-FORMAT.md`.
- `RESOURCES.md`: read `references/RESOURCES-FORMAT.md`.
- `learning-records/`: read `references/LEARNING-RECORD-FORMAT.md`.
- `lessons/`: read `references/LESSON-FORMAT.md`.
- `exercises/`: follow `references/EXERCISE-GUIDELINES.md`.

Create and update files inside `.teach/` as normal teaching output. Ask before actions outside the agreed learning workspace that could incur cost, affect other people or systems, use credentials, or be destructive. When `SETTINGS.md` is first needed, ask whether `.teach/` should be tracked or ignored. Do not stage or commit anything unless explicitly asked.

Treat a Git preference separately from its effective state. If the learner chooses to ignore `.teach/`, inspect `.gitignore`; when no applicable rule exists, explain that ignoring requires an edit and ask for explicit approval before making it. If they decline, record that ignoring is preferred but not enacted. If they choose to track it, record the preference but do not stage or commit files.

## Start or resume a topic

When the learner invokes the skill with a topic:

1. Look for relevant existing topic directories.
2. Resume an unambiguous match. If several could match, list them briefly and let the learner choose one or create a new topic.
3. For a new topic, establish the mission, target outcome, available time, preferred depth, and whether to use a real setting or isolated practice. Assess the learner with two to four diagnostic questions or a tiny practical task before choosing the first lesson; follow `references/ASSESSMENT-GUIDELINES.md`.
4. For a resumed topic, read `MISSION.md`, `PROGRESS.md`, and `SETTINGS.md`; consult the glossary, resources, and learning records needed to understand the learner's current state. Start with two or three targeted recall or application prompts unless the learner asks to skip them.

Keep only a short adaptive learning path in `PROGRESS.md`. Write learning records only after evidence of learning, stated prior knowledge, a corrected misconception, or a meaningful mission change.

## Lessons and practice

Each lesson teaches one capability and provides one tangible win. Keep it within the learner's stated time budget; otherwise prefer 10–20 minutes. Write each lesson using `references/LESSON-FORMAT.md`.

Explain unfamiliar concepts clearly before using questions to test them. Use retrieval, application, and immediate feedback to build durable learning. Follow `references/EXERCISE-GUIDELINES.md` to choose an appropriate practice artifact and verification method.

Update `PROGRESS.md` only after evidence: a completed exercise, correct explanation, successful check, or explicit learner confirmation. Apply `references/ASSESSMENT-GUIDELINES.md` and the capability states in `references/PROGRESS-FORMAT.md` so exposure is not mistaken for mastery.

## Research and completion

For claims that depend on current knowledge or an external source, research high-trust, mission-relevant material and record it in `RESOURCES.md`. For stable fundamentals, teach directly when appropriate and state meaningful assumptions.

When the mission has been met, finish with a short retrieval review and a practical capstone or application tied to it. Follow `references/ASSESSMENT-GUIDELINES.md`, then record demonstrated capabilities and sensible next topics in `PROGRESS.md`.
