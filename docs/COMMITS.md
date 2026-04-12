# Commit Conventions

Verso follows the [Conventional Commits](https://www.conventionalcommits.org/) specification.

## Format

```
type(scope): description

[optional body]

[optional footer]
```

## Types

| Type       | When to use                                             |
| ---------- | ------------------------------------------------------- |
| `feat`     | A new feature                                           |
| `fix`      | A bug fix                                               |
| `docs`     | Documentation only                                      |
| `chore`    | Maintenance : dependencies, config, tooling             |
| `ci`       | CI/CD pipeline changes                                  |
| `refactor` | Code change that neither fixes a bug nor adds a feature |
| `test`     | Adding or updating tests                                |
| `style`    | Formatting, whitespace : no logic change                |
| `perf`     | Performance improvement                                 |

## Scopes

Use the package or area name as scope:

| Scope    | Meaning                          |
| -------- | -------------------------------- |
| `api`    | Backend (apps/api)               |
| `web`    | Web frontend (apps/web)          |
| `mobile` | Mobile app (apps/mobile)         |
| `shared` | Shared package (packages/shared) |
| `docs`   | Documentation                    |
| `repo`   | Root-level repo config           |

## Examples

```
feat(api): add IGDB search endpoint
fix(web): correct tier drag-and-drop position update
docs: update README with Phase 1 progress
chore(repo): upgrade TypeScript to 5.x
ci: add lint check to PR workflow
refactor(shared): extract algorithm into dedicated module
test(api): add integration tests for work search
feat(api)!: change authentication from JWT to session-based

BREAKING CHANGE: JWT tokens are no longer accepted.
Use session cookies instead.
```

## Rules

1. **Use imperative mood** : "add feature" not "added feature" or "adds feature"
2. **Lowercase** : No capital letter at the start of the description
3. **No period** : Don't end the description with a dot
4. **Keep it short** : Description under 72 characters
5. **One concern per commit** : Don't mix a feature and a refactor in the same commit
6. **Breaking changes** : Add `!` after the type/scope and explain in the footer
