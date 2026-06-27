# Agent Loops

Reusable agent prompt loops for scaffolding SaaS applications quickly and consistently.

These loops are designed for Codex, Claude Code, ChatGPT agents, or any coding assistant that can read project files and execute structured tasks.

## How to use

Copy this repository or the `agent-loops/` folder into any new SaaS project.

Then ask your agent:

```txt
Read agent-loops/01-master-saas-scaffold.md and execute it for this SaaS idea:

[PASTE YOUR SAAS IDEA]

Use the default stack unless there is a strong reason not to.
Build the project to 90% completion.
Leave only env setup, provider keys and final business rules for me.
```

For domain, auth, and billing setup, ask:

```txt
Read agent-loops/16-domain-auth-billing-setup.md and create the setup plan for:

Domain: [yourdomain.com]
App name: [your app name]
Product idea: [your SaaS idea]
Target users: [who will pay]
Currency: [GBP/USD/EUR]
Preferred billing: [monthly / yearly / both]
Auth provider: [Clerk / Auth.js / Supabase Auth]
Payment provider: [Stripe]
```

## Suggested execution order

1. `01-master-saas-scaffold.md`
2. `02-ui-ux-design.md`
3. `03-auth-prisma.md`
4. `04-google-login.md`
5. `05-billing.md`
6. `06-database-seed.md`
7. `07-analytics.md`
8. `08-agent-readiness.md`
9. `09-marketing.md`
10. `10-testing.md`
11. `11-ecommerce-testing.md`
12. `12-admin-panel.md`
13. `13-email-notifications.md`
14. `14-security-hardening.md`
15. `15-deployment.md`
16. `16-domain-auth-billing-setup.md`

## Default SaaS stack

- Next.js App Router
- TypeScript
- Tailwind CSS
- shadcn/ui
- Prisma ORM
- PostgreSQL-compatible database
- Clerk or Auth.js
- Google login
- Subscription billing
- PostHog or GA4 analytics
- Playwright testing
- Vercel, Hostinger VPS, Railway, Render, or Docker deployment
