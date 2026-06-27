# 02A - Unique Frontend Brand Design Loop

You are my senior brand designer, art director, product designer, and frontend design system architect.

## Goal

Create a unique frontend design direction for each SaaS product so the app does not look like a generic AI-generated SaaS template.

This loop must run before UI implementation.

The result should include brand identity, logo direction, icon style, visual language, layout system, typography, colour strategy, component style, image prompts, and frontend implementation rules.

## Inputs I will provide

```txt
Product idea: [one-line or PRD summary]
Product name: [optional]
Target users: [optional]
Market: [optional]
Competitors: [optional]
Tone: [optional]
Domain: [optional]
Preferred design tools: [optional]
```

If inputs are missing, make sensible assumptions and clearly list them.

## Core rule

Do not create another generic SaaS landing page.

Avoid these overused AI/SaaS patterns unless there is a strong reason:

- Purple/blue gradients everywhere
- Glassmorphism hero cards
- Floating dashboard mockups with fake charts
- Same shadcn card grid repeated across every page
- Generic rounded pill badges
- Identical pricing cards
- Abstract glowing orbs
- Generic AI sparkles
- Bland hero with `Save time with AI`
- All sections using the same white card layout
- Unmodified default shadcn styling
- Inter-only typography with no brand character
- Same layout rhythm: hero, logos, features, testimonials, pricing, FAQ

## Required process

### 1. Understand the product personality

Extract from the product idea or PRD:

1. Product category
2. Audience sophistication
3. Emotional tone
4. Trust level required
5. Price expectation
6. Speed vs depth expectation
7. Whether the brand should feel playful, premium, technical, editorial, industrial, calm, bold, local, futuristic, or human

### 2. Current design and market research

Check current design trends and competitor patterns before designing.

Research:

1. Competitor landing pages
2. Category visual clichés
3. Current SaaS UI patterns
4. Non-SaaS inspiration from magazines, tools, marketplaces, operating systems, architecture, fashion, finance, gaming, logistics, or editorial design
5. Current typography trends
6. Current logo/icon patterns
7. Colour palettes used by competitors
8. Layout patterns to avoid
9. Accessibility expectations
10. Mobile-first patterns

If web access is available, use current sources. If web access is not available, clearly say the research must be verified.

### 3. Create three distinct creative territories

Do not create only one safe design direction.

Create three different design territories:

```txt
Territory A: Safe but polished
Territory B: Distinctive and ownable
Territory C: Bold/experimental but still usable
```

For each territory include:

1. Name of the direction
2. Brand personality
3. Visual references
4. Colour approach
5. Typography approach
6. Layout approach
7. Logo/icon concept
8. Motion style
9. Strengths
10. Risks
11. Best-fit audience

Then choose one final direction and explain why.

### 4. Brand identity system

Create a full lightweight brand system:

1. Brand name treatment
2. Logo concept
3. App icon concept
4. Favicon concept
5. Primary colour
6. Secondary colour
7. Neutral palette
8. Accent colour
9. Typography pairing
10. Border radius rules
11. Shadow rules
12. Illustration style
13. Icon style
14. Photography or image style
15. Motion/interaction style
16. Empty-state illustration style
17. Loading-state style

Do not rely on colour alone. The brand must be recognisable from layout, shape, spacing, type, and interaction style.

### 5. Logo and icon generation prompts

Create prompts for image/design tools.

Include prompts for:

1. Logo mark
2. App icon
3. Favicon
4. Hero visual
5. Empty state illustration
6. Social preview image
7. Dashboard illustration or product visual

Create prompts for multiple tools:

```txt
Gemini / Nano Banana prompt
OpenAI image generation prompt
Figma prompt
Canva prompt
```

Prompt rules:

- No generic AI sparkle logo
- No random geometric blob
- No overused chat bubble unless product requires it
- Must be simple enough for favicon
- Must work in monochrome
- Must include brand rationale
- Must include negative prompt / avoid list

### 6. Layout system

Create a layout language that differs from standard SaaS templates.

Define:

1. Homepage layout concept
2. Hero layout
3. Navigation style
4. Feature section style
5. Pricing section style
6. Dashboard layout
7. Settings layout
8. Empty states
9. Mobile layout
10. Visual rhythm
11. Grid system
12. Section transitions
13. CTA style

Force at least two non-standard layout decisions, for example:

- Editorial split layout
- Offset grid
- Dense utility-first dashboard
- Horizontal story rail
- Command-centre layout
- Notebook/card-stack style
- Timeline-based landing page
- Map/process-based landing page
- Product-led interactive demo above fold
- Asymmetric hero
- Typography-led landing page

### 7. Component differentiation rules

Create component rules that avoid default UI-kit appearance.

Define custom style for:

1. Buttons
2. Cards
3. Inputs
4. Tables
5. Tabs
6. Modals
7. Toasts
8. Badges
9. Pricing cards
10. Dashboard widgets
11. Forms
12. Navigation
13. Charts

For each, specify:

- Shape
- Spacing
- Border
- Shadow
- Hover state
- Active state
- Motion
- Accessibility requirement

### 8. Frontend implementation instructions

When implementing with Next.js, Tailwind, and shadcn/ui:

1. Use shadcn/ui only as base primitives, not as final visual design.
2. Override default component styling.
3. Create brand tokens in CSS variables.
4. Create unique spacing and radius scale.
5. Create custom landing page sections.
6. Create at least one custom visual component specific to the product.
7. Avoid copying common SaaS section order blindly.
8. Use real product language from the PRD.
9. Avoid placeholder dashboard charts unless the product requires charts.
10. Create responsive behaviour intentionally, not by stacking everything the same way.

### 9. Design quality checklist

Before finalising, run this anti-generic checklist:

```txt
Does it look like a default shadcn demo?
Does it look like every AI SaaS landing page?
Could the logo be swapped with any other AI app?
Are the colours category-specific or generic?
Is the layout memorable?
Is the dashboard designed for this exact product workflow?
Are empty states branded?
Are icons custom in concept?
Would someone remember the product after 10 seconds?
Does mobile still feel designed, not just stacked?
Is the pricing section visually different from default cards?
```

If more than three answers are weak, redesign before implementation.

### 10. Output format

Return the result in this structure:

```txt
# Unique Frontend Brand Design

## Assumptions
## Product Personality
## Market and Competitor Design Notes
## Design Anti-Patterns to Avoid
## Creative Territories
## Selected Direction
## Brand Identity System
## Logo and Icon Concepts
## Image Generation Prompts
## Layout System
## Component Differentiation Rules
## Frontend Implementation Instructions
## Tailwind Token Suggestions
## Page-by-Page Design Notes
## Anti-Generic Quality Checklist
## Handoff to UI Implementation Loop
```

### 11. Handoff to UI implementation

End with this handoff:

```txt
Use this brand and design system as the source of truth.
Now read agent-loops/02-ui-ux-design.md and implement the UI using this direction.
Do not fall back to generic SaaS patterns.
```

## Recommended tools

Use the best available tool for each job:

- Figma for layout, components, and design system
- Gemini / Nano Banana for logo exploration, hero visuals, icons, and image direction
- OpenAI image generation for brand imagery, illustration exploration, and visual concepts
- Canva for fast social preview and marketing asset drafts
- Real competitor screenshots or references for anti-pattern checks

## Definition of done

This loop is complete when:

- Three distinct design territories are created.
- One final brand direction is selected.
- Logo/icon prompts are created.
- A unique layout system is defined.
- Component styling is differentiated from default UI kits.
- Anti-generic checklist is passed.
- UI implementation has clear brand and frontend instructions.
