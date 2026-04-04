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

## Audience and outcomes

The template serves **novices through experts**, for **creative and technical** work alike. “Product” in [`SPEC.md`](SPEC.md) means whatever outcome you are specifying (software, story, game, event, research, course, …)—the same files support different domains.

---

## Progressive disclosure (Personas 1–4)

Optional depth lives under **`.advanced/`** (a dot-directory by convention). Personas describe **how much** to surface at once; [`.advanced/PERSONAS.md`](.advanced/PERSONAS.md) is the operational map. **Persona 1** should not need anything under `.advanced/` on day one.

---

## Portability (mobile, desktop, many tools)

Committed files are **markdown-first** and **tool-agnostic** (`AGENTS.md`, `SPEC.md`, `CONTEXT_TRANSFER` pattern, etc.) so the same repo works across IDE assistants and chat models. **How** to work on mobile vs desktop is in `README.md` and `SOP.md`; this file only states that **portability is intentional**.

---

## Research before reinventing

Prefer **borrowing and citing** existing patterns (spec-driven workflows, prior art, community templates) over duplicating whole ecosystems. See **Researching Prior Art** in [`SOP.md`](SOP.md) and **Background and Further Reading** in [`README.md`](README.md).

---

## Specs vs code (sharing and layout)

**Default pattern for this template:** a **markdown-only planning repository** separate from **implementation** (code or production tools), often as a **second repository**. That gives the cleanest story for **sharing ideas without sharing generated code** and keeps **default IDE context** small.

Alternatives (one repo with `docs/` + gitignored `src/`, etc.) are possible for advanced users but carry **leak and indexing** risks—see discussion in maintainer planning if you fork for your own process.

---

## Maintainer vs fork user artifacts

- **Root `TODO.md` (this upstream template):** milestones for **evolving the template**—not your product backlog. Your work lives in **`SPEC.md`** and local **`CONTEXT.md`**; optionally gitignored **`TASKS.md`** from `TASKS.example.md`.
- **`DEV.md`:** public maintainer guide. Optional **local `.dev/`** (gitignored) holds **pair-specific** maintainer preferences—see `DEV.md` and `AGENTS.md`.

---

## Related

- [`README.md`](README.md) — onboarding and file map  
- [`SOP.md`](SOP.md) — workflows, tokens, prior art  
- [`SECURITY.md`](SECURITY.md) — Rule #1 detail  
- [`AGENTS.md`](AGENTS.md) — assistant contract  
