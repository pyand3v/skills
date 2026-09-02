---
name: teach-dev
description: Teach developer tools, languages, and practices through stateful lessons and exercises. Use only when explicitly invoked for deliberate technical learning.
---

# Teach Dev

This is the development specialization of `../teach/SKILL.md`. It uses the core teaching workflow and `.teach/` workspace; do not create a separate `.teach-dev/` workspace.

Use this skill only for an explicit `$teach-dev` request about programming languages, frameworks, tools, workflows, processes, or other developer-facing technical subjects. First read the core skill and then apply these development-specific rules. Ordinary technical questions should remain ordinary answers.

## Development-specific research

For version-sensitive technologies, APIs, tools, libraries, and processes, research current primary sources before teaching: official documentation, specifications, release notes, or maintainer material. Use other reputable sources only when primary sources do not explain the needed idea well. Record sources in `RESOURCES.md` and link them from the relevant lesson.

For stable fundamentals, teach directly when appropriate and state meaningful assumptions. Do not present unsupported claims as current implementation details.

## Development-specific practice and safety

- Prefer code, command-line tasks, tests, builds, debugging, reviews, and small working tools when they best demonstrate the mission's capability.
- Follow the target project's conventions when practice belongs in a real repository.
- Ask before editing project source or configuration, adding dependencies, starting networked services, using credentials, performing destructive operations, or changing `.gitignore`.
- Read-only checks, builds, and tests are allowed when appropriate; ask before actions with side effects beyond the agreed exercise or project boundary.
