---
name: tdd
description: Build or fix software through focused red-green-refactor cycles. Use when the user asks for test-driven or explicitly test-first work.
---

# Test-Driven Development

Build requested behavior through short red-green-refactor cycles. The goal is a small, observable change with tests that remain useful when its implementation changes.

Use this skill when the user asks for TDD, a test-first workflow, or red-green-refactor. Ordinary requests to add tests or make a change should follow the project's normal development workflow unless the user asks to work test-first.

## Start with the behavior

Read the relevant code, test conventions, and project guidance. Identify the public interface that will express the requested behavior. If the behavior or its boundary is unclear, resolve that before writing a test.

Choose a seam a caller or user can observe. State it briefly when a feature has several plausible entry points. Do not reach through that boundary to test private methods, internal calls, or storage side effects.

## Red, green, refactor

For each thin, vertical slice of behavior:

1. Write one focused test for the next observable outcome, with an expected value grounded in the specification, a worked example, or another independent source of truth.
2. Run it and confirm that it fails for the behavior being added or corrected.
3. Write the smallest production change that makes it pass.
4. Run the relevant test again. Start the next cycle only after it is green.
5. Refactor only with the tests green, and rerun the relevant suite after the refactor.

Keep each slice small. Do not write a large batch of speculative tests or implementation before checking the first slice. A test that cannot fail meaningfully does not establish the behavior.

## Test design

Tests should describe what a caller can do, use the public interface, and survive an internal refactor that preserves behavior. Name the capability, not an implementation step. Prefer clear setup and one logical outcome per test.

Read [references/test-design.md](references/test-design.md) when designing or reviewing a test, deciding how to verify persistence or effects, or diagnosing brittle and tautological tests.

## External boundaries

Use real collaborators within the system boundary where practical. Replace dependencies at boundaries the code does not control, such as network services, time, randomness, and sometimes the filesystem or database. Keep the fake focused on the boundary contract.

Read [references/mocking.md](references/mocking.md) when the change crosses an external boundary or needs a test double.

## Completion

Run the narrowest relevant tests throughout the loop, then run the repository's required checks when the change is complete. Report the behavior covered and any external boundary that remained simulated.
