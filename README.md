# Spec-Driven Development Template (Markdown-Only)

## What This Is
A markdown-only, planning-first template for **spec-driven work** with AI. “Spec” means any structured plan you care about—not only software. This repository is intentionally inert: no executable code lives here, only specifications, context, and workflows for coordinating multiple AI tools.

## Who This Is For
- Developers and tinkerers exploring AI-assisted planning for apps and systems.
- **Creative and non-software work**: story or character development, game narrative and content bibles, play or screenplay structure, research notes, events, courses, or any project where you want clarity before you “produce” the final artifact.
- People using multiple assistants (IDE plugins and chat models) across desktop and mobile.
- Anyone who wants a portable, tool-agnostic way to describe an outcome—whether that outcome is code, a manuscript, a design doc, or something else—**before** heavy implementation elsewhere.

## Choose Your Persona (First Session)

This template defines **four personas** in [`advanced/PERSONAS.md`](advanced/PERSONAS.md). Each persona has a recommended reading path so you are not overwhelmed.

**Short summary**

| Persona | Who it fits |
| --- | --- |
| **1 – Curious Non-Developer** | Not a programmer; you want plain-language planning and gentle AI help. |
| **2 – Developer, AI Novice** | You write code; you want structure and a clear planning-before-code workflow. |
| **3 – AI-Native Non-Developer** | Strong at prompting; you want coordination across tools without coding as the focus. |
| **4 – Full-Stack AI Developer** | You code with AI daily; you want the full template and `advanced/` as a quick menu. |

**Default:** If you are unsure, treat yourself as **Persona 1** and follow that path in `advanced/PERSONAS.md` first (README → AGENTS → SPEC vision → `advanced/GETTING_STARTED_WITH_ASSISTANTS.md`).

**Tell your assistant which persona to use** — paste something like this on your first message (change the number or wording as needed):

> I’m using the spec-driven-template repo (markdown-only, no code here). I identify most with **Persona [1, 2, 3, or 4]** in `advanced/PERSONAS.md` — or between [e.g. 1 and 2]. Please follow that persona’s recommended file path: suggest only the next 2–3 files to read, keep answers concise until I ask for more, and don’t dump all of `advanced/` unless I match Persona 4 or I ask for it.

You can also record a stable choice in **`HUMAN.md`** under **“My persona (optional)”** and ask assistants to respect it when you invite them to read that file.

## Why Markdown-Only (No Code Here)
- Keeps this repository safe to share and fork.
- Encourages creativity and careful thinking instead of auto-generating code.
- Makes it easy to use from any environment, device, or AI assistant.

When you are ready to **implement**—whether that means writing code, locking a final draft, building game content in tools, or rehearsing from a script—do that work in a **separate space** (often a second repository for software, or your usual creative toolchain). This planning repo stays markdown-only; follow `SECURITY.md` and `HUMAN.md` when you graduate.

## Setup After Clone (Local Context Files)

**`CONTEXT.md`**, **`CONTEXT_TRANSFER.md`**, and **`CONTEXT_TRANSFER_FROM_*.md`** are **gitignored** so your live notes and handoffs are not pushed by accident. After cloning or forking, copy the tracked templates once:

```bash
cp CONTEXT.example.md CONTEXT.md
cp CONTEXT_TRANSFER.example.md CONTEXT_TRANSFER.md
```

(On Windows PowerShell you can use `Copy-Item`.) Edit those local files freely; they stay on your machine unless you change `.gitignore`.

### Teams and sharing `CONTEXT*` files

This repo is set up so **`CONTEXT.md`**, **`CONTEXT_TRANSFER.md`**, and **`CONTEXT_TRANSFER_FROM_*.md`** stay **private by default** (gitignored). That still supports collaboration: everyone aligns on **shared, committed** docs (`SPEC.md`, `SOP.md`, `DECISIONS.md`, etc.) while each person keeps **their own** live context and handoffs local — which matches how most teams work today with AI tools, where each person’s scratch notes and session state differ.

If you work with **multiple people** and decide you **want** to share those `CONTEXT*` files, you can remove or adjust the relevant lines in `.gitignore` and commit them. Only do that after **everyone understands** that whatever goes into git is **visible to collaborators** and **retained in git history** (including if the repo is later forked or made public). There is no obligation to share them; the default is intentionally cautious.

## How to Start (Minimal Path)
This matches **Persona 1** by default; other personas may add steps — see `advanced/PERSONAS.md`.

1. Read `AGENTS.md` to understand how AI assistants should behave in this repo.
2. Skim `SECURITY.md` to understand the safety and “no secrets / no code” rules.
3. Open `SPEC.md` and start drafting what you want to create (product, story, game, event—see `SPEC.md` for scope).
4. Use your own `CONTEXT.md` (or a similar file) as a live snapshot for daily work.
5. Refer to `SOP.md` for suggested day-to-day workflows with multiple tools and devices.

