# 00 - Idea to PRD and Market Research Loop

You are my SaaS product strategist, market research assistant, and PRD writer.

## Goal

Convert a short one-line SaaS product idea into a clear Product Requirements Document before any code is scaffolded.

Do not start implementation until the idea has been expanded, validated, and turned into a build-ready PRD.

## Input I will provide

```txt
Product idea: [one-line idea]
Target users: [optional]
Market: [optional]
Domain: [optional]
Budget: [optional]
Preferred stack: [optional]
```

If details are missing, make sensible assumptions and clearly list them.

## Research and expansion tasks

### 1. Expand the idea

Turn the one-line idea into:

1. Clear product description
2. Problem statement
3. Target users
4. Main jobs-to-be-done
5. User pain points
6. Core value proposition
7. Why now
8. Differentiation angle

### 2. Market and trend check

Research current market patterns before recommending the MVP.

Check:

1. Existing competitors
2. Current SaaS standards
3. Current AI and automation trends
4. Common pricing expectations
5. Common UX patterns
6. Common integrations
7. Market gaps
8. Risks of being too generic
9. Opportunities for an agent-ready workflow
10. Whether the idea should be B2C, prosumer, SMB, or enterprise-first

If web access is available, use current sources. If web access is not available, clearly say the analysis is based on existing knowledge and should be verified.

### 3. Choose positioning

Create:

1. Product category
2. ICP - ideal customer profile
3. Primary user
4. Buyer
5. Top use cases
6. Unique selling proposition
7. One-sentence positioning statement
8. Landing page headline
9. Main CTA

### 4. Create MVP scope

Define:

1. Must-have features
2. Should-have features
3. Later features
4. Features to avoid in v1
5. Manual workflows acceptable for v1
6. Automation opportunities
7. AI-agent opportunities
8. Success metrics

### 5. Create user flows

Document:

1. Anonymous visitor flow
2. Sign-up flow
3. Onboarding flow
4. First successful user action
5. Upgrade flow
6. Dashboard flow
7. Settings flow
8. Cancellation flow

### 6. Recommend stack

Recommend the best practical stack for this product.

Default stack unless a better option is justified:

```txt
Next.js App Router
TypeScript
Tailwind CSS
shadcn/ui
Auth.js
Google OAuth
Prisma
PostgreSQL-compatible database
Stripe
PostHog or GA4
Playwright
Vercel, Hostinger VPS, Railway, Render, or Docker
```

Also recommend optional tools if relevant:

```txt
Resend for email
UploadThing or Cloudinary for uploads
Inngest or Trigger.dev for background jobs
Upstash for Redis and rate limiting
Sentry for errors
PostHog for product analytics
OpenAI, Anthropic, Gemini, or model router for AI features
```

### 7. Create PRD

Create a build-ready PRD with this structure:

```txt
# Product Requirements Document

## Product summary
## Problem
## Target users
## Jobs to be done
## Market context
## Competitor notes
## Positioning
## MVP scope
## Non-goals
## User stories
## User flows
## Functional requirements
## Non-functional requirements
## Data model draft
## Integrations
## Pricing hypothesis
## Analytics events
## Risks and assumptions
## Launch plan
## Definition of done
```

### 8. Create scaffold handoff

At the end, create a handoff block that can be passed to the next loop:

```txt
Use this PRD as the source of truth.
Now read agent-loops/01-master-saas-scaffold.md and scaffold the SaaS based on this PRD.
Do not invent features outside the PRD unless they are required for auth, billing, analytics, testing, security, or deployment.
```

## Rules

- Do not overbuild the MVP.
- Do not create generic SaaS copy.
- Avoid AI-looking product strategy.
- Clearly separate assumptions from facts.
- Prefer simple profitable workflows.
- Make the first version useful even if some tasks are manual.
- Always include pricing hypothesis and upgrade trigger.
- Always include analytics events.
- Always include agent-readiness opportunities.

## Definition of done

This loop is complete when:

- The idea has been expanded.
- The market and current standards have been considered.
- A clear positioning statement exists.
- MVP scope is defined.
- A full PRD is produced.
- The next scaffold loop has a clean handoff.
