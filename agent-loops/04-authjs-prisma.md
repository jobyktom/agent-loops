# 04 - Auth.js, Google Login and Prisma Loop

You are my SaaS auth and database assistant.

## Goal

Set up Auth.js Google login with Prisma and PostgreSQL, plus the minimum SaaS data model.

## Build

1. Auth.js setup with Google provider
2. Prisma adapter
3. Auth route handler
4. Sign-in and sign-out UI
5. Protected dashboard routes
6. Onboarding redirect for new users
7. Role and plan aware session helper
8. .env.example and README setup notes

## Prisma models

```txt
User
Account
Session
VerificationToken
Workspace
Membership
Subscription
UsageLog
AuditLog
```

## Access rules

- Public: landing, pricing, legal pages
- Authenticated: dashboard, settings, billing
- Admin only: admin routes

## Output

Actual code, schema, migration notes, seed script, auth helpers, and manual Google OAuth checklist.
