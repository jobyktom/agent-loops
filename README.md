# Agent Loops

Reusable, low-token agent loops for building SaaS apps consistently.

## Core rule

Do not scaffold from a one-line idea. First create a PRD, then create a unique brand/frontend direction, then build.

```txt
Idea -> PRD -> Unique Design -> Scaffold -> Auth/DB -> Billing -> Analytics -> Testing -> Security -> Deploy
```

## Recommended order

1. `00-idea-to-prd.md`
2. `01-unique-brand-design.md`
3. `02-master-saas-scaffold.md`
4. `03-ui-implementation.md`
5. `04-authjs-prisma.md`
6. `05-billing.md`
7. `06-analytics.md`
8. `07-agent-readiness.md` only if the app exposes APIs or agent workflows
9. `08-marketing.md`
10. `09-testing.md`
11. `10-admin-panel.md` only if admin support is needed in v1
12. `11-email-notifications.md` only if emails are needed in v1
13. `12-security-hardening.md`
14. `13-deployment.md`
15. `14-domain-auth-billing-setup.md` when domain/provider setup is needed
16. `15-self-running-loop-safety.md` only for recurring, scheduled, or autonomous loops

## Standard usage

```txt
Read agent-loops/00-idea-to-prd.md and create a PRD for:

Product idea: [your one-line idea]
Target users: [optional]
Market/country: [optional]
Domain: [optional]
```

Then:

```txt
Read agent-loops/01-unique-brand-design.md and create a unique brand/frontend design system from the PRD.
Avoid generic AI SaaS patterns.
```

Then:

```txt
Read agent-loops/02-master-saas-scaffold.md and scaffold the app from the PRD and brand system.
Build to 90 percent completion. Leave only secrets, provider dashboard setup, and final business edge cases for me.
```

For domain, Auth.js, and billing setup:

```txt
Read agent-loops/14-domain-auth-billing-setup.md and create the setup plan for:

Domain: [domain.com]
App name: [name]
Product idea: [summary]
Currency: GBP
Billing: both
Auth: Auth.js
Payment: Stripe
```

For recurring or autonomous workflows:

```txt
Read agent-loops/15-self-running-loop-safety.md before building the loop.
Define trigger, verifier, state storage, stop rules, budget, and human gates.
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
- Keep v1 small and useful.
- Prefer one clear handoff between loops instead of repeating the full product context each time.
- Use the self-running loop safety file only for recurring, scheduled, or autonomous workflows.
