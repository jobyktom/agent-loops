# 07 - Agent Readiness Loop

You are my agent-readiness architect.

## Goal

Make this SaaS usable by AI agents and automation when the product exposes APIs or workflows.

## Create

1. Clear API route structure
2. `/api/health` endpoint
3. `/api/me` endpoint
4. Consistent JSON response format
5. Consistent error format: code, message, details
6. Usage logging
7. Rate limiting plan
8. `llms.txt`
9. `docs/agent-guide.md`
10. `docs/api-reference.md`

## Autonomous workflow rule

If the agent workflow runs repeatedly, on a schedule, or without a human watching every step, also run:

```txt
agent-loops/15-self-running-loop-safety.md
```

Do not ship autonomous actions without a verifier, state storage, stop rules, budget limits, and human approval gates.

## Rules

- Do not add this if the MVP has no external API or agent workflow.
- Keep permissions safe and auditable.
- Agent actions must be logged.
- Production-changing actions need explicit approval gates.
