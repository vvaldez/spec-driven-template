# SOP.md

## Purpose of This SOP
This document describes how to work with this markdown-only, spec-driven template in a consistent, safe, and creative way. It focuses on planning and coordination with AI assistants across devices and tools.

## Git Workflow (Contributing to This Template)
For substantive edits to the template itself, use a **feature branch** and open a **pull request** to `main` rather than committing large changes directly on `main`. Small doc fixes can stay on `main` if that matches your workflow, but branches keep history reviewable and match how many teams work with shared repos.

**Maintainer milestones** for the template live in **`TODO.md`**; scope and maintainer-only process are summarized in **`DEV.md`** (distinct from a fork user’s product spec in **`SPEC.md`**).

## Principles
- **Planning-only**: Use this repository for specifications, context, and workflows—not for executable code.
- **Markdown-only**: Keep all content in human-readable markdown files.
- **Multi-model, multi-device**: Assume you may switch between different AI tools and between desktop and mobile.
- **Simple first**: Start with a minimal set of files and structure; only add more when it clearly helps.
- **Research before reinventing**: Look for prior art and existing patterns before designing something new, and avoid duplicating work when a suitable approach already exists.

## Daily Workflow – Desktop
1. Open `SPEC.md` and review what you are currently defining or refining.
2. Skim your `CONTEXT.md` (or equivalent) to recall the current phase and priorities.
3. Consult `SOP.md` and `SECURITY.md` if you are unsure about process or safety.
4. Use your preferred IDE assistants (e.g., Cursor, Copilot, Gemini Code Assist, Codeium) to help structure and edit markdown files.
5. Capture decisions and next steps in specs and context, not in transient chat only.

## Daily Workflow – Mobile / On-the-Go Planning
1. Use a chat-based model (e.g., Claude, ChatGPT, Gemini) to discuss and sketch ideas.
2. Focus on outlines, lists, and small spec updates the desktop environment can refine later.
3. Keep the conversation anchored to the documents in this repo (especially `SPEC.md` and your `CONTEXT.md`), not just free-floating chat.
4. Favor short, easy-to-skim or easy-to-listen-to responses, especially when your attention is limited.
5. When you return to desktop, reconcile mobile notes into the markdown files.

## Multi-Model Collaboration Patterns
- Use chat models for brainstorming, trade-off analysis, and rewriting sections of specs.
- Use IDE assistants for structured edits, navigation, and consistency checks across files.
- Clearly tell each assistant which files they should read and which they should ignore.

When you want the assistant to behave as a **named specialist during implementation** (e.g. security review, UX critique) inside a **code** repository or IDE workspace, you can optionally install or copy patterns from **third-party markdown agent libraries**. One example is [**agency-agents**](https://github.com/msitarzewski/agency-agents). Treat those as **add-ons for the implementation side**: they do not replace this template’s **`AGENTS.md`** in the **planning** repo, and they often conflict with “markdown-only here” if applied blindly—scope them to the repo or tool where code and automation belong.

## Session Handoffs (`CONTEXT_TRANSFER.md`)
For handoffs between devices, models, or sessions, use a local **`CONTEXT_TRANSFER.md`** (create it from **`CONTEXT_TRANSFER.example.md`** after clone; see `README.md`). Overwrite it each time with current focus, decisions, and open questions. It is ephemeral and should not contain private data or secrets. Point the next assistant at it (and optionally your private `CONTEXT.md`) when resuming work.

For **traceability**, you can ask a model to write a handoff to **`CONTEXT_TRANSFER_FROM_<MODEL>_<PLATFORM>.md`** (same sections as `CONTEXT_TRANSFER.md`) — for example `CONTEXT_TRANSFER_FROM_CLAUDE_MOBILE.md`. Merge or replace into `CONTEXT_TRANSFER.md` when you want a single file for the next assistant. Those `FROM_*` files and `CONTEXT_TRANSFER.md` are **gitignored** in this template so they are not pushed by default; see `CONTEXT_TRANSFER.example.md` for the full convention.

## How to Ask for Help (From Models or Humans)
You will get far better answers if you ask smart, well-contextualized questions. Before asking for help:

1. **Do minimal homework**
   - Skim the relevant docs (`README.md`, `SPEC.md`, this `SOP.md`, your `CONTEXT.md`).
   - Search the repo for obvious keywords.

2. **Include the right context in your question**
   - **Goal**: What you are trying to achieve.
   - **What you tried**: Steps you already took or ideas you considered.
   - **What happened**: The result, including any surprising behavior.
   - **What you want now**: The kind of help you are asking for (explanation, options, critique, next step).

3. **Ask specific, bounded questions**
   - Prefer “Help me choose between option A and B for this feature” over “What should I do?”.
   - Prefer “How can I simplify this section of `SPEC.md`?” over “Rewrite everything.” 

Assistants are encouraged to nudge you toward this pattern when your questions are too vague.

## Researching Prior Art
Before committing to new process patterns, templates, or structures:
1. Ask an assistant to search for existing spec-driven development tools and workflows (for example, GitHub Spec Kit and similar projects).
2. Skim a few examples to understand how others solve similar problems.
3. Decide explicitly what you want to borrow and what you want to do differently.
4. Document that rationale briefly in your specs or decision logs so future you remembers why.

## Updating Specs and Context
- Keep `SPEC.md` as the source of truth for what you are building.
- Use your `CONTEXT.md` (or equivalent) as a living snapshot of current status and focus.
- When you make meaningful changes to specs or workflow, briefly note why, and update any references in related docs.

## Creating and Using a Separate Implementation Repository
When you are ready to write code:
1. Review `HUMAN.md` to confirm your own criteria and boundaries for starting a real implementation project.
2. Review `SECURITY.md` to ensure you understand the “no secrets / no code here” policy.
3. Create a new implementation repository for actual code and automation.
4. Copy only selected specs and documents into that repository as needed.
5. Continue to treat this template repository as a planning and reference space, or fork it for future projects.

