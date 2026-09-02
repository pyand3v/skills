---
name: explain-back
description: Test a learner's understanding by having them explain a concept, then provide targeted feedback. Use only when explicitly invoked for deliberate retrieval and correction.
---

# Explain Back

Have the learner explain a concept in their own words before giving feedback. The goal is to surface a usable mental model, reinforce what is correct, and correct the smallest meaningful gap or misconception.

Use this skill only for an explicit `$explain-back` request. Ordinary requests for explanation or clarification should remain ordinary answers.

## Find the learning context

Support both workspace-aware and standalone sessions.

- When the learner names an existing learning topic or workspace, use it as the source of truth.
- When they do not name one, look for relevant existing learning workspaces. If one match is clear, use it. If several match, list them briefly and let the learner choose; do not guess.
- Read only the state that exists and is relevant: mission/source, progress, glossary, resources, learning records, notes, or lessons. Do not require identical layouts or invent missing state.
- For future workspace types, inspect their available artifacts and apply the same principle: use demonstrated knowledge, active goals, and documented sources when present.
- If no useful workspace exists, run a standalone session. Do not create a workspace or persist learning state merely for an explain-back exercise.

## Set the prompt

Let the learner name the concept, audience, or explanation mode. Useful modes include explaining to a beginner, to a teammate, or defending a design decision.

If they do not name a concept, choose one tightly scoped, mission-relevant item from material that is introduced, practiced, recently studied, or not yet demonstrated. Ask one prompt at a time.

Use the workspace's stored lesson-duration preference when present. Otherwise ask for a time budget; if the learner gives none, use a brief 5–10 minute exchange.

State the audience and prompt, then invite a complete explanation. Do not reveal the expected answer, lead the learner step by step, or correct them while they are explaining unless they explicitly ask for help.

## Give feedback

After the explanation, compare it against the selected workspace's documented sources, established glossary, and demonstrated state. For a standalone session, use information supplied by the learner; research only when needed to verify an unstable claim or fill a documented source gap.

Classify the explanation without a numeric grade:

- **Clear**: the essential relationships are accurate and sufficient for the chosen audience.
- **Partial**: the core is sound, but an important link, constraint, or example is absent.
- **Misconception**: a claim is materially incorrect or leads to an incorrect conclusion.

Give feedback in this order:

1. Name the accurate ideas worth retaining.
2. Identify the exact missing or incorrect claim, with the relevant source or glossary term when available.
3. Explain the smallest useful correction.
4. Ask one targeted follow-up prompt or suggest one concrete practice action.

Do not inflate a partial explanation into mastery, and do not turn feedback into a long replacement lecture.

## Update learning state

For a workspace-aware session, update only when the learner's explanation supplies meaningful evidence:

- Update progress when an explanation supports an introduced, practiced, or demonstrated status.
- Add or revise a glossary term only after the learner uses it correctly.
- Write a learning record only for demonstrated non-trivial understanding, stated prior knowledge, or a corrected misconception that changes future learning.

Preserve each workspace's own evidence definitions and file conventions. Do not write learning files for a standalone session, or merely because an explain-back session occurred.
