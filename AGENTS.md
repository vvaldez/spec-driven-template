# AGENTS.md

## Read This First (For All Agents and Models)
If you are an AI assistant, agent, or tool operating in this repository, read and respect this file before doing anything else.

This is a **markdown-only, planning-first template**. Your job here is to help the human think, plan, and organize. You must not turn this repository into an executable codebase.

If a human is skimming this file, the single most important next step is:
- **Read `README.md`** to understand what this template is, why it is markdown-only, and how to get started safely.

If the human is **maintaining or changing the template repository itself** (not using a fork only for their own product plan), they should also read **`DEV.md`** and **`TODO.md`** for maintainer scope, milestones, and workflow—without confusing those with the end-user’s **`SPEC.md`**.

This `AGENTS.md` pattern grew out of real-world experience converting a provider-specific configuration file (for example, a `GEMINI.md` used to boot a particular agent) into a single, tool-agnostic set of rules. Treat this file as the shared contract for any assistant, regardless of vendor.

## Repository Rules
- **Markdown-only**: Do not create or modify executable code, scripts, binaries, or configuration files intended for direct execution.
- **No dependencies or build setup**: Do not add package manifests, build pipelines, or tooling configuration that turns this into a runnable project.
- **No secrets**: Never introduce or store secrets, API keys, tokens, passwords, or private data in this repository.
- **Separate implementation repos**: If the human asks for code, guide them to create or use a separate implementation repository and operate there instead.
- **Planning and creativity only**: Focus on helping clarify specs, workflows, risks, and ideas—not automating risky changes.

When a human explicitly wants to generate real code, assistants should:
- Remind them that this repository is planning-only.
- Point them to the high-level steps in `README.md`, `SECURITY.md`, and `HUMAN.md` for creating a separate implementation repository.
- If they use `HUMAN.md`, mention the optional **Acknowledgment before code** ritual so they pause and record a dated line before treating an implementation repo as “open season”; you cannot verify git state—only remind them.

## File Reading Order and Priorities
When you start working in this repository:
1. Read `AGENTS.md` (this file) to learn the rules.
2. Read `README.md` to understand the overall intent and structure.
3. Read `SECURITY.md` to internalize safety and privacy expectations.
4. If the human indicates, read their `CONTEXT.md` (or equivalent) to understand the current project state.
5. Read `SPEC.md` and `SOP.md` to understand what they are building and how they prefer to work.
6. Only look into `advanced/` files when the human explicitly mentions them or asks for deeper structure — **unless** the human states a persona or asks you to follow `advanced/PERSONAS.md` (see below).

## Persona-Aware Behavior
- If the human **does not** state a persona, assume **minimal disclosure**: prioritize root files (`README.md`, `SPEC.md`, `SOP.md`, `SECURITY.md`) and avoid surfacing the whole `advanced/` tree at once.
- If the human names a **persona (1–4)** or points to **`advanced/PERSONAS.md`**, read that file and follow the **recommended path** for that persona: which files to suggest next, how deep to go, and what to skip.
- **Persona 4 (Full-Stack AI Developer)** is the exception to hiding `advanced/`: you may summarize `advanced/` as an optional menu or browse list so they can navigate quickly; still do not overwhelm with full file dumps unless they ask.
- If the human asks you to respect their saved persona, read **`HUMAN.md`** → **“My persona (optional)”** when they explicitly invite you to use `HUMAN.md`.

## How to Treat `HUMAN.md`
- `HUMAN.md` exists primarily for the human’s own notes, constraints, and decisions.
- By default, **do not** read from or write to `HUMAN.md` unless the human explicitly asks you to.
- When invited to use `HUMAN.md`, treat it as a guide for:
  - How the human prefers you to behave.
  - When and how they want to create or update a separate implementation repository.
  - Their optional **persona** line, if present, aligned with `advanced/PERSONAS.md`.

## Guidelines by Agent Type

### IDE / Editor Assistants (e.g., Cursor, Copilot, Gemini Code Assist, Codeium)
- Prefer working inside markdown files only.
- Offer structured edits (headings, lists, tables) instead of proposing code files.
- If asked to refactor or generate code, suggest moving that work into a separate implementation repository.

### Chat-Based Models (Desktop)
- Summarize and cross-reference specs, context, and workflows.
- Help the human update documents consistently and safely.
- Ask clarifying questions when instructions conflict with the rules in this file.

### Chat-Based Models (Mobile / On-the-Go)
- Assume mobile use may be low-attention (for example, while walking, in line, or using voice input).
- Focus on lightweight planning: outlines, bullet lists, and small spec updates the human can reconcile later.
- Keep responses brief and easy to listen to or skim on a small screen.
- Be extra conservative about suggesting large-scale changes; favor ideas and options over edits.
- End mobile-oriented sessions with a short recap and clear next steps the human can pick up on desktop.

## Creativity and Planning Guidelines
- Encourage exploratory thinking and multiple options when designing features or workflows.
- Clearly label speculation, assumptions, and trade-offs.
- When suggesting changes across multiple files, describe the plan first so the human can decide what to apply.
- Do not silently introduce complexity; keep the experience simple at first, and only suggest advanced structures (like files in `advanced/`) when the human expresses interest or needs more organization.

