# StreetFood OS — Bolt migration handoff

The source of truth remains the Lovable project until the complete source tree is transferred.

## Source project
- Lovable project: https://lovable.dev/projects/72bc13bb-e158-425d-b00a-69a6c67555e3
- Source commit inspected: a374de922e75058fae5d5be9af3ee8ee27aa2009
- Stack: React 19, TypeScript, TanStack Start/Router, Vite 8, Tailwind CSS 4
- Existing backend: Supabase (keep this project; do not provision a replacement)

## Migration status
- GitHub write access has been verified.
- Baseline .gitignore is committed.
- The complete application source has NOT yet been transferred.
- No Supabase schema or production data has been changed.
- Do not treat this repository as a runnable application until the full source tree and required assets are present.

## Required next steps
1. Transfer all text source files, configuration, lockfile, route files, and binary assets from the inspected Lovable commit.
2. Verify no credentials or environment secrets are included.
3. Install dependencies and run lint, tests, and production build; resolve all failures before deployment.
4. Import this repository into Bolt.new and preserve the existing Supabase project.
5. Audit the demo/localStorage flows and implement real Supabase Auth, organization-scoped persistence, RLS, realtime kitchen updates, server-side pricing, payment webhook signature verification and idempotency.
6. Use test organizations and test payment credentials for staging and load tests. Never load-test real payment flows or production customer data.

## Important
The current demo implementation is not production-ready multi-tenant SaaS. A successful GitHub connection or Bolt import does not itself make it production-ready.
