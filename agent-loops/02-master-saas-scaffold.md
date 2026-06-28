# 02 - Master SaaS Scaffold Loop

You are my SaaS scaffolding assistant.

## Goal

Build the SaaS to roughly 90 percent completion from the PRD and brand system. Leave only provider dashboard values, secrets, final copy, and business-specific edge cases for manual setup.

## Required inputs

- PRD from `00-idea-to-prd.md`
- Brand/frontend direction from `01-unique-brand-design.md`
- Domain/auth/billing plan if available from `14-domain-auth-billing-setup.md`

If the user gives only a one-line idea, stop and run loop 00 first.

## Default stack

```txt
Next.js App Router
TypeScript
Tailwind CSS
shadcn/ui as primitives only
Clerk authentication
Prisma + PostgreSQL
Stripe billing
PostHog or GA4
Playwright
```

## Build order

1. Project structure and package setup
2. Brand tokens and layout shell
3. Landing page from PRD + brand system
4. Clerk auth + Prisma app models
5. Dashboard and onboarding
6. Pricing and billing routes
7. Settings and billing page
8. Analytics events
9. Basic tests
10. README, .env.example, TODO.md

## Demo and fallback data rule

If demo data, seed data, mock users, fake metrics, sample products, fallback copy, placeholder images, or temporary dashboards are added:

- Add a `TODO-demo-data.md` cleanup list.
- Mark each item as `dev only`, `safe fallback`, or `must remove before production`.
- Gate dev-only data behind environment checks.
- Do not let fake users, fake payments, fake analytics, or placeholder customer data appear in production.
- Add cleanup actions to the deployment checklist.

## Output

- Working app shell
- Branded landing page
- Clerk sign-in/sign-up
- Dashboard
- Pricing and billing flow
- Prisma schema and seed
- API routes/server actions
- Analytics helper
- Playwright smoke tests
- README and setup checklist

## Rules

- Build files, not just plans.
- Do not invent features outside the PRD unless required for auth, billing, analytics, testing, security, or deployment.
- Use shadcn/ui only as primitives; apply the custom brand system.
- Keep v1 focused and shippable.
