# Mocking boundaries

## When to use a test double

Use a test double at a boundary that is costly, unavailable, non-deterministic, or unsafe to use in a test: a third-party service, clock, random source, operating-system resource, or similar external dependency. For a database, prefer a real disposable test database when that gives better confidence at reasonable cost.

Do not mock modules or classes owned by the system merely to observe how they collaborate. Test their combined behavior through the public seam instead.

## Shape the boundary

Make external dependencies explicit so a test can substitute them. Pass a narrow client, clock, generator, or storage interface into the code rather than constructing a concrete external client deep inside it.

Prefer operation-specific boundary methods over a generic transport wrapper when it keeps the contract clear. A `get_user` or `send_receipt` boundary lets a test provide a small, typed response without conditional request-matching logic.

## Keep doubles honest

Model the behavior your code relies on: the relevant response, error, delay, or time value. Do not assert implementation-only details such as an internal collaborator's call sequence unless that sequence is itself part of the boundary contract.

When practical, cover the boundary adapter separately with an integration or contract test, and keep the application test focused on its observable behavior.
