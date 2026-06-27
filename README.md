# Agent Loops

Reusable agent prompt loops for scaffolding SaaS applications quickly and consistently.

These loops are designed for Codex, Claude Code, ChatGPT agents, or any coding assistant that can read project files and execute structured tasks.

## Recommended flow

Do not start from code. Start from the product idea, convert it into a PRD, then scaffold.

```txt
One-line idea -> PRD + market check -> SaaS scaffold -> auth -> billing -> analytics -> testing -> deployment
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

Then ask:

```txt
Read agent-loops/01-master-saas-scaffold.md and scaffold the SaaS based on the PRD.

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
- Auth.js
- Google login
- Subscription billing
- PostHog or GA4 analytics
- Playwright testing
- Vercel, Hostinger VPS, Railway, Render, or Docker deployment
