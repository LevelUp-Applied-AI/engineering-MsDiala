## Pre-PR Checklist

- [ ] Code correctness — The implementation matches the PR title and requirements, and the feature works as expected.
- [ ] Tests passing — All existing tests pass locally, and any new logic includes appropriate test coverage.
- [ ] No regressions — Verified that changes do not break existing functionality.
- [ ] Documentation updated — README and relevant docs reflect any new setup steps, dependencies, or usage changes.
- [ ] Scope is focused — The PR addresses a single concern and does not bundle unrelated changes.
- [ ] No debug artifacts — Removed breakpoint(), temporary print statements, commented debug code, and unused imports.
- [ ] Clean commit history — Commits are meaningful, logically grouped, and clearly described.
- [ ] Environment consistency — Code runs successfully inside the project’s virtual environment.
- [ ] Linting/formatting — Code follows project style guidelines and passes linters (if applicable).
- [ ] Files reviewed — No unintended files (e.g., .venv, cache files, local configs) are included in the PR.