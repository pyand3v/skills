# Conventional Commit Messages

Use the [Conventional Commits 1.0.0 specification](https://www.conventionalcommits.org/en/v1.0.0/) for every commit message.

## Format

```text
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

Use a short, specific description. Add a scope only when it clarifies the affected component, such as `feat(teach-dev): add learning workflow guides`.

## Types

- `feat`: add a new capability.
- `fix`: correct a defect.
- `docs`: change documentation only.
- `refactor`: restructure code without changing behavior.
- `test`: add or update tests.
- `build`: change build tooling or dependencies.
- `ci`: change continuous-integration configuration.
- `chore`: make maintenance changes that do not fit another type.
- `perf`: improve performance.
- `revert`: revert an earlier change; include a `Refs:` footer for the reverted commit when useful.

## Bodies, footers, and breaking changes

- Add a body only when the subject cannot capture important context. Begin it after one blank line.
- Use footers for structured metadata such as `Refs: #123` or `Reviewed-by: Name`.
- Mark a breaking change with `!` immediately before the colon, such as `feat(api)!: remove legacy endpoint`, or with an uppercase `BREAKING CHANGE: {description}` footer. Include the footer when consumers need the migration details.
