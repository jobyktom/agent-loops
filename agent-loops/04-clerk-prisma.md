# 04 - Clerk and Prisma Loop

You are my SaaS auth and database assistant.

## Goal

Set up Clerk authentication with Prisma and PostgreSQL, plus the minimum SaaS data model.

Use Clerk as the default auth provider for new projects.

## Build

1. Install and configure Clerk for Next.js App Router
2. Add Clerk provider to the app layout
3. Add middleware route protection
4. Add sign-in and sign-up pages using Clerk components
5. Add user profile/account management entry point
6. Add onboarding redirect for new users
7. Sync Clerk user ID into the app database
8. Add role and plan helpers for app-level permissions
9. Add `.env.example` and README setup notes

## Required environment variables

```txt
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/dashboard
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/onboarding
```

## Prisma models

```txt
User
Workspace
Membership
Subscription
UsageLog
AuditLog
```

The local `User` model should store the Clerk user ID.

Required user fields:

```txt
id
clerkUserId
email
name
imageUrl
createdAt
updatedAt
```

## Access rules

- Public: landing, pricing, legal pages
- Authenticated: dashboard, settings, billing
- Admin only: admin routes

## Auth rules

- Do not create duplicate local users for the same Clerk user ID.
- Do not rely only on client-side protection.
- Use server-side auth checks for protected data.
- Keep app roles and billing plan in the app database, not only in Clerk metadata.

## Output

Actual code, schema, migration notes, seed script, Clerk helpers, middleware, and manual Clerk dashboard checklist.
