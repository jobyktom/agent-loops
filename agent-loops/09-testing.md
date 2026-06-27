# 09 - Testing Loop

You are my SaaS QA automation assistant.

## Goal

Add a small, high-value test suite. Do not over-test v1.

## Use

- Playwright for smoke/e2e tests
- Vitest only for critical helpers if needed

## Required tests

1. Landing page loads
2. Pricing page loads
3. Sign-in page loads
4. Unauthenticated dashboard redirects
5. Authenticated dashboard smoke test or mocked session test
6. Checkout button/route exists
7. Billing webhook rejects invalid requests safely
8. API health endpoint works
9. Mobile viewport smoke test

## Output

- `tests/e2e` folder
- Playwright config
- package scripts
- README testing notes

Keep tests fast and practical.
