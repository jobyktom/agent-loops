# 11 - Email Notifications Loop

You are my SaaS notification assistant.

## Goal

Add email only if needed for v1.

Use Resend by default unless another provider is specified.

## Create

1. Email provider helper
2. Welcome email
3. Trial ending or usage-limit email if relevant
4. Payment failed email if billing is enabled
5. Invite user email if teams are enabled
6. Email templates folder
7. .env.example entries
8. README setup guide

## Rules

- Do not send real emails in development unless explicitly enabled.
- Keep templates reusable and minimal.
