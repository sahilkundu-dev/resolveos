# ResolveOS

> From everyday frustration to a resolved outcome.

ResolveOS is a personal problem-resolution assistant. It helps a person turn a messy consumer issue (a delayed refund, a damaged delivery, a billing dispute) into one organised case: evidence, a sourced timeline, a clear next step, and follow-up until closure.

![CI](https://github.com/sahilkundu-dev/resolveos/actions/workflows/ci.yml/badge.svg)

**Status:** Under active development, building V1 one day at a time. India-first.

## Why this exists

When something goes wrong with an order or a service, the facts are scattered across email, chats, screenshots and memory. The hard part is not writing a complaint; it is remembering, proving, and following through. ResolveOS keeps the whole case in one place and always shows where each fact came from.

## Principles

- **You stay in control.** Nothing is sent or filed without your review.
- **Evidence first.** Every fact links back to its source.
- **Honest about uncertainty.** If something is unknown, the app says so.
- **Privacy by default.** Export and delete everything, any time.

## Tech stack

| Layer | Choice |
|---|---|
| App | Next.js (App Router), TypeScript, Tailwind CSS |
| Database | PostgreSQL (Neon) with Drizzle ORM |
| Hosting | Vercel |
| CI | GitHub Actions |

## Getting started

```bash
git clone https://github.com/sahilkundu-dev/resolveos.git
cd resolveos
npm install
npm run dev
```

Open http://localhost:3000.

## Project docs

- [Architecture decisions](docs/adr/)
- [Contributing](CONTRIBUTING.md) | [Security policy](SECURITY.md)

## Roadmap

V1 is being built in small, reviewed steps, each with its own issue, branch, and pull request.

## License

Copyright (c) 2026 Sahil. All rights reserved. See [LICENSE](LICENSE).