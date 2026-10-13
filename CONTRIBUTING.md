# Contributing to ResolveOS

Thanks for your interest. This is currently a solo-built product, but it follows the same workflow a team would.

## Workflow

1. Every change starts from a GitHub issue.
2. Branch from `main` using the pattern `type/short-description`, for example `feat/day-05-case-workspace`.
3. Make small commits using [Conventional Commits](https://www.conventionalcommits.org/):

   | Prefix | Use for |
   |---|---|
   | `feat:` | A new feature |
   | `fix:` | A bug fix |
   | `docs:` | Documentation only |
   | `test:` | Adding or fixing tests |
   | `refactor:` | Code change with no behaviour change |
   | `chore:` | Tooling, config, dependencies |

4. Open a pull request using the template. CI must pass.
5. Squash-merge into `main`. `main` is always deployable.

## Local checks before opening a PR

```bash
npm run lint
npm run typecheck
npm run build
```

## Ground rules

- Never commit secrets. Use `.env.local` (git-ignored) and keep `.env.example` up to date.
- Every route and server action must check authentication and ownership.
- Record significant decisions as a short ADR in `docs/adr/`.