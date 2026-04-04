# INTENT.md — Why this template is shaped this way

This file is **design philosophy** for the spec-driven template: the *why*, not step-by-step *how* (see `README.md`, `SOP.md`, and `.advanced/` when you need detail).

---

## Rule #1 — Safety and reputation

**Security and trust come before speed or cleverness.** Treat [`SECURITY.md`](SECURITY.md) as authoritative: no secrets, credentials, or sensitive personal or customer data in committed markdown; be cautious what you paste into third-party AI tools.

“Not being in the news in a bad way” means avoiding preventable harm: leaks, compliance failures, unsafe recommendations, and sloppy sharing of private context. **Rule #1 is not optional** and is **never** traded away for convenience.

---

## Rule #2 — Token and attention efficiency

**After Rule #1**, this template optimizes for **small, bounded context**: fewer files read per session, section-scoped help, and handoff files so you do not re-paste long chat history when you switch devices or models. Operational habits live in [`SOP.md`](SOP.md) (*Token and attention efficiency*) and [`AGENTS.md`](AGENTS.md).

Efficiency **never** overrides redaction, safety, or honesty about uncertainty.

---

## Rule #3 — Simplicity and honest reuse

**After Rules #1 and #2**, prefer the **smallest** structure and wording that still works: fewer new files and headings, clearer names, and **no parallel copies** of the same guidance when one canonical place exists. **Borrow and cite** prior art—link to existing sections, `README.md`, or external references—instead of duplicating long explanations. Habits for “simple first” and **Researching Prior Art** live in [`SOP.md`](SOP.md) (*Principles* and *Researching Prior Art*).

Rule #3 **never** overrides Rule #1 or Rule #2 when they conflict.

---

## Audience and outcomes

The template serves **novices through experts**, for **creative and technical** work alike. “Product” in [`SPEC.md`](SPEC.md) means whatever outcome you are specifying (software, story, game, event, research, course, …)—the same files support different domains.

**Vocabulary:** **Template user** means someone using this repo to plan their own work; **template maintainer** means someone evolving the shared template for others. **Product audience** means whoever the *planned outcome* serves (readers, players, customers, …)—see [`.advanced/AUDIENCE.md`](.advanced/AUDIENCE.md) for a compact map and alternate terms.

---

## Explicit language

Prefer **named roles** over vague “user” or “we” when it matters: say **template user**, **template maintainer**, or **product audience** (or point to a section of `SPEC.md`). Synonyms and examples live in [`.advanced/AUDIENCE.md`](.advanced/AUDIENCE.md). Being explicit reduces confusion between “reader of this template” and “user of the thing I am specifying.”

---

## Progressive disclosure (Personas 1–4)

Optional depth lives under **`.advanced/`** (a dot-directory by convention). Personas describe **how much** to surface at once; [`.advanced/PERSONAS.md`](.advanced/PERSONAS.md) is the operational map. **Persona 1** should not need anything under `.advanced/` on day one.

---

## Portability (mobile, desktop, many tools)

Committed files are **markdown-first** and **tool-agnostic** (`AGENTS.md`, `SPEC.md`, `CONTEXT_TRANSFER` pattern, etc.) so the same repo works across IDE assistants and chat models. **How** to work on mobile vs desktop is in `README.md` and `SOP.md`; this file only states that **portability is intentional**.

---

## Research before reinventing

Prefer **borrowing and citing** existing patterns (spec-driven workflows, prior art, community templates) over duplicating whole ecosystems. This reinforces **Rule #3**. See **Researching Prior Art** in [`SOP.md`](SOP.md) and **Background and Further Reading** in [`README.md`](README.md).

---

## Specs vs code (sharing and layout)

**Default pattern for this template:** a **markdown-only planning repository** separate from **implementation** (code or production tools), often as a **second repository**. That gives the cleanest story for **sharing ideas without sharing generated code** and keeps **default IDE context** small.

Alternatives (one repo with `docs/` + gitignored `src/`, etc.) are possible for advanced users but carry **leak and indexing** risks—see discussion in maintainer planning if you fork for your own process.

---

## Template user vs template maintainer artifacts

- **Root `TODO.md`:** **template user** checklist—next steps for *your* planned outcome (see file header). **Not** upstream maintainer milestones.
- **`.dev/TODO.md`:** milestones for **evolving the shared template** (maintainers). A template user’s **spec** still lives in **`SPEC.md`** and local **`CONTEXT.md`**; optionally gitignored **`TASKS.md`** from `TASKS.example.md`.
- **`DEV.md`:** public maintainer guide. Tracked **`.dev/`** holds **shared** maintainer-layer docs (including **`.dev/AGENTS.md`** for assistants when the human states maintainer context)—see `DEV.md` and root `AGENTS.md`.

See [`.advanced/AUDIENCE.md`](.advanced/AUDIENCE.md) for role names and synonyms.

---

## Related

- [`README.md`](README.md) — onboarding and file map  
- [`SOP.md`](SOP.md) — workflows, tokens, prior art  
- [`SECURITY.md`](SECURITY.md) — Rule #1 detail  
- [`AGENTS.md`](AGENTS.md) — assistant contract  
- [`.advanced/AUDIENCE.md`](.advanced/AUDIENCE.md) — template user, maintainer, product audience  
- [`.dev/TODO.md`](.dev/TODO.md) — maintainer milestones (upstream); root [`TODO.md`](TODO.md) — template user checklist  
