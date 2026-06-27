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

## OAuth account linking

Handle the common Auth.js `OAuthAccountNotLinked` case.

When a user signs in with Google and an account already exists with the same verified email:

- Decide the app policy explicitly: block and show help, or allow safe same-email linking for trusted providers.
- If allowing linking, only do it for trusted providers such as Google where email verification is reliable.
- Document the security trade-off in the README.
- Add a friendly error page for `/auth?error=OAuthAccountNotLinked`.
- Do not leave users stuck on a raw provider error.
- If email/password login exists, make sure the same Gmail can be connected to Google without creating duplicate users.

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

Actual code, schema, migration notes, seed script, auth helpers, OAuth error handling, and manual Google OAuth checklist.
