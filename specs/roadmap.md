# Roadmap

High-level implementation order, broken into very small phases. Each phase
should be shippable and reviewable on its own before moving to the next.

1. **Project scaffolding** - initialize a Next.js + TypeScript app on top of
   the existing repo setup.
2. **Core data model** - define TypeScript types for `Agent`, `Ailment`,
   `Therapy`, `Appointment`, and `Staff`. No database yet; back it with
   static/seed data.
3. **Read-only "Agents & Ailments" page** - the first vertical slice,
   rendering seed data through a real route end to end.
4. **Read-only Therapies list/detail page.**
5. **Staff dashboard shell** - basic layout/navigation for staff to view
   agents and ailments (auth stubbed out for now).
6. **Agent dashboard shell** - basic layout for an agent to view their own
   ailments and history.
7. **Booking flow** - an agent can request an appointment (still backed by
   in-memory data).
8. **Staff appointment management** - staff can view and approve booked
   appointments.
9. **Persistence layer** - introduce a real database and replace seed data
   (database choice is tracked as an open decision in
   [tech-stack.md](tech-stack.md)).
10. **Authentication & accounts** - real login with role-based access for
    agents vs. staff.
11. **Visual polish & responsiveness** - apply attractive styling and verify
    modern-browser support (Steve's ask).
12. **Reliability hardening** - error handling, logging, and a deployment
    pipeline (Mary's "reliable site").
