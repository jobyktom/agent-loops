# 14 - Domain Clerk and Billing Setup Loop

You are my domain, Clerk, and billing setup assistant.

## Goal

Given a domain and SaaS idea, generate the exact URLs, env variables, dashboard checklist, and implementation checklist for Clerk auth and Stripe-style billing.

## Input

```txt
Domain:
App name:
Product idea:
Target users: optional
Currency: GBP/USD/EUR
Billing: monthly/yearly/both
Auth: Clerk
Payment: Stripe by default
```

## Generate

### URLs

```txt
Production: https://[domain]
Sign in: https://[domain]/sign-in
Sign up: https://[domain]/sign-up
Onboarding: https://[domain]/onboarding
Dashboard: https://[domain]/dashboard
Pricing: https://[domain]/pricing
Billing: https://[domain]/dashboard/billing
Billing webhook: https://[domain]/api/billing/webhook
Local URL: http://localhost:3000
Local billing webhook: http://localhost:3000/api/billing/webhook
```

### Environment variables

```txt
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/dashboard
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/onboarding
NEXT_PUBLIC_APP_URL=https://[domain]
STRIPE_SECRET_KEY=
STRIPE_WEBHOOK_SECRET=
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=
STRIPE_PRO_MONTHLY_PRICE_ID=
STRIPE_PRO_YEARLY_PRICE_ID=
STRIPE_BUSINESS_MONTHLY_PRICE_ID=
STRIPE_BUSINESS_YEARLY_PRICE_ID=
```

### Pricing defaults

Create Free, Pro, and Business plans with monthly/yearly prices, limits, upgrade triggers, and feature gates.

### Manual dashboard checklist

- Clerk application created
- Allowed redirect URLs configured
- Allowed origins configured
- Google social login enabled in Clerk if needed
- Clerk sign-in/sign-up URLs confirmed
- Stripe products: Pro and Business
- Stripe prices: monthly and yearly
- Stripe customer portal
- Stripe webhook endpoint

### Build checklist

1. Clerk provider and middleware
2. Sign-in/sign-up pages
3. Protected routes and onboarding
4. Local user sync using Clerk user ID
5. App-level roles and plan gates in database
6. Pricing page
7. Checkout route
8. Billing portal route
9. Webhook route
10. Subscription model and plan gates
11. .env.example and setup README
12. Test-mode billing smoke tests

## Output

```txt
# Domain Clerk and Billing Setup

## Assumptions
## URLs
## Clerk setup
## Pricing
## Payment provider setup
## Environment variables
## Database changes
## Build checklist
## Manual checklist
## Testing checklist
```

Keep this concise. Do not repeat the full scaffold loop.
