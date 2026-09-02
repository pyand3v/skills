# Feature Trace Format

Feature traces live in `traces/` and use sequential names such as `0001-user-sign-in.md`. Each trace follows one concrete behavior through inspected code; it is not a speculative call graph.

## Template

```md
# {Feature or behavior}

## Trigger and expected result
{User action, request, job, event, or command and its visible outcome.}

## Trace
1. `{path:symbol}` — {observed role and handoff}
2. `{path:symbol}` — {transformation, decision, or state interaction}
3. `{path:symbol}` — {output or external boundary}

## Relevant state and configuration
- `{path or symbol}` — {what affects this behavior}

## Tests and observability
- `{path or command}` — {what provides evidence about the behavior}

## Open branches and uncertainty
- {A conditional path, uninspected implementation, or inference}
```

## Rules

- Trace a real, scoped behavior; do not summarize every related module.
- Cite paths and symbols at each material handoff.
- State unverified branches as questions rather than filling gaps from convention.
- Record tests as navigation evidence; do not turn the trace into an exercise or require them to be run.
