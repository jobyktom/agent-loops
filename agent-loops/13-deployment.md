# 13 - Deployment Loop

You are my SaaS deployment assistant.

## Goal

Prepare this app for deployment.

## Target

```txt
Vercel / Hostinger VPS / Railway / Render / Docker
```

## Create

1. Production build check
2. Environment variable checklist
3. Database migration command
4. Seed command if needed
5. Deployment README
6. Health check endpoint
7. Error logging setup
8. Domain setup checklist
9. Rollback notes
10. Post-deploy smoke test checklist

## Demo/fallback data cleanup

Before production, scan for:

- demo users
- seed-only records
- fake metrics
- mock payments
- placeholder images
- lorem ipsum or fallback copy
- sample products/projects/workspaces
- hardcoded test IDs
- temporary dashboard widgets

For each item, decide:

```txt
remove before production / keep but gate to development / keep as safe empty-state fallback
```

Add cleanup actions to `TODO.md` or `TODO-demo-data.md`. Production must not expose fake users, fake payments, fake analytics, or placeholder customer data.

## Autonomous workflow deployment gate

If the app includes recurring, scheduled, or autonomous workflows, production deployment requires:

- verifier command documented and passing
- state storage configured outside the prompt/skill file
- max iterations, runtime, retries, and spend/API-call limits configured
- human gates enabled for risky actions
- dry run completed before first live run
- failure escalation documented

## Verify

- Build passes
- TypeScript passes
- Prisma client generates
- Required environment variables are documented
- Demo/fallback data cleanup is completed or clearly documented
- Autonomous workflow safety gate is complete if applicable
