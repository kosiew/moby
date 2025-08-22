# Repository Guidelines

This file collects key conventions contributors should follow when working on this repository.

## Code style
- Format Go source using `gofmt -s`.
- Ensure code passes `golint` and `go vet`, and follow advice from *Effective Go* and *Go Code Review Comments*.
- Comment and document all declarations, even private ones, and keep variable names proportional to their scope.
- Avoid underscores in package names and refrain from creating generic `util` or `helpers` packages.
- All tests should run with `go test` without requiring external tooling.

## Testing
- Before committing, run `make validate` to execute checks for DCO, formatting, vetting, and vendor consistency.
- Run unit tests with `make test-unit`. Add integration tests in `integration/` when behavior changes and run them with `make test-integration`. The full suite is available via `make test`.

## Commit guidelines
- Include a `Signed-off-by:` line in each commit message to satisfy the DCO.
- Reference issues using `Closes #<id>` or `Fixes #<id>` when applicable.
- Do not manually edit the `AUTHORS` file; it is generated from Git history.
- Keep documentation changes in the same pull request as the code they describe and ensure the test suite passes after each commit.

## Documentation
- Documentation in `docs/` is written in Markdown. Update docs alongside code changes.

These guidelines apply to the entire repository.
