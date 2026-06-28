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
5. Authenticated dashboard smoke test or mocked Clerk session test
6. Checkout button/route exists
7. Billing webhook rejects invalid requests safely
8. API health endpoint works
9. Mobile viewport smoke test
10. Clerk sign-in/sign-up pages render correctly

## Critical journey test

Add one end-to-end or mocked happy-path journey:

```txt
Visitor -> pricing -> sign in/sign up with Clerk -> onboarding -> dashboard -> choose plan -> checkout route -> billing success state -> paid feature access
```

Rules:

- Use mocked Clerk auth/session if real OAuth is not practical in CI.
- Use payment test mode or mocked checkout. Never use real card payments.
- Test the journey at route/state level if external providers cannot run in CI.
- Keep this as one focused journey test, not many duplicated tests.

## Auth edge-case tests

Add one test or manual QA step for:

```txt
Clerk user signs in -> local database user is created or updated using clerkUserId -> no duplicate local users are created for the same Clerk user ID or email
```

Also verify protected routes use server-side auth checks, not only client-side UI hiding.

## Self-running loop tests

If the product includes recurring, scheduled, or autonomous workflows, verify:

- separate verifier exists and can fail clearly
- state storage exists and survives between runs
- max iterations/runtime/retries are enforced
- human-gated actions cannot run without approval
- dry run works before live run

## Output

- `tests/e2e` folder
- Playwright config
- package scripts
- README testing notes

Keep tests fast and practical.
