# Spec-Driven Development Template (Markdown-Only)

## What This Is
A markdown-only, planning-first template for spec-driven development with AI. It is intentionally inert: no executable code lives here, only specifications, context, and workflows for coordinating multiple AI tools.

## Who This Is For
- Developers and tinkerers exploring AI-assisted planning.
- People using multiple assistants (IDE plugins and chat models) across desktop and mobile.
- Anyone who wants a portable, tool-agnostic way to describe what they are building before they write code.

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

All real implementation work and executable code should live in a **separate implementation repository** that you create once you are ready, following the guidance in `SECURITY.md` and `HUMAN.md`.

## How to Start (Minimal Path)
This matches **Persona 1** by default; other personas may add steps — see `advanced/PERSONAS.md`.

1. Read `AGENTS.md` to understand how AI assistants should behave in this repo.
2. Skim `SECURITY.md` to understand the safety and “no secrets / no code” rules.
3. Open `SPEC.md` and start drafting what you want to build.
4. Use your own `CONTEXT.md` (or a similar file) as a live snapshot for daily work.
5. Refer to `SOP.md` for suggested day-to-day workflows with multiple tools and devices.

You can have a complete, useful planning loop using only the required files in the project root.

## Core Files in the Root
- `README.md` – Overview, intent, and how to get started.
- `SPEC.md` – Main product and feature specifications.
- `SOP.md` – Standard operating procedures for working with AI tools and this template.
- `SECURITY.md` – Safety boundaries, “no secrets / no code” policy, and how to graduate to a real implementation repo.
- `HUMAN.md` – Private human context and a personal gate for when to start real implementation work.
- `AGENTS.md` – Instructions and priorities for all agents and AI models operating in this repo.
- `CONTEXT.md` – A live project snapshot for your own use (this template describes a shape; your contents are private).
- `CONTEXT_TRANSFER.md` – Optional ephemeral handoff between sessions or devices; overwrite each time; do not put secrets in it. For model-generated handoffs with explicit provenance, use the naming pattern **`CONTEXT_TRANSFER_FROM_<MODEL>_<PLATFORM>.md`** (documented inside `CONTEXT_TRANSFER.md`).

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
When you decide you are ready to write real code:
1. Review `HUMAN.md` and `SECURITY.md` to confirm your own criteria and boundaries.
2. Create a new repository for implementation code.
3. Copy over only the specifications and documents you want to use there.
4. Keep this template repository as a planning and reference space, or fork it for your next project.

### Quickstart Prompt for When You’re Ready to Code
If you have read and understood the rules above and want help getting started with real code, you can paste a prompt like this into your assistant:

> I have read and understand this template’s rules (markdown-only, no code, no secrets).  
> Help me create a **separate implementation repository** for my project.  
> 1) Propose a minimal folder and file structure for the new repo.  
> 2) Tell me which specs from this template I should copy over.  
> 3) Once we’re “inside” that new repo, it’s okay to generate code there, but **never in this template repo**.

