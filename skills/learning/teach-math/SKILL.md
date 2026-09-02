---
name: teach-math
description: Teach mathematical and logical concepts through stateful lessons, worked reasoning, and progressively independent practice. Use only when explicitly invoked for deliberate math learning.
---

# Teach Math

This is the mathematics and logic specialization of `../teach/SKILL.md`. It uses the core teaching workflow and `.teach/` workspace; do not create a separate `.teach-math/` workspace.

Use this skill only for an explicit `$teach-math` request about mathematical, statistical, logical, or proof-oriented concepts. Ordinary calculations, one-off proofs, or answer checks should remain ordinary responses unless the learner asks for deliberate instruction.

## Mathematical learning setup

First read the core `teach` skill, then apply these rules. Clarify the learner's target capability: compute, model, reason formally, prove, interpret, or critique. Establish prerequisites and desired formality with proportionate diagnostic questions or a small problem before selecting the first lesson.

Keep definitions, notation, assumptions, domains, and edge cases explicit. Introduce notation only after its role is clear; distinguish an intuitive model from a formal statement. When a claim needs conditions, make those conditions visible rather than teaching a misleading shortcut.

For externally sourced, notation-dependent, or current material, use high-trust sources and record them in the shared `RESOURCES.md`. Stable fundamentals may be taught directly when their assumptions are clear.

## Explain, practice, and assess

Follow `references/MATH-PRACTICE-GUIDELINES.md` for the math-specific teaching loop.

- Start with a worked example that exposes decisions and intermediate reasoning, not just the final answer.
- Then fade support: a near-transfer problem with prompts, followed by an independent problem or explanation when appropriate.
- Use counterexamples or boundary cases when they clarify the limits of a definition, theorem, heuristic, or proof technique.
- For proofs, have the learner state an outline or write an argument, identify the exact claim and assumptions, then diagnose unsupported steps, missing cases, invalid implications, or notation ambiguity before suggesting a repair.
- For computations, ask for enough intermediate work to identify the method and error source; use symbolic or numerical tools as a check when useful, not as a substitute for reasoning.

Give feedback on the reasoning, not only correctness. A correct answer by luck or copied pattern is not evidence of a demonstrated capability. Mark a capability in the shared `PROGRESS.md` as introduced, practiced, or demonstrated only according to the core assessment rules and observable work.

Keep difficulty adaptive: change one meaningful dimension at a time—numbers, representation, constraints, abstraction, or proof independence. If an attempt fails, isolate the smallest misconception or missing subskill, give a corrected example or prompt, and retry with a comparable problem rather than jumping ahead.

## Completion

For a completed math topic, use a short retrieval review plus a transfer problem, proof critique, modeling choice, or application fitting the mission. Have the learner explain the assumptions and why their method applies. Record unresolved conditions, common confusions, and sensible next concepts in the shared workspace rather than claiming blanket mastery.
