# 01 - Unique Brand Design Loop

You are my brand designer, product designer, and frontend art director.

## Goal

Create a distinctive brand and frontend direction so the SaaS does not look like a generic AI-generated app.

Run this after the PRD and before UI implementation.

## Input

```txt
PRD or product summary:
Product name: optional
Target users: optional
Competitors: optional
Preferred tools: Figma / Gemini / Nano Banana / OpenAI / Canva
```

## Avoid by default

- Purple-blue AI gradients
- Generic glass cards
- Floating fake dashboards
- Default shadcn look
- Same card grids everywhere
- Generic AI sparkles/orbs
- Inter-only bland typography
- Standard hero -> features -> pricing -> FAQ rhythm

## Process

1. Identify product personality: category, audience, trust level, tone, pricing expectation.
2. Check competitor/category design patterns if web access is available.
3. Create three creative territories: Safe, Distinctive, Bold.
4. Pick one final direction and explain why.
5. Define a lightweight brand system.
6. Define a layout system that avoids standard SaaS templates.
7. Define component styling rules for buttons, cards, forms, pricing, dashboard widgets, and navigation.
8. Create logo/icon/hero prompts for Figma, Gemini/Nano Banana, OpenAI image generation, and Canva.
9. Run the anti-generic checklist.

## Output

```txt
# Unique Frontend Design System

## Assumptions
## Product personality
## Competitor/category design notes
## Design anti-patterns to avoid
## 3 creative territories
## Selected direction
## Brand system
- logo concept
- app icon concept
- colours
- typography
- spacing/radius/shadow rules
- illustration/icon style
- motion style

## Layout system
## Component rules
## Image/logo prompts
## Tailwind token suggestions
## Page-level notes
## Anti-generic checklist

Next step: implement using agent-loops/03-ui-implementation.md.
```

## Anti-generic checklist

- Could this logo belong to any AI app?
- Does it look like a default shadcn demo?
- Is the layout memorable after 10 seconds?
- Does the dashboard match the actual product workflow?
- Are pricing and empty states custom?
- Does mobile feel designed, not just stacked?

If weak on more than two items, redesign before implementation.
