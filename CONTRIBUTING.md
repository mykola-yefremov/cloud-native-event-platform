# Contributing

## Branch Model

We use a `main` + `develop` workflow.

- `main`: release-only, stable branch.
- `develop`: integration branch for completed feature work.
- `feature/*`: short-lived branches for implementation, merged into `develop` via Pull Request.

## Commit Style

Use Conventional Commits:

- `feat: ...` for new functionality
- `fix: ...` for bug fixes
- `docs: ...` for documentation changes
- `test: ...` for test-related changes
- `refactor: ...` for refactoring without behavior changes
- `chore: ...` for maintenance/config tasks
- `ci: ...` for CI/CD pipeline changes

Rules:
- Keep commits atomic (one logical change per commit).
- Use clear, specific commit messages.
- Avoid generic messages like `update` or `fix stuff`.

## Pull Request Rules

- Open PRs from `feature/*` into `develop`.
- Keep PR scope focused and small enough to review.
- Ensure required status checks are green before merge.
- Resolve all conversations before merge.
- Use `Squash and merge` by default to keep history clean.

## Basic PR Checklist

- [ ] Branch is up to date with `develop`
- [ ] Commit messages follow Conventional Commits
- [ ] No secrets or credentials are included
- [ ] Documentation updated if behavior changed
- [ ] CI checks are green
