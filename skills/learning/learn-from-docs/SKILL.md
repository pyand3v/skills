---
name: learn-from-docs
description: Guide stateful study of a learner-provided document, chapter, or paper through concise notes and comprehension checks. Use only when explicitly invoked for deliberate source-based learning.
---

# Learn from Docs

Study a learner-provided document, chapter, paper, or documentation section over one or more sessions. The source is the learning anchor; the goal is demonstrated understanding of an agreed scope, not a substitute copy or generic summary.

Use this skill only for an explicit `$learn-from-docs` request. Ordinary requests to summarize or explain a document should remain ordinary answers.

## Study workspace

Treat the current repository as a study workspace. Persist study material beneath `.learn-from-docs/`:

```text
.learn-from-docs/
  SETTINGS.md
  <source-slug>/
    SOURCE.md
    PROGRESS.md
    GLOSSARY.md                 # when terms are demonstrated
    RESOURCES.md                # when supplemental material is used
    SYNTHESIS.md                # when the study is completed or closed
    learning-records/           # when durable evidence is recorded
      0001-<learning-record>.md
    notes/
      0001-<section>.md
```

`SETTINGS.md` is repository-wide, human-readable operational state. It records confirmed preferences such as whether `.learn-from-docs/` is tracked in Git, default session length, and whether retrieval checks are normally enabled. Do not put secrets, credentials, or personal data in it. Use [SETTINGS-FORMAT.md](./SETTINGS-FORMAT.md).

Each source directory begins with these core artifacts:

- `SOURCE.md`: source title, author or publisher when known, URL or local path, edition/version/date when relevant, agreed scope, and the learner's goal. Use [SOURCE-FORMAT.md](./SOURCE-FORMAT.md).
- `PROGRESS.md`: covered sections, takeaways marked introduced/practiced/demonstrated, the next bounded section, and unresolved questions. Use [PROGRESS-FORMAT.md](./PROGRESS-FORMAT.md).
- `notes/`: concise Markdown notes for the studied sections, numbered sequentially. Use [SECTION-NOTE-FORMAT.md](./SECTION-NOTE-FORMAT.md).

Create these additional artifacts only when their stated condition applies:

- `GLOSSARY.md`: canonical terms the learner has demonstrated understanding of. Use [GLOSSARY-FORMAT.md](./GLOSSARY-FORMAT.md).
- `RESOURCES.md`: supplemental sources, with their purpose and the notes they inform. Use [RESOURCES-FORMAT.md](./RESOURCES-FORMAT.md).
- `SYNTHESIS.md`: a concise conclusion when the agreed study scope is complete or the learner closes the study. Use [SYNTHESIS-FORMAT.md](./SYNTHESIS-FORMAT.md).
- `learning-records/`: numbered records of demonstrated understanding, stated prior knowledge, corrected misconceptions, and meaningful scope changes. Use [LEARNING-RECORD-FORMAT.md](./LEARNING-RECORD-FORMAT.md).

Create and update files inside `.learn-from-docs/` as normal study output. Ask before editing project source or configuration, adding dependencies, starting networked services, using credentials, performing destructive operations, or changing `.gitignore`. Do not stage or commit anything unless explicitly asked.

When `SETTINGS.md` is first needed, ask whether `.learn-from-docs/` should be tracked or ignored. Treat that preference separately from its effective state: if ignoring requires a new `.gitignore` rule, explain this and ask for explicit approval before editing `.gitignore`. If the learner declines, record that ignoring is preferred but not enacted.

## Start or resume a study

Require a learner-supplied source or clear source list: a local file, URL, document title and chapter, or paper. If they have only a broad learning goal, ask them to choose material rather than selecting arbitrary sources for them.

When a source is supplied:

1. Look for relevant existing source directories.
2. Resume an unambiguous match. If several could match, list them briefly and let the learner choose one or create a new study. Do not guess.
3. For a new study, establish the learner's goal, exact scope, available time, desired depth, and the source's edition/version/date when that matters. Assess source-specific prior knowledge with proportionate questions or a tiny application task, following [ASSESSMENT-GUIDELINES.md](./ASSESSMENT-GUIDELINES.md). Record this in `SOURCE.md` and `PROGRESS.md`.
4. For a resumed study, read `SOURCE.md`, `PROGRESS.md`, and `SETTINGS.md`; consult the glossary, supplemental resources, and learning records needed to understand the learner's current state. Summarize the state, then begin with a short retrieval check unless the learner asks to skip it.

Work through one bounded section at a time. For a large source, choose a section that fits the learner's session rather than attempting a whole-book or whole-paper summary.

## Study loop

For each section:

1. State the learning objective and source scope.
2. Explain the essential ideas faithfully and concisely.
3. Save notes that capture concepts, relationships, examples, and source citations—not a reproduction of the source.
4. Ask a small number of retrieval or application questions before continuing, unless the learner explicitly asks to skip checks.
5. Use the learner's answers to correct misunderstandings and choose the next section.

Mark a takeaway as **introduced**, **practiced**, or **demonstrated** only with appropriate evidence. Reading or receiving an explanation is not demonstration; a correct explanation, successful application, or completed exercise is. Follow [ASSESSMENT-GUIDELINES.md](./ASSESSMENT-GUIDELINES.md) for proportionate feedback and evidence. Add glossary terms only after correct use. Write a learning record only for demonstrated non-trivial understanding, stated prior knowledge, corrected misconceptions, or a meaningful change to scope; do not use records as a session log.

Keep the learning path short and adaptive. Update `PROGRESS.md` with the next relevant section and open questions rather than prescribing a long, fixed reading plan.

## Sources and quotation

Keep the supplied material central. Supplement it only when clarification, context, or currency is needed, and label supplemental claims and sources clearly. Record supplemental material in `RESOURCES.md`; for unstable technical claims, prefer current official primary sources.

Do not copy large passages or produce notes that substitute for access to a book, paper, article, or documentation. Use concise paraphrase, citations, and only short quotations when necessary for analysis or discussion.

## Completion

Complete a study when the agreed scope is covered, the learner has demonstrated the selected takeaways through recall or application, and `PROGRESS.md` records unresolved questions and sensible next material. Follow [ASSESSMENT-GUIDELINES.md](./ASSESSMENT-GUIDELINES.md), then create `SYNTHESIS.md` using [SYNTHESIS-FORMAT.md](./SYNTHESIS-FORMAT.md). Do not require finishing every page of a large source when that was not the mission.

If the learner explicitly closes a study before the agreed scope is covered, do not mark the mission complete. Create a synthesis that clearly identifies its partial coverage, then record the uncovered scope and the most useful next material in `PROGRESS.md`.
