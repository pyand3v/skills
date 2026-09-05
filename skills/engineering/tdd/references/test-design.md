# Test design

## Choose an observable seam

Exercise behavior through the same public interface a caller uses: a function, command, route, UI action, or other supported entry point. Verify the result through that interface or another defined public read path.

Avoid checking private helpers, internal collaborators, call counts, call order, or raw persistence when the feature can be verified through its public behavior. Those tests turn a refactor into needless test maintenance.

For example, if creating an account makes it retrievable, create it through the supported API and retrieve it through the supported lookup. Do not inspect a database row solely to prove that the write occurred.

## Make the oracle independent

The expected result must be able to disagree with the production code. Use a known literal, a worked-out example, a fixture, a documented rule, or an independent reference calculation.

Do not derive the expected result by repeating the algorithm under test. A test for a total should supply a known input and known answer; it should not reduce the same input in test code and compare one calculation with another.

## Keep tests useful

A durable test:

- names a behavior someone cares about;
- uses only the necessary inputs and setup;
- makes the meaningful outcome obvious;
- fails when that behavior breaks; and
- still passes when implementation details change without changing behavior.

Split tests when they cover different behaviors or failure causes. Multiple related assertions are fine when together they establish one outcome.

## Diagnose a brittle test

Ask whether it would fail after an internal refactor with identical behavior. If yes, move the test outward to a public seam or remove assertions about collaboration details. If it cannot fail when the product behavior is wrong, replace its oracle with an independent expected outcome.
