# DEV.md — Developing *this* template repository

## Who should read this

| Role | Primary docs |
| --- | --- |
| **Fork or clone to plan *your* product** (app, story, game, etc.) | `README.md`, `SPEC.md`, `SOP.md`, `AGENTS.md`, `.advanced/PERSONAS.md` |
| **Maintainer: improve the shared markdown template** | `INTENT.md`, this file, `TODO.md`, plus `SOP.md` (Git workflow) and `AGENTS.md` (rules) |

If you are **not** changing the upstream template—only filling specs for your own work—you can ignore `DEV.md` and `TODO.md`.

### Optional local `.dev/` (gitignored)

For **pair-specific** process preferences while you maintain this repo (how you want assistants to behave in *this* workspace), create a **`.dev/`** directory locally (see **`.dev.example/README.md`**). Put files such as `PREFERENCES.md` or `PAIR.md` there—**not** `DEV.md` (name collision with this file). **Agents** only read `.dev/` when the human identifies as a **contributor** and invites it—see `AGENTS.md`.

---

## SPEC — Scope of development for *this* repo

**In scope**

- Markdown documentation: clarity, structure, examples, personas, safety messaging, and discoverability for **people who use the repo as a template**.
- Tracked templates such as `*.example.md` and optional `.advanced/` depth.
- Keeping the repository **markdown-only**: no executable code, no dependency manifests, no CI that turns this into a runnable project (see `AGENTS.md`).

**Out of scope**

- Implementing application or product code **inside** this repository.
- Secrets, credentials, or private customer data in any committed file.
- Automated enforcement (hooks, bots) that contradict the “planning-only, human-readable contract” unless the project explicitly decides otherwise in `TODO.md` / decision logs.

**Persona (maintainer)** — Distinct from template users (Personas 1–4 in `.advanced/PERSONAS.md`): you optimize for **many strangers** who fork once, read little, and need safe defaults. Prefer small, reviewable doc changes and cross-links over bulk rewrites.

---

## SOP — How maintainers work here

1. **Milestones and tasks** — Track them in **`TODO.md`**: mark items complete when merged; add new rows for upcoming work. Keep entries short; use `.advanced/DECISIONS.md` for rationale when it matters.
2. **Git** — Follow **`SOP.md` → Git workflow**: feature branch and pull request to `main` for substantive edits; tiny fixes on `main` if your team agrees.
3. **Scope check** — Before a larger change, skim **SPEC (above)** so the repo stays template-first and markdown-only.
4. **End-user docs** — Changes that affect fork users should eventually be reflected in `README.md` or the relevant root / `.advanced/` file, not only in `DEV.md`.
5. **Agents** — AI assistants in this repo still follow **`AGENTS.md`**. When you ask them to help **maintain the template**, point them at **`DEV.md`** and **`TODO.md`** so they do not confuse maintainer work with a user’s `SPEC.md`. Optionally invite them to read **`.dev/`** only when using local maintainer prefs.

---

## See also

- `INTENT.md` — Charter: Rule #1 / #2 and design intent.
- `TODO.md` — Maintainer milestone checklist.
- `SOP.md` — Day-to-day template usage and Git workflow.
- `AGENTS.md` — Rules for all assistants operating in the repository.
- `.dev.example/README.md` — Explains optional gitignored `.dev/` for maintainer pair prefs.
