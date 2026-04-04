# `.dev/AGENTS.md` — Maintainer context for assistants

Read this file **only when** the human has identified themselves as a **maintainer**, **template contributor**, or **template editor** for *this* repository (or has asked you explicitly to follow maintainer rules). Otherwise, follow root **`AGENTS.md`** only and assume a **template user** audience.

This file **adds** to root `AGENTS.md`; it does not relax **Rule #1** (safety, `SECURITY.md`, no secrets) or the **markdown-only** contract.

## When you are in maintainer context

1. Keep root **`AGENTS.md`** in force (planning-first, no executable codebase, separate implementation repos).
2. Read **`DEV.md`** for scope (what belongs in this template repo vs. out of scope) and maintainer workflow.
3. Read **`.dev/TODO.md`** for maintainer milestones and in-flight work; align suggestions with it when relevant. **Do not** confuse it with **root `TODO.md`** (the template user’s project checklist).
4. Use **`SOP.md`** (especially Git workflow) when proposing how changes should land.
5. Prefer **`INTENT.md`** when trade-offs touch charter, Rules **#1–#3**, **explicit language** (template user vs maintainer vs product audience), or template design intent. Use **`.advanced/AUDIENCE.md`** when naming roles or synonyms in docs.

## Maintainer-specific behavior

- Optimize for **many fork users** who read little: small, reviewable edits; clear cross-links; avoid bulk rewrites unless asked.
- End-user-facing changes should surface in **`README.md`** or the relevant root / `.advanced/` file, not only in `DEV.md` or `.dev/`.
- Do not add executable code, dependency manifests, or runnable-project tooling to this repository.
- **No secrets** in any path, including under `.dev/`.

## Other files under `.dev/`

The **`.dev/`** directory is **tracked** in git. Besides this file, maintainers may add other shared notes here over time. Do not assume every file under `.dev/` exists; read paths the human names. If only maintainer context is stated and no other paths are given, **this file (`AGENTS.md`) is the default extra contract** beyond the repo root.
