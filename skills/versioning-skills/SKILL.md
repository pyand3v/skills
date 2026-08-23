---
name: versioning-skills
description: Safe Git assistance for this repository. Inspect changes by default; stage and commit only when the user explicitly asks, without changing branches or rewriting history.
---

# Safe Git Workflow

Use Git to inspect and, when explicitly authorized, record work in this repository. Preserve the user's branch and history.

## Scope and invariants

- Operate only in this existing Git repository. Use `git rev-parse --show-toplevel` to verify it.
- Stay on the branch that is checked out when the request begins. A normal, user-requested commit advances that branch's `HEAD`; do not otherwise change its branch or commit.
- Never run `git init`, `git checkout`, `git switch`, `git rebase`, `git merge`, `git reset`, `git restore`, `git clean`, `git branch -d`, `git branch -D`, `git fetch`, `git pull`, `git push`, or `git config --global` unless the user explicitly asks for that exact action and the host's safety rules allow it.
- Never create or delete branches, alter remotes, change Git configuration, or initialize a repository as part of this skill.
- Never use `git add .` or stage every changed file by default. Stage only the specific paths or hunks relevant to the user's requested commit.
- Do not create changelogs, comparison files, commits, tags, or backups unless the user asks.

## Default: inspect only

Use read-only commands to answer questions about repository state:

- `git status --short`
- `git diff` and `git diff --cached`
- `git log --oneline`
- `git diff --stat`, `git show`, and `git blame`

Summarize the result clearly. Do not turn inspection into a write action.

## Staging

Stage changes only when the user explicitly asks to stage them. Before staging:

1. Inspect `git status` and the relevant diff.
2. Identify the exact paths or hunks that belong to the requested change.
3. Preserve unrelated and pre-existing user changes.
4. Stage only those selected paths or hunks.

If the intended scope is unclear, ask the user rather than staging broadly.

## Committing

Create a commit only when the user explicitly asks. Before committing:

1. Review the staged diff and current branch.
2. Confirm that the staged change matches the user's intent.
3. Use the user's requested message, or propose one and obtain approval when needed.
4. Create one normal commit on the current branch with no history rewrite or branch switch.

Do not commit automatically after edits or after each logical change.

## Reverting and experiments

Do not discard work, rewrite commits, create branches, merge branches, or delete branches automatically. Explain safer options such as `git revert` when the user asks, then request explicit direction before any state-changing or destructive Git command.

Keep experiments on the already checked-out branch unless the user explicitly directs a branch operation.

## Verification

After a user-requested staging or commit action, report the resulting status and commit ID. Do not push or otherwise contact a remote unless the user explicitly asks.
