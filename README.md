# My Codex Skills

A personal collection of small, composable skills for Codex and compatible coding agents. Each skill captures a workflow or constraint that I want applied consistently, while remaining easy to inspect and adapt.

## Install

Install selected skills with the Skills CLI:

```bash
npx skills@latest add pyand3v/skills
```

Choose the skills and agents in the interactive prompt. For local development, keep this repository cloned and copy or link an individual skill directory into your Codex skills directory.

## Validate skills

Install the validator once with Go:

```bash
go install github.com/pyand3v/skill-validator/cmd/skill-validator@v0.1.0
```

Validate this collection locally:

```bash
skill-validator skills
```

To validate another collection, pass its skills directory instead:

```bash
skill-validator /path/to/skills
```

GitHub Actions runs the same validator for every push and pull request.

## Included skills

| Skill                                                               | Purpose                                                                                     |
| ------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| [`versioning`](skills/engineering/versioning/SKILL.md)              | Inspect Git safely and only stage or commit when explicitly asked.                          |
| [`codebase-onboarding`](skills/engineering/codebase-onboarding/SKILL.md) | Map an unfamiliar codebase through architecture and feature notes.                      |
| [`grilling`](skills/productivity/grilling/SKILL.md)                 | Stress-test a plan or decision through rounds of questions.                                 |
| [`grill-me`](skills/productivity/grill-me/SKILL.md)                 | Start a user-invoked grilling session.                                                      |
| [`teach-dev`](skills/learning/teach-dev/SKILL.md)                  | Learn developer topics through persistent Markdown lessons and practice.                    |
| [`learn-from-docs`](skills/learning/learn-from-docs/SKILL.md)       | Study supplied sources through guided notes and practice.                                    |
| [`explain-back`](skills/learning/explain-back/SKILL.md)             | Test understanding through learner explanations and feedback.                                |
| [`practice-recall`](skills/learning/practice-recall/SKILL.md)       | Strengthen learning through short retrieval-practice rounds.                                 |
| [`learn-by-building`](skills/learning/learn-by-building/SKILL.md)   | Learn through small project increments with observable verification.                         |
| [`teach-math`](skills/learning/teach-math/SKILL.md)                 | Learn mathematical and logical reasoning through guided practice.                            |
| [`to-questionnaire`](skills/productivity/to-questionnaire/SKILL.md) | Turn unanswered decisions into a questionnaire for the person who holds the needed context. |

## Adding a skill

Add each skill as its own directory beneath `skills/`:

```text
skills/
  my-skill/
    SKILL.md
    agents/
      openai.yaml
```

Use lowercase hyphenated names. Keep `SKILL.md` focused on guidance that is specific to the workflow; add `scripts/`, `references/`, or `assets/` only when they directly support repeated work. Group skills in a domain subdirectory once that domain has more than a few related skills.

## Thanks

Thanks to [Matt Pocock](https://github.com/mattpocock) for inspiration and the productivity skills included in this collection.
