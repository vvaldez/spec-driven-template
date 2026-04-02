# SECURITY.md

## Scope and Intent
This repository is a **markdown-only, planning-first template**. It is not a place for executable code, secrets, or sensitive production data. The goal is to keep this project safe to share and fork while you think and plan.

## No Code, No Secrets Policy
- **No executable code**: Do not add source files, scripts, binaries, or configurations intended to be run directly.
- **No build or deployment setup**: Do not add package manifests, CI/CD pipelines, or infrastructure definitions here.
- **Never commit secrets**: Never store API keys, tokens, passwords, private keys, or any other secret material in this repository.
- **No sensitive personal or customer data**: Do not paste real credentials, private logs, or identifiable user data into any file.

Assume that anything committed here may eventually become public. Treat this repo as a safe, shareable planning space.

## Collaboration and `CONTEXT*` files (default: private)

The template **gitignores** `CONTEXT.md`, `CONTEXT_TRANSFER.md`, and `CONTEXT_TRANSFER_FROM_*.md` so personal session notes and handoffs are not pushed by mistake. **Collaboration still works** when each contributor keeps their own context private and the team shares **committed** specs and process docs instead.

If your team **chooses** to track and share those files, you must treat them like any other committed markdown: **everyone with repo access can read them**, and **git history keeps past versions**. Only opt in after the group agrees that level of sharing is acceptable. With today’s tooling, keeping per-person context private and sharing `SPEC.md`-style artifacts is a reasonable default.

## Data Handling
- When you need to discuss real systems, redact or anonymize details before adding them to markdown files.
- If you must reference logs or stack traces, remove or obfuscate any sensitive identifiers.
- Prefer describing patterns and structures over copying raw data.

## Safe Use of AI Models
- Be cautious when pasting context into AI tools; avoid including secrets or sensitive data in prompts.
- If you suspect sensitive content was added to this repository or shared with a model, **rotate any affected credentials** and clean the content immediately.
- Treat AI outputs as suggestions; review them with human judgment before adopting them into your plans.

## Rules for Agents and Tools
- Agents must follow the constraints defined here and in `AGENTS.md`.
- If the human asks for actions that conflict with these rules (for example, adding code or secrets), assistants should:
  - Explain the conflict.
  - Suggest safer alternatives, such as creating a separate implementation repository or using a secure secret manager.

## Creating a Safe Implementation Repository
When you are ready to build a real system:
1. Create a **separate implementation repository** for actual code and automation.
2. Configure it to use environment variables, secret managers, or other secure mechanisms for credentials.
3. Copy only the necessary markdown specs from this template into that implementation repo.
4. Keep this template repository free of code and secrets, using it as a planning and documentation space.

