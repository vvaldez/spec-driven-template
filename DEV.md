# DEV.md — Developing *this* template repository

## Who should read this

| Role | Primary docs |
| --- | --- |
| **Template user** — use a copy to plan *your* product (app, story, game, etc.); also: fork user, clone user | `README.md`, `SPEC.md`, [`TODO.md`](TODO.md) (your project checklist), `SOP.md`, `AGENTS.md`, `.advanced/PERSONAS.md`, `.advanced/AUDIENCE.md` |
| **Maintainer: improve the shared markdown template** | `INTENT.md`, this file, `.dev/TODO.md`, `.dev/AGENTS.md` (assistant maintainer layer), plus `SOP.md` (Git workflow) and root `AGENTS.md` (rules) |

**This file (`DEV.md`) is for template maintainers only.** If you are a **template user** (planning your own work, not evolving the shared template), you do **not** need to read **`DEV.md`** or anything under **`.dev/`**—those are the maintainer layer. You **should** use **root [`TODO.md`](TODO.md)** for your project: it explains how to run a checklist next to **`SPEC.md`**.

### Tracked `.dev/` (maintainer layer)

The **`.dev/`** directory is **committed** with this repo. **`AGENTS.md`** inside it is the **shared** maintainer-facing contract for assistants when the human states they are maintaining the template—see root **`AGENTS.md` → Default audience** and **How to Treat `.dev/`**.

You may add other maintainer-facing markdown under `.dev/` over time (e.g. team prefs). **Do not** use the filename **`DEV.md`** here (name collision with this file). **No secrets** in `.dev/`.

For a quick pattern of optional extra files, see **`.dev.example/README.md`**.

---

## SPEC — Scope of development for *this* repo

**In scope**

- Markdown documentation: clarity, structure, examples, personas, safety messaging, and discoverability for **people who use the repo as a template**.
- Tracked templates such as `*.example.md` and optional `.advanced/` depth.
- Keeping the repository **markdown-only**: no executable code, no dependency manifests, no CI that turns this into a runnable project (see `AGENTS.md`).

**Out of scope**

- Implementing application or product code **inside** this repository.
- Secrets, credentials, or private customer data in any committed file.
- Automated enforcement (hooks, bots) that contradict the “planning-only, human-readable contract” unless the project explicitly decides otherwise in **`.dev/TODO.md`** / decision logs.

**Persona (maintainer)** — Distinct from **template users** (Personas 1–4 in `.advanced/PERSONAS.md`): you optimize for **many strangers** who copy the template once, read little, and need safe defaults. Prefer small, reviewable doc changes and cross-links over bulk rewrites. Role vocabulary: `.advanced/AUDIENCE.md`.

---

## SOP — How maintainers work here

1. **Milestones and tasks** — Track them in **`.dev/TODO.md`**: mark items complete when merged; add new rows for upcoming work. Keep entries short; use `.advanced/DECISIONS.md` for rationale when it matters.
2. **Git** — Follow **`SOP.md` → Git workflow**: feature branch and pull request to `main` for substantive edits; tiny fixes on `main` if your team agrees.
3. **Scope check** — Before a larger change, skim **SPEC (above)** so the repo stays template-first and markdown-only.
4. **Template-user-facing docs** — Changes that affect **template users** should eventually be reflected in `README.md` or the relevant root / `.advanced/` file, not only in `DEV.md`.
5. **Agents** — AI assistants follow root **`AGENTS.md`**; when you identify as a **maintainer**, they should also read **`.dev/AGENTS.md`**. Point them at **`DEV.md`** and **`.dev/TODO.md`** so they do not confuse maintainer work with a **template user**’s **`SPEC.md`** or root **`TODO.md`**.

---

## See also

- `INTENT.md` — Charter: Rules #1–#3 and design intent.
- `.dev/TODO.md` — Maintainer milestone checklist (upstream template work).
- `TODO.md` (root) — **Template user** project checklist; maintainers should not use it for upstream milestones.
- `SOP.md` — Day-to-day template usage and Git workflow.
- `AGENTS.md` — Rules for all assistants operating in the repository.
- `.dev/AGENTS.md` — Shared maintainer rules for assistants (read when human states maintainer context).
- `.dev.example/README.md` — Example ideas for additional files under `.dev/`.
- `.advanced/AUDIENCE.md` — Template user vs maintainer vs product audience; synonyms.
