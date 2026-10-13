# ADR 0001: Build V1 as a single Next.js application

- **Status:** Accepted
- **Date:** 13 October 2026

## Context

ResolveOS needs a web interface, server-side logic (cases, evidence, AI calls), a database, and background work (reminders). A separate backend, worker service, and queue were considered. The product is built by one developer who already works in Next.js and TypeScript, and the goal is a reliable V1, not scale.

## Decision

Build V1 as **one Next.js (App Router) application** with server actions and route handlers for server logic, PostgreSQL via Drizzle ORM, and scheduled jobs for reminders. Keep domain code in separate modules (`src/server/<domain>`) so any part can be extracted into its own service later if real usage requires it.

## Alternatives considered

| Option | Why not now |
|---|---|
| Next.js + separate NestJS API | Two deployables, duplicated types, more setup, with no V1 benefit |
| Next.js + Spring Boot | Different language and tooling; slows learning and iteration |
| Microservices | Operational cost far above V1 needs |

## Consequences

- One repo, one deploy, shared types end to end.
- Server-side authorisation must be enforced in every action and route.
- Long-running work must stay short or move to scheduled jobs; revisit if AI processing outgrows request limits.