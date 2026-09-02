---
name: codebase-onboarding
description: Guide durable exploration of an unfamiliar codebase through architecture maps, feature traces, and navigation notes. Use only when explicitly invoked for codebase onboarding.
---

# Codebase Onboarding

Build a useful, revisable understanding of an unfamiliar codebase. The outcome is a concise map that helps someone orient themselves and trace real behavior—not an exhaustive directory listing, an implementation plan, or a code exercise.

Use this skill only for an explicit `$codebase-onboarding` request. Ordinary requests to locate a file, explain a feature, or make a change should remain ordinary work.

## Onboarding workspace

Treat the current repository as the onboarding workspace. Persist notes beneath `.codebase-onboarding/`:

```text
.codebase-onboarding/
  SETTINGS.md
  <codebase-slug>/
    CODEBASE.md
    ARCHITECTURE.md
    NAVIGATION.md
    traces/
      0001-<feature>.md
```

`SETTINGS.md` is repository-wide, human-readable operational state. It records only confirmed preferences such as whether `.codebase-onboarding/` should be tracked in Git and the preferred detail level. Do not put secrets, credentials, or personal data in it. Use `references/SETTINGS-FORMAT.md`.

Each codebase directory contains:

- `CODEBASE.md`: the local target location, repository identity and revision when available, onboarding goal, scope, and known constraints. Use `references/CODEBASE-FORMAT.md`.
- `ARCHITECTURE.md`: a bounded component map, important data/control boundaries, dependencies, and clearly labeled uncertainty. Use `references/ARCHITECTURE-FORMAT.md`.
- `NAVIGATION.md`: high-value directories, entry points, conventions, and “where to look when” guidance. Use `references/NAVIGATION-FORMAT.md`.
- `traces/`: one concise, evidence-backed path for each explored behavior. Use `references/FEATURE-TRACE-FORMAT.md`.

Create and update files inside `.codebase-onboarding/` as normal onboarding output. When `SETTINGS.md` is first needed, ask whether `.codebase-onboarding/` should be tracked or ignored. Keep the preference separate from its effective state: if ignoring needs a `.gitignore` edit, explain that and request explicit approval before changing it. Do not stage or commit anything unless explicitly asked.

## Explore safely

Read the target codebase by default. Inspect files, Git history, tests, configuration, dependency metadata, and documentation as needed to establish a map. Do not edit the target codebase, install dependencies, run services, use credentials, or make network calls unless the learner explicitly asks and the necessary approval is obtained.

Require a target local directory or an unambiguous current repository. If the learner supplies only a remote repository, ask for a local checkout or explicit permission to obtain one; do not clone it by default. For a new onboarding, establish the learner's goal, their role or likely first task, desired detail, and the relevant subsystem or feature. Keep the first pass bounded.

Look for relevant existing onboarding directories. Resume an unambiguous match. If several could match, list them briefly and let the learner choose one or create a new workspace. On resume, read `CODEBASE.md`, `ARCHITECTURE.md`, `NAVIGATION.md`, and relevant traces; confirm whether the target's revision or scope has materially changed before relying on old notes.

## Map and trace

Build understanding from evidence, beginning with the smallest set of files that explain the requested behavior or architectural boundary.

1. Identify the product purpose, runtime or build entry points, major modules, external boundaries, and the ownership of important state. Record only relationships supported by inspected files; mark inferences and unanswered questions.
2. Turn the map into navigation notes that answer practical questions such as where a request enters, where a feature is configured, where tests live, or which module owns a type. Prefer useful landmarks over a complete tree.
3. Trace one concrete behavior at a time from trigger or input through routing, transformation, state or side effects, and visible output. Cite paths and symbols. If a branch is unknown, record the uncertainty rather than inventing continuity.
4. Update the architecture map and navigation notes when a trace contradicts or materially sharpens them. Preserve a concise note about changed understanding rather than silently presenting inference as fact.

Do not create exercises, challenge tasks, implementation work, or test assignments. Explain the map and traces in the learner's terms, answer follow-up questions, and offer the next highest-value feature or boundary to explore when useful.

## Completion and maintenance

An onboarding is sufficiently complete when it answers the learner's stated goal with a navigable architecture map and one or more relevant traces. Keep scope limits, stale areas, and open questions visible in `CODEBASE.md` or the affected notes. On a later revision, revalidate only the parts relevant to the learner's question rather than rebuilding the whole map.
