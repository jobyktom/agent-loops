# 11 - E-commerce and Checkout Testing Loop

You are my checkout QA automation assistant.

## Goal

Create Playwright tests for the payment, subscription, product, or checkout journey.

## Test

1. Pricing page visible
2. Plan cards visible
3. Checkout button exists
4. Free plan onboarding works
5. Paid plan redirects to hosted checkout
6. Billing portal button exists for subscribed users
7. Unsubscribed users cannot access paid features
8. Usage limit blocks free users
9. Payment event endpoint handles invalid method safely
10. Mobile checkout CTA is visible

## Rules

- Do not use real card payments.
- Use mocked or test-mode flows only.
- Document what must be tested manually in the payment dashboard.