You can have a complete, useful planning loop using only the required files in the project root.

## Core Files in the Root
- `README.md` – Overview, intent, and how to get started.
- `SPEC.md` – Main specifications for your outcome (software, creative work, or hybrid); see file header for how to read “product” and “features.”
- `SOP.md` – Standard operating procedures for working with AI tools and this template.
- `SECURITY.md` – Safety boundaries, “no secrets / no code” policy, and how to graduate to a real implementation repo.
- `HUMAN.md` – Private human context and a personal gate for when to start real implementation work.
- `AGENTS.md` – Instructions and priorities for all agents and AI models operating in this repo.
- `CONTEXT.example.md` – Tracked template for a live project snapshot; **copy to `CONTEXT.md`** (gitignored) after clone.
- `CONTEXT_TRANSFER.example.md` – Tracked template for session handoffs; **copy to `CONTEXT_TRANSFER.md`** (gitignored). Model-generated provenance files use **`CONTEXT_TRANSFER_FROM_<MODEL>_<PLATFORM>.md`** (also gitignored); full convention is documented inside `CONTEXT_TRANSFER.example.md`.
- `DEV.md` – **Template maintainers only**: scope and SOP for evolving *this* repository; see `TODO.md` for maintainer milestones. Skip if you are only using the repo to plan your own product.
- `TODO.md` – Maintainer milestone checklist for the template itself (not your product backlog—use `SPEC.md` for that).

## Advanced Docs in `advanced/` (Unlock Later)
The `advanced/` directory contains optional documents that add structure and depth once the basics feel comfortable. You do **not** need any of them to start.

Examples include:
- Reading paths by persona (`advanced/PERSONAS.md`).
- Architecture and data model templates.
- Feature indexes, decision logs, risk registers.
- Model catalogs, prompt libraries, milestone timelines.
- Story and example files, including a case study that inspired this template.

Treat `advanced/` as expansions you unlock when you are curious, not prerequisites.

If you are new to AI coding assistants, you can also look at:
- `advanced/GETTING_STARTED_WITH_ASSISTANTS.md` – a gentle introduction to what these tools are and how to use them with this template.

## Using This Template With Different Tools
This template is intentionally tool-agnostic. It is designed to work equally well with IDE assistants (GitHub Copilot, Cursor, Gemini Code Assist, Codeium, and similar tools) and chat-first models (Claude, ChatGPT, Gemini, Perplexity, Poe, Replit Agents, and others). It also plays nicely alongside classic spec and modeling tools like OpenAPI/Swagger, AsyncAPI, JSON Schema, the C4 model, and Mermaid or PlantUML diagrams for architecture and flows. The goal is to give you a lightweight, markdown-only backbone for specs and workflows that you can plug into whatever combination of AI assistants and developer tools you already use.

## Background and Further Reading
If you want to explore related work and prior art:
- GitHub blog: “Spec-driven development: Using Markdown as a programming language when building with AI” – an introduction to spec-first workflows using Markdown and AI assistants.
- GitHub Spec Kit – a toolkit and templates for spec-driven development workflows.
- Projects such as `spec-kitty` and `spec-driven-workflow` – examples of applying spec-driven ideas in different environments.

This template focuses specifically on being:
- Markdown-only and permanently inert (no compile-to-code path here).
- Multi-model and multi-device friendly (desktop and mobile, multiple assistants).
- Structured like a gentle tutorial, starting simple and slowly revealing more optional depth.

## Creating a Separate Implementation Repository (When Ready)
When you decide you are ready to **implement** (e.g. write code, or move creative work into production tools):

1. Review `HUMAN.md` and `SECURITY.md` to confirm your own criteria and boundaries.
2. If you will use **code**, complete the optional **acknowledgment ritual** in `HUMAN.md` (*Acknowledgment before code*) so you pause before the first implementation repo—not enforced by software, but recommended friction.
3. Create a **new repository or workspace** for implementation (typical for software; for purely creative work, your “implementation” might be Scrivener, a game engine, or a shared drive—still keep this template as planning-only).
4. Copy over only the specifications and documents you want to use there.
5. Keep this template repository as a planning and reference space, or fork it for your next project.

### Quickstart Prompt for When You’re Ready to Code
If you have read and understood the rules above and want help getting started with **real code** in a **separate** repo, paste a prompt like this (include your acknowledgment line from `HUMAN.md` if you use that ritual):

> I have read and understand this template’s rules (markdown-only, no code, no secrets in the planning repo).  
> I have added my acknowledgment line to `HUMAN.md` under “Acknowledgment before code” (paste the same line here if you like).  
> Help me create a **separate implementation repository** for my project.  
> 1) Propose a minimal folder and file structure for the new repo.  
> 2) Tell me which specs from this template I should copy over.  
> 3) Once we’re “inside” that new repo, it’s okay to generate code there, but **never in this template repo**.

