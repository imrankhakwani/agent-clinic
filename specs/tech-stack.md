# Tech Stack

## Language

TypeScript, end to end (frontend and backend), consistent with the
`typescript` + `tsc` setup already in this repo's `package.json`.

## Framework recommendation: Next.js (App Router)

Next.js is the recommended framework for AgentClinic.

**Rationale:**

- **One framework, full stack** - Next.js unifies server-side TypeScript with
  the UI dashboard Mary asked for, so there's no separate backend service to
  stand up and keep in sync.
- **Popular and reliable** - it has a huge ecosystem and community, which
  satisfies Mary's ask for "a reliable site with a popular stack."
- **Modern browser support out of the box** - built-in SSR/routing and
  React give Steve's "attractive site that works well with a modern browser"
  a solid foundation.
- **Backend logic included** - API routes / server actions cover the
  ailments, therapies, and booking logic Susan needs, without a separate
  backend framework.

**Alternatives considered and deferred:**

- Express or Fastify + a separate single-page app - more moving pieces than
  this project needs right now.
- NestJS - a heavier, backend-only framework that would still require a
  separate frontend to deliver the dashboard.

## Database: SQLite

AgentClinic uses SQLite for persistence.

- Zero external infrastructure to run or deploy - fits a course/demo project
  where students and conference-booth developers need to get up and running
  quickly.
- Plays well with the small, self-contained scope of AgentClinic's data
  (agents, ailments, therapies, appointments, staff).
- Early phases (per [roadmap.md](roadmap.md)) still use in-memory/seed data;
  SQLite is introduced when the persistence-layer phase begins.

## Open decisions for later passes

The following are intentionally left open and will be decided in a future
pass:

- UI styling approach / component library.
- Authentication strategy.
- Testing framework.
