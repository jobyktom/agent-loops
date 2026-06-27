# Agent Loops

Reusable agent prompt loops for scaffolding SaaS applications quickly and consistently.

These loops are designed for Codex, Claude Code, ChatGPT agents, or any coding assistant that can read project files and execute structured tasks.

## Recommended flow

Do not start from code. Start from the product idea, convert it into a PRD, create a unique brand/design direction, then scaffold.

```txt
One-line idea -> PRD + market check -> unique brand/frontend design -> SaaS scaffold -> auth -> billing -> analytics -> testing -> deployment
```

## How to use

Copy this repository or the `agent-loops/` folder into any new SaaS project.

For a new product idea, ask your agent:

```txt
Read agent-loops/00-idea-to-prd-market-research.md and create a PRD for this SaaS idea:

Product idea: [PASTE YOUR ONE-LINE SAAS IDEA]
Target users: [OPTIONAL]
Market: [OPTIONAL]
Domain: [OPTIONAL]
```

Then create the unique frontend/brand direction:

```txt
Read agent-loops/02a-unique-frontend-brand-design.md and create a unique frontend design system for this PRD.

The design must not look like a generic AI-generated SaaS app.
Create brand identity, logo/icon prompts, layout system, component styling rules, and anti-generic checks before implementation.
```

Then scaffold:

```txt
Read agent-loops/01-master-saas-scaffold.md and scaffold the SaaS based on the PRD and the unique frontend brand design system.

Use the default stack unless there is a strong reason not to.
Build the project to 90% completion.
Leave only env setup, provider keys and final business rules for me.
```

For domain, Auth.js, and billing setup, ask:

```txt
Read agent-loops/16-domain-auth-billing-setup.md and create the setup plan for:

Domain: [yourdomain.com]
App name: [your app name]
Product idea: [your SaaS idea]
Target users: [who will pay]
Currency: [GBP/USD/EUR]
Preferred billing: [monthly / yearly / both]
Auth provider: [Auth.js]
Payment provider: [Stripe]
```

## Suggested execution order

0. `00-idea-to-prd-market-research.md`
1. `02a-unique-frontend-brand-design.md`
2. `01-master-saas-scaffold.md`
3. `02-ui-ux-design.md`
4. `03-auth-prisma.md`
5. `04-google-login.md`
6. `05-billing.md`
7. `06-database-seed.md`
8. `07-analytics.md`
9. `08-agent-readiness.md`
10. `09-marketing.md`
11. `10-testing.md`
12. `11-ecommerce-testing.md`
13. `12-admin-panel.md`
14. `13-email-notifications.md`
15. `14-security-hardening.md`
16. `15-deployment.md`
17. `16-domain-auth-billing-setup.md`

## Default SaaS stack

- Next.js App Router
- TypeScript
- Tailwind CSS
- shadcn/ui as base primitives only
- Prisma ORM
- PostgreSQL-compatible database
- Auth.js
- Google login
- Subscription billing
- PostHog or GA4 analytics
- Playwright testing
- Vercel, Hostinger VPS, Railway, Render, or Docker deployment
