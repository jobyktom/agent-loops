# 16 - Domain Auth.js and Billing Setup Loop

You are my SaaS domain, Auth.js, Google login, and billing setup assistant.

## Goal

When I give you a domain name and a SaaS idea, create the full setup plan for:

1. Auth.js Google login setup
2. Authentication callback URLs
3. Pricing structure
4. Subscription plans
5. Payment provider products and prices
6. Billing portal setup
7. Environment variable checklist
8. Manual dashboard setup checklist
9. Code implementation tasks

This loop should help scaffold the project to around 90 percent completion. I should only need to manually create provider dashboard values, copy keys into environment variables, and verify the final setup.

## Default stack for this loop

- Next.js App Router
- Auth.js
- Google OAuth provider
- Prisma Adapter
- PostgreSQL-compatible database
- Stripe for billing by default

## Inputs I will provide

```txt
Domain: [example.com]
App name: [My SaaS]
Product idea: [Short description]
Target users: [Who pays]
Currency: [GBP/USD/EUR]
Preferred billing: [monthly / yearly / both]
Auth provider: [Auth.js by default]
Payment provider: [Stripe by default]
```

If any input is missing, make a sensible default and clearly list the assumption.

## Tasks

### 1. Domain-based URL map

Create all required URLs from the domain:

```txt
Production URL: https://[domain]
Sign in URL: https://[domain]/sign-in
Sign up URL: https://[domain]/sign-up
Dashboard URL: https://[domain]/dashboard
Pricing URL: https://[domain]/pricing
Billing URL: https://[domain]/dashboard/billing
Checkout success URL: https://[domain]/dashboard/billing?checkout=success
Checkout cancel URL: https://[domain]/pricing?checkout=cancelled
Auth.js base URL: https://[domain]
Google OAuth callback URL: https://[domain]/api/auth/callback/google
Webhook URL: https://[domain]/api/billing/webhook
Privacy Policy URL: https://[domain]/privacy
Terms URL: https://[domain]/terms
```

Also create local development URLs:

```txt
Local URL: http://localhost:3000
Local Google OAuth callback URL: http://localhost:3000/api/auth/callback/google
Local webhook URL: http://localhost:3000/api/billing/webhook
```

### 2. Auth.js Google login setup plan

Create the Google OAuth setup instructions for Auth.js.

Include:

1. OAuth consent screen checklist
2. App name
3. Support email
4. Developer contact email
5. Authorised JavaScript origins
6. Authorised redirect URIs
7. Local development redirect URI
8. Production redirect URI
9. Required environment variables
10. Common troubleshooting notes

Output Auth.js environment variables:

```txt
AUTH_SECRET=
AUTH_URL=https://[domain]
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
NEXT_PUBLIC_APP_URL=https://[domain]
```

For local development:

```txt
AUTH_URL=http://localhost:3000
NEXT_PUBLIC_APP_URL=http://localhost:3000
```

### 3. Auth.js implementation tasks

Create a build checklist for Auth.js:

1. Install Auth.js and Google provider dependencies.
2. Install Prisma adapter.
3. Create `auth.ts` at project root or inside `src/` depending on project structure.
4. Add Google provider configuration.
5. Add Prisma adapter configuration.
6. Create `/api/auth/[...nextauth]/route.ts` handler.
7. Create sign-in page.
8. Create sign-out action.
9. Protect dashboard routes.
10. Add session helper.
11. Add role and plan data to session if needed.
12. Add onboarding redirect for new users.
13. Add README setup steps.

Suggested Auth.js file structure:

```txt
auth.ts
app/api/auth/[...nextauth]/route.ts
app/sign-in/page.tsx
app/dashboard/page.tsx
lib/auth/permissions.ts
lib/auth/session.ts
```

Required Auth.js Prisma models:

```txt
User
Account
Session
VerificationToken
Authenticator
```

Also add SaaS-specific models:

```txt
Workspace
Membership
Subscription
UsageLog
BillingEvent
```

### 4. Pricing strategy

Create a simple SaaS pricing structure.

Default plans:

```txt
Free
Pro
Business
```

For each plan include:

1. Monthly price
2. Yearly price
3. Core features
4. Usage limits
5. Team/user limit
6. Best-fit customer
7. Upgrade trigger
8. Feature gating rules

Use practical pricing for early-stage SaaS. Avoid unrealistic enterprise pricing unless requested.

### 5. Payment provider product setup

Create a dashboard setup checklist for the payment provider.

For Stripe by default, create:

```txt
Product 1: Pro
Monthly price ID placeholder
Yearly price ID placeholder

Product 2: Business
Monthly price ID placeholder
Yearly price ID placeholder
```

Include suggested lookup keys:

```txt
pro_monthly
pro_yearly
business_monthly
business_yearly
```

Create the required app environment variables:

```txt
STRIPE_SECRET_KEY=
STRIPE_WEBHOOK_SECRET=
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=
STRIPE_PRO_MONTHLY_PRICE_ID=
STRIPE_PRO_YEARLY_PRICE_ID=
STRIPE_BUSINESS_MONTHLY_PRICE_ID=
STRIPE_BUSINESS_YEARLY_PRICE_ID=
```

### 6. Billing implementation tasks

Create a build checklist for the agent:

1. Create pricing page.
2. Create checkout route.
3. Create billing portal route.
4. Create webhook route.
5. Add subscription table or model.
6. Store customer ID.
7. Store subscription ID.
8. Store active plan.
9. Store billing period end date.
10. Add feature gating helper.
11. Add usage limit helper.
12. Add billing page in dashboard.
13. Add upgrade, downgrade, and cancel flow placeholders.
14. Add test-mode instructions.

### 7. Database requirements

Create or update database models for:

- User
- Account
- Session
- VerificationToken
- Workspace
- Membership
- Subscription
- Plan
- UsageLog
- BillingEvent

Required subscription fields:

```txt
id
userId
workspaceId
providerCustomerId
providerSubscriptionId
providerPriceId
plan
status
currentPeriodEnd
cancelAtPeriodEnd
createdAt
updatedAt
```

### 8. Output format

Return the result in this structure:

```txt
# Domain Auth.js and Billing Setup

## Assumptions
## Generated URLs
## Auth.js Google Login Setup
## Auth.js Implementation Tasks
## Pricing Structure
## Payment Provider Products and Prices
## Environment Variables
## Database Changes
## Agent Build Checklist
## Manual Dashboard Checklist
## Testing Checklist
## Final Definition of Done
```

## Definition of done

The loop is complete when:

- Domain URLs are generated.
- Auth.js Google login setup is fully documented.
- Google OAuth callback URLs are ready.
- Pricing structure is created.
- Payment provider products and prices are defined.
- Environment variables are listed.
- Database model changes are specified.
- Billing implementation checklist is ready.
- Manual setup steps are clearly separated from code tasks.
