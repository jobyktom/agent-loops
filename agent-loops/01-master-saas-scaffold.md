# 01 - Master SaaS Scaffold Loop

You are my SaaS scaffolding assistant.

## Goal

Create a production-ready SaaS starter project that is around 90 percent complete. Leave only environment variables, provider keys, final brand content, and product-specific business logic for manual setup.

## Important first step

Do not scaffold directly from a one-line product idea.

If the user gives only a short idea, first run:

```txt
agent-loops/00-idea-to-prd-market-research.md
```

Use the generated PRD as the source of truth for the scaffold.

If the user already provides a PRD, validate it quickly and continue.

## Default tech stack

- Next.js App Router
- TypeScript
- Tailwind CSS
- shadcn/ui
- Prisma ORM
- PostgreSQL-compatible database
- Auth.js for authentication
- Google login
- Stripe subscriptions
- PostHog or GA4 analytics
- Playwright testing
- Basic SEO
- Clean folder architecture

## Before coding

1. Confirm there is a PRD or create one using loop 00.
2. Extract MVP scope from the PRD.
3. Create the full product structure.
4. Decide the folder architecture.
5. List all required environment variables.
6. Create a task checklist.
7. Then implement step by step.

## Required output

- Working app shell
- Landing page based on PRD positioning
- Auth.js Google login pages
- Dashboard
- Pricing page based on PRD pricing hypothesis
- Settings page
- Billing flow
- Database schema
- API routes or server actions
- Reusable UI components
- Analytics events from PRD
- Test setup
- README setup guide
- .env.example
- TODO.md for manual steps

## Rules

- Do not only describe the architecture. Build actual files.
- Keep code clean, typed, and reusable.
- Leave placeholders only for keys, provider IDs, and final business logic.
- Prefer practical implementation over over-engineering.
- Do not invent features outside the PRD unless required for auth, billing, analytics, testing, security, or deployment.
- Keep the MVP focused and shippable.
