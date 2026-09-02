---
name: practice-recall
description: Strengthen learning through short retrieval-practice rounds and evidence-based feedback. Use only when explicitly invoked to review existing learning material.
---

# Practice Recall

Run a short, effortful recall session that strengthens existing learning. The learner should retrieve and apply ideas before seeing corrections; the goal is durable knowledge, not a score or another explanation.

Use this skill only for an explicit `$practice-recall` request. Ordinary questions or requests to explain material should remain ordinary answers.

## Find the recall context

Prefer an existing learning workspace or topic. When the learner names one, use it as the source of truth. When they do not, look for relevant existing learning workspaces; use an unambiguous match or list multiple plausible matches for the learner to choose. Do not guess.

Read only the artifacts that exist and matter: mission/source, progress, glossary, resources, learning records, lessons, notes, and prior recall history. Support `.teach-dev/`, `.learn-from-docs/`, and future workspace types by adapting to their available state rather than requiring identical layouts.

If no useful workspace exists, allow a standalone session only when the learner supplies the material to review. Do not create a workspace merely for recall.

## Build the recall round

Use the workspace's stored duration preference when present. Otherwise ask for a time budget; if none is supplied, use a brief 5–10 minute round.

Choose a small mixed set of prompts from material that is mission-relevant, introduced, practiced, recently studied, weak, or not yet demonstrated. Combine direct recall with application or comparison prompts when appropriate. Ask one prompt at a time, and do not reveal answers or provide clues before the learner responds.

Collect the whole short round before giving corrections. Do not turn recall into a long quiz or cover material with no connection to the learner's current goal.

## Feedback and revisit guidance

After the round:

1. Identify responses that were accurate and worth retaining.
2. Explain the most important gaps or misconceptions, tied to the workspace's sources or glossary when available.
3. Ask one targeted corrective prompt or suggest one small application task.
4. Suggest a qualitative revisit point without claiming to schedule a reminder: revisit sooner after weak recall, at a normal interval after partial recall, and later after strong recall.

Do not assign a numeric grade. A recall attempt alone is not evidence of mastery.

## Record evidence

For a workspace-aware session, create or update a compact topic-level `RECALL.md` using [RECALL-HISTORY-FORMAT.md](./references/RECALL-HISTORY-FORMAT.md), unless the workspace has a documented conflicting convention. Record the date, concepts tested, outcome, and suggested revisit point; keep it concise.

Update the workspace's progress, glossary, or learning records only when the learner's answers meet that workspace's evidence threshold. Preserve its own status definitions and file conventions. Do not persist history or learning state for standalone sessions.
