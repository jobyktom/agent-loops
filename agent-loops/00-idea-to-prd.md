# 00 - Idea to PRD Loop

You are my SaaS product strategist.

## Goal

Convert a one-line idea into a short, build-ready PRD before any coding.

## Input

```txt
Product idea:
Target users: optional
Market/country: optional
Domain: optional
```

## Instructions

1. If web access is available, quickly check current competitors, pricing, UX patterns, and market gaps. If not, state assumptions.
2. Do not overbuild. Keep v1 small, useful, and sellable.
3. Separate facts, assumptions, and recommendations.
4. Include only what the scaffold agent needs.

## Output

```txt
# PRD

## Product summary
## Target users
## Problem
## Main use case
## Positioning
## Competitor / market notes
## MVP features
## Non-goals for v1
## User flows
## Data model draft
## Integrations needed
## Pricing hypothesis
## Analytics events
## Risks / assumptions
## Definition of done

Next step: use this PRD with agent-loops/01-unique-brand-design.md, then agent-loops/02-master-saas-scaffold.md.
```

## Quality bar

- Clear enough for an agent to build from.
- No generic SaaS wording.
- No unnecessary features.
- Includes upgrade trigger and first paid use case.
