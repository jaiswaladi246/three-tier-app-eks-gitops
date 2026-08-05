# Contributing

## Branch naming

Every change is made on a branch off `main` and merged back through a
pull request. Use one of the following prefixes:

- `feat/` a new capability
- `fix/` a correction to something broken
- `chore/` structure, configuration, tooling
- `docs/` documentation and README work
- `ci/` workflow and pipeline changes
- `refactor/` changing shape without changing behaviour

## Commit convention

Follow Conventional Commits: `type(scope): imperative summary`.

    feat(auth): add JWT authentication
    fix(api): resolve null pointer on user lookup

## Pull requests

- Keep pull requests focused on one unit of work
- Explain what changed and why in the description
- Link the related issue with `Closes #<number>`
- Wait for CI to pass before merging
- Squash-merge and delete the branch afterwards
