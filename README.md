# Agent Loops

Reusable, low-token agent loops for building SaaS apps consistently.

## Core rule

Do not scaffold from a one-line idea. First create a PRD, then create a unique brand/frontend direction, then build.

```txt
Idea -> PRD -> Unique Design -> Scaffold -> Auth/DB -> Billing -> Analytics -> Testing -> Security -> Deploy
```

## Recommended core order

1. `00-idea-to-prd-market-research.md`
2. `02a-unique-frontend-brand-design.md`
3. `01-master-saas-scaffold.md`
4. `02-ui-ux-design.md`
5. `03-auth-prisma.md`
6. `05-billing.md`
7. `07-analytics.md`
8. `08-agent-readiness.md` only if the app exposes APIs/agent workflows
9. `09-marketing.md`
10. `10-testing.md`
11. `13-email-notifications.md` only if emails are needed in v1
12. `14-security-hardening.md`
13. `15-deployment.md`
14. `16-domain-auth-billing-setup.md` when domain/provider setup is needed

## Deprecated / do not use directly

These are kept only as pointers for older workflows:

- `04-google-login.md` -> use `03-auth-prisma.md`
- `06-database-seed.md` -> use `03-auth-prisma.md`
- `11-ecommerce-testing.md` -> use `05-billing.md` and `10-testing.md`

## Standard usage

```txt
Read agent-loops/00-idea-to-prd-market-research.md and create a PRD for:

Product idea: [your one-line idea]
Target users: [optional]
Market/country: [optional]
Domain: [optional]
```

Then:

```txt
Read agent-loops/02a-unique-frontend-brand-design.md and create a unique brand/frontend design system from the PRD.
Avoid generic AI SaaS patterns.
```

Then:

```txt
Read agent-loops/01-master-saas-scaffold.md and scaffold the app from the PRD and brand system.
Build to 90 percent completion. Leave only secrets, provider dashboard setup, and final business edge cases for me.
```

For domain, Auth.js, and billing setup:

```txt
Read agent-loops/16-domain-auth-billing-setup.md and create the setup plan for:

Domain: [domain.com]
App name: [name]
Product idea: [summary]
Currency: GBP
Billing: both
Auth: Auth.js
Payment: Stripe
```

## Default stack

- Next.js App Router
- TypeScript
- Tailwind CSS
- shadcn/ui as primitives only
- Auth.js + Google OAuth
- Prisma + PostgreSQL
- Stripe-style subscriptions
- PostHog or GA4
- Playwright
- Vercel / Hostinger VPS / Railway / Render / Docker

## Token-saving guidance

- Run only the loops needed for the current stage.
- Do not paste every loop into the agent at once.
- Do not use deprecated loops.
- Keep v1 small and useful.
- Prefer one clear handoff between loops instead of repeating the full product context each time.
