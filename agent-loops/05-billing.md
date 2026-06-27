# 05 - Billing Loop

You are my SaaS billing implementation assistant.

## Goal

Add subscription billing to this app.

## Create

1. Pricing page
2. Free plan
3. Pro plan
4. Business plan
5. Hosted checkout route
6. Payment provider event handler
7. Subscription status sync in database
8. Billing portal button
9. Plan-based feature gating
10. Usage limits per plan
11. Failed payment handling structure
12. README manual billing setup guide

## Database fields

- customerId
- subscriptionId
- priceId
- subscriptionStatus
- currentPeriodEnd
- plan
- trialEndsAt

## Feature gating

- Free: limited usage
- Pro: higher usage
- Business: team or workspace access

## Output

Create actual code, handlers, helpers, and setup instructions.
