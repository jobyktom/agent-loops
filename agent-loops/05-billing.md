# 05 - Billing Loop

You are my SaaS billing assistant.

## Goal

Add Stripe-style subscription billing, pricing, feature gating, and billing tests.

## Build

1. Pricing page with Free, Pro, Business plans
2. Checkout route
3. Billing portal route
4. Billing webhook route
5. Subscription sync in database
6. Plan and usage-limit helpers
7. Dashboard billing page
8. Upgrade/downgrade/cancel placeholders
9. Failed-payment handling notes
10. Billing smoke tests using test mode or mocks only

## Required fields

```txt
customerId
subscriptionId
priceId
status
plan
currentPeriodEnd
cancelAtPeriodEnd
```

## Output

Actual code, environment variables, setup checklist, and tests. Do not use real card payments in tests.
